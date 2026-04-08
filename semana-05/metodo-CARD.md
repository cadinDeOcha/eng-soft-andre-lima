## Parte 1: Descrição do aplicativo por parte do cliente (Levantamento de Necessidades)

Preciso de um aplicativo para resolver um problema que venho enfrentando. Moro em uma cidade onde acontecem muitas chuvas fortes, e frequentemente há **alagamentos em algumas regiões**. O problema é que:

- Não existe um sistema eficiente de alerta em tempo real
- Muitas pessoas só descobrem o alagamento quando já estão no local
- Rotas alternativas não são informadas
- As informações ficam espalhadas (redes sociais, grupos de WhatsApp, etc.)

###  Funcionalidades desejadas

1. Receber **alertas em tempo real** sobre chuvas fortes e alagamentos
2. Visualizar no mapa as **áreas afetadas**
3. Poder **reportar alagamentos** (com foto/localização)
4. Ver **rotas alternativas seguras**
5. Receber notificações baseadas na **minha localização**
6. Ter um histórico ou previsão de risco (ex: regiões mais críticas)

---

##  Parte 2: Histórias de Usuário

1. Como cidadão, quero receber alertas em tempo real sobre chuvas fortes para me prevenir de riscos.

2. Como usuário, quero visualizar no mapa as áreas com alagamento para evitar essas regiões.

3. Como usuário, quero reportar alagamentos com foto e localização para ajudar outras pessoas.

4. Como motorista, quero receber sugestões de rotas alternativas para chegar ao meu destino com segurança.

5. Como usuário, quero receber notificações baseadas na minha localização para obter informações relevantes.

6. Como usuário, quero visualizar um histórico de áreas afetadas para entender regiões de risco.

---

##  Parte 3: Aplicação do método CARD

###  Capture 

- Alertas em tempo real
- Mapa com áreas afetadas
- Reporte de alagamentos
- Rotas alternativas
- Notificações por localização
- Histórico de risco

---

###  Approve

**Alta prioridade:**

- Alertas em tempo real
- Mapa com áreas afetadas
- Notificações por localização

**Média prioridade:**

- Reporte de alagamentos
- Rotas alternativas

**Baixa prioridade:**

- Histórico de áreas afetadas

---

###  Refine 

- Alertas devem ser enviados via notificação push
- O mapa deve destacar regiões com cores (ex: vermelho = alto risco)
- O reporte deve incluir foto + localização automática
- Rotas alternativas devem considerar áreas bloqueadas
- Notificações devem ser personalizadas por localização do usuário
- Histórico deve mostrar padrões de risco por região
