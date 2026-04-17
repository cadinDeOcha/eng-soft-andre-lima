# Documento de Requisitos de Software (SRS)

## Informações do Projeto

| Campo | Descrição |
| :--- | :--- |
| **Nome do Projeto** | Sistema de Gestão Hotel Bela Vista |
| **Dono do Projeto** | Proprietário do Hotel Bela Vista |
| **Versão** | 1.0 |
| **Data** | 16/04/2026 |

## 1. Introdução

O objetivo deste documento é descrever os requisitos para o desenvolvimento do Sistema de Gestão Hotel Bela Vista. Este documento servirá como guia para a equipe de desenvolvimento, garantindo que todas as características e funcionalidades necessárias sejam implementadas conforme as expectativas dos stakeholders, visando modernizar a administração do hotel, que atualmente é feita de forma manual, e solucionar problemas como overbooking, perda de receitas de consumo e filas na recepção.

## 2. Escopo

O escopo do Sistema de Gestão Hotel Bela Vista inclui, mas não se limita às seguintes funcionalidades:

*   **Gestão de Reservas e Ocupação:** Visualização em tempo real do status dos quartos (livre, ocupado, limpeza) através de um mapa visual com cores, bloqueio automático de datas para evitar overbooking e gestão de diferentes tipos de quartos com preços variados.
*   **Controle de Hóspedes e Consumo:** Cadastro rápido de hóspedes, consulta de histórico, registro de consumo vinculado diretamente ao quarto e gestão de pagamentos antecipados (sinal).
*   **Fechamento de Conta e Financeiro:** Cálculo automático do valor total da estadia (diárias mais consumo, descontando o sinal pago), relatórios de faturamento diário e mensal, e relatórios de ocupação.
*   **Operação e Limpeza:** Atualização do status de limpeza dos quartos pelas camareiras através de dispositivos móveis (celulares), refletindo instantaneamente na recepção.

## 3. Requisitos Funcionais

### 3.1 Gestão de Reservas e Ocupação

| ID | Descrição do Requisito |
| :--- | :--- |
| **RF 1.1** | O sistema deve exibir um mapa visual dos quartos com indicação de status por cores (livre, ocupado, sujo, limpo). |
| **RF 1.2** | O sistema deve permitir o cadastro de reservas informando datas e quarto, bloqueando automaticamente o quarto selecionado para o período. |
| **RF 1.3** | O sistema deve impedir reservas duplicadas para o mesmo quarto e período, emitindo um alerta ao tentar reservar um quarto já ocupado. |
| **RF 1.4** | O sistema deve permitir o cadastro de diferentes tipos de quartos (simples, luxo, família) e associar preços diferentes para cada tipo. |
| **RF 1.5** | O sistema deve calcular automaticamente o valor da diária com base no tipo de quarto selecionado na reserva. |

### 3.2 Controle de Hóspedes e Consumo

| ID | Descrição do Requisito |
| :--- | :--- |
| **RF 2.1** | O sistema deve permitir o cadastro rápido de hóspedes com dados essenciais (nome, CPF e telefone) e a consulta ao histórico de estadias anteriores. |
| **RF 2.2** | O sistema deve permitir o registro de consumos (produtos/serviços) e vinculá-los automaticamente à conta do quarto correspondente. |
| **RF 2.3** | O sistema deve permitir o registro de pagamento antecipado (sinal) e identificar visualmente quais reservas possuem sinal pago. |

### 3.3 Fechamento de Conta e Financeiro

| ID | Descrição do Requisito |
| :--- | :--- |
| **RF 3.1** | O sistema deve calcular automaticamente o valor total da estadia, somando diárias e consumo, e descontando automaticamente o valor do sinal pago. |
| **RF 3.2** | O sistema deve permitir o fechamento da conta (checkout) de forma rápida para evitar filas na recepção. |
| **RF 3.3** | O sistema deve gerar e apresentar relatórios simples de faturamento diário, faturamento mensal e ocupação dos quartos. |

### 3.4 Operação e Limpeza

| ID | Descrição do Requisito |
| :--- | :--- |
| **RF 4.1** | O sistema deve permitir que a camareira atualize o status do quarto (ex: de sujo para limpo) utilizando um dispositivo móvel (celular). |
| **RF 4.2** | O sistema deve refletir a atualização do status de limpeza em tempo real no mapa visual da recepção. |

## 4. Requisitos Não Funcionais

