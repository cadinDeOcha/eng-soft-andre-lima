# PIM (Platform Independent Module) - Sistema de Gestão Hotel Bela Vista

Este documento apresenta o Platform Independent Module (PIM) para o Sistema de Gestão do Hotel Bela Vista, conforme os requisitos levantados e validados. O PIM é dividido em três partes principais, utilizando diagramas UML para representar a interação, a estrutura e o comportamento do sistema.

## Parte 1: Interação - Diagrama de Sequência

O Diagrama de Sequência ilustra a ordem das interações entre os atores e os objetos do sistema para um cenário específico. Abaixo, é apresentado o fluxo de registro de uma reserva com pagamento de sinal.

### Cenário: Registro de Reserva com Sinal

```mermaid
sequenceDiagram
    actor Recepcionista
    participant Sistema
    participant BancoDados

    Recepcionista->>Sistema: Iniciar Reserva (datas, tipo quarto)
    Sistema->>BancoDados: Verificar disponibilidade
    BancoDados-->>Sistema: Lista de quartos disponíveis
    Sistema-->>Recepcionista: Exibir quartos disponíveis
    
    Recepcionista->>Sistema: Selecionar Quarto e Hóspede
    Sistema->>Recepcionista: Solicitar confirmação de Sinal
    
    Recepcionista->>Sistema: Registrar Pagamento de Sinal
    Sistema->>BancoDados: Salvar Reserva (Status: Reservado com Sinal)
    BancoDados-->>Sistema: Confirmação
    
    Sistema-->>Recepcionista: Reserva Confirmada com Sucesso
```

