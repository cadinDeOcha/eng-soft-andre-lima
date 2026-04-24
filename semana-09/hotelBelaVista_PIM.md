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