*   **RNF 4.1:** O sistema deve possuir uma interface simples, intuitiva e de fácil uso, adequada a usuários não técnicos, evitando excesso de botões e complexidade desnecessária.
*   **RNF 4.2:** O sistema deve ser responsivo, estando disponível e funcional tanto em computadores (foco na recepção) quanto em dispositivos móveis (celulares para o dono e camareiras).
*   **RNF 4.3:** O sistema deve garantir a atualização em tempo real das informações, especialmente o status dos quartos e o mapa de ocupação.

## 5. Design da Interface do Usuário (UI)

*   **Design 1:** A interface principal (painel de controle) deve apresentar um mapa visual dos quartos utilizando um esquema de cores claro e intuitivo (ex: verde para livre, vermelho para ocupado, amarelo para limpeza), visando não forçar a vista do usuário.
*   **Design 2:** O fluxo de navegação deve ser direto, permitindo realizar ações comuns (como check-in, checkout e registro de consumo) com o mínimo de cliques possível, priorizando a agilidade no atendimento no balcão. A interface móvel para camareiras deve ser minimalista, focada apenas na seleção do quarto e alteração de status.

## 6. Arquitetura do Sistema

*   **Arquitetura 1:** O sistema deve adotar uma arquitetura baseada em nuvem (Web Application) para permitir o acesso remoto de qualquer dispositivo conectado à internet, garantindo que o proprietário possa acompanhar o hotel de casa.
*   **Arquitetura 2:** Recomenda-se o uso de tecnologias web modernas para o frontend (ex: React ou Vue.js) para garantir a reatividade em tempo real do mapa de quartos, e um backend robusto (ex: Node.js ou Python) com banco de dados relacional para garantir a integridade das transações financeiras e reservas.

## 7. Requisitos de Dados

*   **RD 7.1:** O banco de dados deve modelar entidades principais como Quartos (com tipo e status), Hóspedes, Reservas (com datas, status de sinal e valor), e Consumos (itens e valores vinculados à reserva).
*   **RD 7.2:** O sistema deve realizar backups automáticos e contínuos em ambiente seguro na nuvem ("cofre digital"), garantindo que nenhum dado seja perdido em caso de falha de hardware (ex: queima do computador local ou falta de energia).

## 8. Requisitos de Segurança

*   **RS 8.1:** O sistema deve implementar perfis de acesso distintos: Administrador (Dono do hotel, com acesso total a relatórios e configurações), Recepcionista (acesso a reservas, check-in/out e consumo) e Camareira (acesso restrito apenas à alteração de status de limpeza dos quartos).
*   **RS 8.2:** Todos os dados trafegados entre os dispositivos (computador da recepção, celulares) e o servidor na nuvem devem ser criptografados utilizando protocolos de segurança padrão (HTTPS/TLS) para proteger as informações pessoais dos hóspedes e dados financeiros.

## 9. Requisitos de Desempenho

*   **RP 9.1:** O sistema deve ser capaz de processar atualizações de status de quartos (ex: camareira marcando como limpo) e refleti-las no painel da recepção em menos de 2 segundos, garantindo a fluidez da operação.
*   **RP 9.2:** O sistema deve suportar acessos simultâneos sem degradação de performance, considerando o uso concorrente pelo computador da recepção, o celular do proprietário e os celulares das camareiras.

## 10. Requisitos de Teste

*   **RT 10.1:** Devem ser realizados testes rigorosos nas regras de negócio de reservas para garantir a impossibilidade absoluta de overbooking (reservas duplicadas para o mesmo quarto/data).
*   **RT 10.2:** Os testes de aceitação do usuário (UAT) devem ser conduzidos com o proprietário e a equipe da recepção, validando a simplicidade da interface, a clareza do mapa de cores e a precisão dos cálculos automáticos de checkout e desconto de sinal.

## 11. Cronograma do Projeto

| Tarefa | Data de Início | Data de Término |
| :--- | :--- | :--- |
| Levantamento de Requisitos | 16/04/2026 | 23/04/2026 |
| Design e Prototipagem | 24/04/2026 | 08/05/2026 |
| Desenvolvimento | 09/05/2026 | 20/06/2026 |
| Testes | 21/06/2026 | 05/07/2026 |
| Implantação | 06/07/2026 | 10/07/2026 |

## Revisões

| Versão | Data | Descrição |
| :--- | :--- | :--- |
| 1.0 | 16/04/2026 | Versão inicial baseada no levantamento de requisitos com o proprietário do Hotel Bela Vista. |

## Assinaturas

**Dono do Projeto:** André Frigo Lima

**Gerente de Projeto:** André Frigo Lima
