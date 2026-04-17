# Validação de Requisitos de Software entre cliente e desenvolvedor 

**André:** Agora, preciso que verifique os requisitos do projeto (sendo RF para Requisitos Funcionais e RNF para Requisitos Não Funcionais) e me diga se concorda ou não, para validarmos e dar sequência no desenvolvimento.

RF1 – O sistema deve exibir um mapa visual dos quartos com indicação de status (livre, ocupado, sujo, limpo).

RF2 – O sistema deve permitir o cadastro de reservas informando datas e quarto.

RF3 – O sistema deve bloquear automaticamente um quarto ao realizar uma reserva.

RF4 – O sistema deve impedir reservas duplicadas para o mesmo quarto e período.

RF5 – O sistema deve emitir alerta ao tentar reservar um quarto já ocupado.

RF6 – O sistema deve permitir o cadastro de diferentes tipos de quartos (simples, luxo, família).

RF7 – O sistema deve associar preços diferentes para cada tipo de quarto.

RF8 – O sistema deve calcular automaticamente o valor da diária com base no tipo de quarto.

RF9 – O sistema deve permitir o cadastro de hóspedes com dados como nome, CPF e telefone.

RF10 – O sistema deve permitir a consulta ao histórico de hóspedes.

RF11 – O sistema deve permitir o registro de consumos (produtos/serviços) associados a um quarto.

RF12 – O sistema deve vincular automaticamente os consumos à conta do quarto.

RF13 – O sistema deve calcular automaticamente o valor total da estadia (diárias + consumo).

RF14 – O sistema deve permitir o fechamento da conta (checkout) de forma rápida.

RF15 – O sistema deve permitir o registro de pagamento antecipado (sinal).

RF16 – O sistema deve identificar visualmente quais reservas possuem sinal pago.

RF17 – O sistema deve descontar automaticamente o valor do sinal no fechamento da conta.

RF18 – O sistema deve permitir que a camareira atualize o status do quarto (ex: limpo).

RF19 – O sistema deve disponibilizar acesso para atualização de status via dispositivo móvel (celular).

RF20 – O sistema deve apresentar relatórios de faturamento diário.

RF21 – O sistema deve apresentar relatórios de faturamento mensal.

RF22 – O sistema deve apresentar relatórios de ocupação dos quartos.

RNF1 – O sistema deve possuir interface simples e de fácil uso, adequada a usuários não técnicos.

RNF2 – O sistema deve estar disponível tanto em computador quanto em dispositivos móveis (celular).

RNF3 – O sistema deve armazenar os dados em ambiente seguro (backup automático).

RNF4 – O sistema deve garantir que os dados não sejam perdidos em caso de falha do computador local.

RNF5 – O sistema deve permitir acesso remoto aos dados (via internet).

RNF6 – O sistema deve apresentar atualização em tempo real das informações (ex: status de quartos).

RNF7 – O sistema deve garantir confiabilidade nas operações para evitar inconsistências (ex: overbooking).

**Cliente:** Ôpa, André! Você trouxe a lista completa, hein? Li cada ponto aqui com a atenção de quem está conferindo o fechamento do caixa.

Vou te falar, meu filho, essa lista de "RF" e "RNF" (que eu imagino que sejam as **Regras de Funcionamento** e as **Regras de Segurança**, certo?) está muito bem feita. Você traduziu direitinho tudo o que a gente conversou no balcão.

**Minha validação ponto a ponto:**

* **Sobre as Funções (RFs):** Está tudo aí. O que eu mais gostei foi ver que você não esqueceu do **desconto do sinal (RF17)** e de separar os **tipos de quarto (RF6 e RF7)**. Se o sistema fizer esse cálculo automático (RF13), eu já economizo metade do meu dia. E o **RF19** sobre o celular para a camareira é o que vai acabar com a gritaria no corredor, então está aprovadíssimo!
* **Sobre o "Como" o sistema funciona (RNFs):**
    * O **RNF1** é o mais importante para mim: **tem que ser simples**. Se tiver muito botão difícil, eu vou acabar voltando para o caderno, e ninguém quer isso.
    * O **RNF3 e RNF4** são o meu "seguro de vida". Saber que os dados estão protegidos contra pane no computador me deixa dormir tranquilo.
    * E o **RNF6** de ser em "tempo real" é ótimo, porque se a Maria limpar o quarto lá no terceiro andar, eu já quero ver o "verde" brilhando aqui na minha tela na mesma hora.

---

**Só um detalhe para a gente não se perder:**
Ali no **RF15 e RF16**, quando o senhor fala de registrar o sinal, só garanta que seja bem fácil de ver **quem já pagou e quem ainda deve o sinal**. Às vezes o sujeito reserva para daqui a um mês e esquece de depositar. Se o sistema me mostrar um alerta de "Sinal Pendente", vai ser uma beleza para eu cobrar o cliente antes de ele chegar.

**Conclusão:**
Pode dar o "carimbo" de aprovado! Eu concordo com todos esses pontos. Se você seguir essa receita aí, o **Hotel Bela Vista** vai ficar uma maravilha de organização.

O que vem agora? Você já vai começar a "construir" o sistema ou ainda tem mais papelada para a gente validar?