![Diagrama de Sequência - Registro de Reserva](https://private-us-east-1.manuscdn.com/sessionFile/8Y2degcgtlIvRAUkICSmL5/sandbox/rxKg5tWOKStBFm2CGLUYAP-images_1776994091762_na1fn_L2hvbWUvdWJ1bnR1L3NlcXVlbmNlX2RpYWdyYW0.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvOFkyZGVnY2d0bEl2UkFVa0lDU21MNS9zYW5kYm94L3J4S2c1dFdPS1N0QkZtMkNHTFVZQVAtaW1hZ2VzXzE3NzY5OTQwOTE3NjJfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzTmxjWFZsYm1ObFgyUnBZV2R5WVcwLnBuZyIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTc5ODc2MTYwMH19fV19&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=J7gezoMfn95nCydEH-c~QYyMMLSTxKuJhfJwSuxKceKN2cgwmhEXEFsx8E87LrqNyHprZswDrhZpMF7H1VcU2ItGvvgBtfRHDhNZ0sz5M~LUzyZY7lZZdft2UEjjOzrQwf0tPm8vC7RhmvcxCgk8vJtlvcTO4-wyTnyVU5Hn58FaI7bGbBi9ZFbgIyX7T7jajKaV-k~UPQSIW7vQ~dY4wNdosiSptmvBPf11E8G2oeUZiq14iA~yQljEgKQU7-KUpGR~kDupmbaLvI8gL5PbAi1rTn~TD4oGuMR1maRqCbF~btAK15DxXFGzwHktwKmsqEltPwG3WZgWcUo1L6g0Rw__)

## Parte 2: Estrutural - Diagrama de Classes

O Diagrama de Classes representa a estrutura estática do sistema, mostrando as classes, seus atributos, métodos e os relacionamentos entre elas. Este diagrama reflete as entidades principais do domínio do Hotel Bela Vista.

```mermaid
classDiagram
    class Hotel {
        +String nome
        +String endereco
    }

    class Quarto {
        +int numero
        +TipoQuarto tipo
        +StatusQuarto status
        +float precoBase
        +atualizarStatus(novoStatus)
    }

    class TipoQuarto {
        <<enumeration>>
        SIMPLES
        LUXO
        FAMILIA
    }

    class StatusQuarto {
        <<enumeration>>
        LIVRE
        OCUPADO
        SUJO
        LIMPEZA_EM_ANDAMENTO
    }

    class Hospede {
        +String nome
        +String cpf
        +String telefone
        +consultarHistorico()
    }

    class Reserva {
        +DateTime dataEntrada
        +DateTime dataSaida
        +float valorSinal
        +boolean sinalPago
        +StatusReserva status
        +calcularTotal()
        +registrarSinal(valor)
    }

    class Consumo {
        +String descricao
        +float valor
        +DateTime dataHora
    }

    class Funcionario {
        +String nome
        +String cargo
    }

    Hotel "1" *-- "many" Quarto
    Quarto "1" -- "many" Reserva
    Hospede "1" -- "many" Reserva
    Reserva "1" *-- "many" Consumo
    Funcionario <|-- Recepcionista
    Funcionario <|-- Camareira
    Recepcionista ..> Reserva : gerencia
    Camareira ..> Quarto : limpa
```

![Diagrama de Classes - Hotel Bela Vista](https://private-us-east-1.manuscdn.com/sessionFile/8Y2degcgtlIvRAUkICSmL5/sandbox/rxKg5tWOKStBFm2CGLUYAP-images_1776994091762_na1fn_L2hvbWUvdWJ1bnR1L2NsYXNzX2RpYWdyYW0.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvOFkyZGVnY2d0bEl2UkFVa0lDU21MNS9zYW5kYm94L3J4S2c1dFdPS1N0QkZtMkNHTFVZQVAtaW1hZ2VzXzE3NzY5OTQwOTE3NjJfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwyTnNZWE56WDJScFlXZHlZVzAucG5nIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzk4NzYxNjAwfX19XX0_&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=kgyMNH6dD5zL3v3VNnYQ0dIl1xRbn2aT1GmbSfWwq1~TvuTbsXgJ8sgA0twg9mEXyUc4G1sZ85uxLP~fmrG1U9tWRd8nQMsWRB0oOPgcuiEvddFjq0HDEBYXsUCWAMxWBQw6335NQnZD3nOeC1C~RO4SEWlsLaSWdiSsQ0on1iO5CyKcI9hKXM3Fz~OywraYBCiruyGsaNFv3Oa5dTaRDTuNHDzjVLOgjWtKwmRes7wvg5mKDaIWrpXbALH-E-YwjEd~tz6nMnMhMlBnYLMT0g13g7qG7nW0~Cv3RR~raR~Xyir0XwlOvVkntiNvUGvJSqlTn79jpQw~uFq59AoR7w__)

## Parte 3: Comportamental - Diagrama de Estados

O Diagrama de Estados descreve os possíveis estados de um objeto (neste caso, um Quarto) e as transições entre esses estados em resposta a eventos. Ele modela o ciclo de vida de um quarto dentro do sistema.

```mermaid
stateDiagram-v2
    [*] --> Livre
    
    Livre --> Ocupado : Check-in
    Livre --> Reservado : Criar Reserva
    
    Reservado --> Ocupado : Check-in
    Reservado --> Livre : Cancelar Reserva
    
    Ocupado --> Sujo : Checkout
    
    Sujo --> LimpezaEmAndamento : Iniciar Limpeza (Camareira)
    LimpezaEmAndamento --> Livre : Finalizar Limpeza (Camareira)
    
    state Ocupado {
        [*] --> SemConsumo
        SemConsumo --> ComConsumo : Registrar Item
        ComConsumo --> ComConsumo : Registrar Item
    }
```

![Diagrama de Estados - Quarto](https://private-us-east-1.manuscdn.com/sessionFile/8Y2degcgtlIvRAUkICSmL5/sandbox/rxKg5tWOKStBFm2CGLUYAP-images_1776994091762_na1fn_L2hvbWUvdWJ1bnR1L3N0YXRlX2RpYWdyYW0.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvOFkyZGVnY2d0bEl2UkFVa0lDU21MNS9zYW5kYm94L3J4S2c1dFdPS1N0QkZtMkNHTFVZQVAtaW1hZ2VzXzE3NzY5OTQwOTE3NjJfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzTjBZWFJsWDJScFlXZHlZVzAucG5nIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzk4NzYxNjAwfX19XX0_&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=AzlVTLUpYY3sHlLLwDb~D1ekMjUxIPl41mRz1H7Ep2hyeYVsYN4IPgsNeBcafqu3r~eUr7F4D1BHMr-oZyrNK2bK~JN-JW0XhqGJqqiUomd28T2TfDmEcHpwX5Exq9rFxLDX6UtAoyvCNDzxYCgjW9uZDQCvVl5yrSHOW23o~n7L6yMH96rdspueUTWtIPEvJya9QZdL1E0oo4wjqztpf6fXkQRO4wsTj~cyYWIGM9wEa7V94S68WwLjORCIcKN-Qm1i4RGd~h~A4LGEbqpzZPodE7vTdXTTBY2SN6Zx0INtbu9j9xUlEqPfl8tGA3TI0OmfRIlV7yTP5h6dahaGHg__)
