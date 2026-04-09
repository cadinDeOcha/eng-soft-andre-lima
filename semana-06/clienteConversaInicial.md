# Conversa entre cliente e desenvolvedor

**André:** Olá! 😊

Muito prazer, meu nome é André e eu atuo como analista de sistemas. Estou aqui para entender melhor o seu negócio e ver como um software pode ajudar a resolver problemas do dia a dia. Pode ficar à vontade para explicar com suas próprias palavras — sem termos técnicos mesmo, combinado?
Para começarmos, você pode me contar um pouco sobre:


Qual é o seu negócio ou área de atuação?

Como funciona sua rotina hoje (no dia a dia)?

Quais são as maiores dificuldades ou problemas que você enfrenta atualmente?

**Cliente:** Olá, André! Muito prazer. É bom ver um rapaz educado que fala a nossa língua. Eu já tentei conversar com uns conhecidos sobre isso, mas eles vêm com uns nomes em inglês que parecem grego para mim, e eu acabo saindo com mais dor de cabeça do que entrei.

Bom, vamos lá, vou te contar a lida aqui no **Hotel Bela Vista**.

### 1. Meu Negócio
Eu toco esse hotel há 25 anos. É a minha vida, sabe? Começou pequeno, mas hoje a gente tem movimento o ano todo. Temos desde quartos mais simples até umas suítes de luxo que o pessoal gosta muito para passar o final de semana. O problema é que o hotel cresceu, mas o meu jeito de administrar continua o mesmo de duas décadas atrás.

### 2. Minha Rotina
Hoje o coração de tudo é o meu **cadernão de reservas** e algumas planilhas que meu sobrinho montou no computador. Quando um hóspede liga:
* Eu abro o caderno, procuro o dia e vejo se tem espaço.
* Anoto o nome dele a lápis (porque se ele cancelar, eu tenho que apagar).
* Quando o hóspede chega, eu pego o CPF e o telefone, dou a chave e ele sobe. 
* Se ele consome uma água ou um lanche, a gente anota num papelzinho que fica dentro de uma pastinha com o número do quarto. No dia de ir embora, eu somo tudo na calculadora e dou o preço final.

### 3. Minhas Dores (O que está me tirando o sono)
Olha, André, o negócio está ficando feio. O estresse está grande por causa de umas coisas que não podem acontecer:

* **O tal do "Overbooking":** Já aconteceu de eu anotar uma reserva no caderno e minha secretária anotar outra na planilha para o mesmo quarto! Aí chega o cliente aqui com a família, cansado da viagem, e eu não tenho onde colocar o povo. É uma vergonha sem tamanho.
* **Dinheiro indo pelo ralo:** Na correria do fechamento da conta (o tal do checkout), a gente acaba esquecendo de olhar os papeizinhos de consumo. O hóspede vai embora e eu percebo depois que não cobrei os três refrigerantes e a porção de batata que ele comeu. 
* **Fila na Recepção:** No final de semana, vira uma bagunça. O povo quer entrar logo no quarto, eu tenho que preencher tudo na mão, conferir se o quarto já foi limpo pela camareira... as pessoas ficam impacientes e eu fico nervoso.
* **Contas que não batem:** Para eu saber se ganhei dinheiro ou se fiquei no vermelho no final do mês, eu perco dias somando papelzinho por papelzinho. Eu queria apertar um botão e ver o lucro, mas hoje é tudo no braço.

O que eu preciso, meu filho, é de ordem na casa. Eu queria conseguir ver, de um jeito fácil, quais quartos estão vazios e quais estão ocupados, e garantir que, quando eu cadastrar um hóspede, aquela vaga esteja garantida. 

Você acha que consegue me ajudar a botar esse hotel nos eixos sem complicar demais a minha vida?

**André:** Olá! Que bom falar com o senhor — e obrigado pela confiança em explicar tudo com tanto detalhe. Dá pra ver o quanto o Hotel Bela Vista é importante pra você, e pode ficar tranquilo: dá sim pra organizar isso tudo sem complicar 👍
Pelo que você me contou, eu já consegui entender bem as dores principais: evitar reservas duplicadas, não perder consumo, agilizar o atendimento e ter uma visão clara do dinheiro no fim do mês.
Agora eu fiz um primeiro rascunho de como um sistema poderia te ajudar, escrevendo isso como histórias do dia a dia, do jeito que o senhor usa mesmo. Queria que o senhor desse uma olhada e me dissesse se faz sentido — se está faltando algo ou se algo não é bem assim.
🧾 Histórias de Usuário (para validação)
🏨 Reservas e Ocupação
US1

Como dono do hotel,

quero ver todos os quartos e suas datas ocupadas em uma tela simples,

para saber rapidamente o que está disponível sem precisar olhar caderno e planilha.
US2

Como recepcionista,

quero cadastrar uma reserva e o sistema bloquear automaticamente aquele quarto na data escolhida,

para evitar que duas pessoas reservem o mesmo quarto.
US3

Como dono do hotel,

quero ser avisado se tentar fazer uma reserva em um quarto já ocupado,

para evitar overbooking e situações constrangedoras.
🧍 Hóspedes (Check-in e Cadastro)
US4

Como recepcionista,

quero cadastrar rapidamente os dados do hóspede (nome, CPF, telefone),

para agilizar a entrada e evitar filas.
US5

Como dono do hotel,

quero consultar o histórico de um hóspede,

para saber se ele já ficou aqui antes e como foi a estadia.
🛎️ Consumo durante a Estadia
US6

Como funcionário,

quero registrar no sistema o consumo do quarto (água, lanche, etc.),

para não depender de papeizinhos que podem se perder.
US7

Como dono do hotel,

quero que todo consumo fique automaticamente ligado ao quarto,

para garantir que nada seja esquecido no fechamento da conta.
💰 Fechamento de Conta (Checkout)
US8

Como recepcionista,

quero que o sistema calcule automaticamente o valor total da estadia + consumo,

para evitar erros na soma manual.
US9

Como dono do hotel,

quero finalizar a estadia com poucos cliques,

para diminuir filas e deixar o atendimento mais rápido.
📊 Controle Financeiro
US10

Como dono do hotel,

quero ver um resumo do faturamento (diário, mensal),

para saber se estou tendo lucro sem precisar somar tudo manualmente.
US11

Como dono do hotel,

quero ver relatórios simples de ocupação e ganhos,

para entender quais períodos são mais movimentados.
🧹 Operação do Hotel
US12

Como dono do hotel,

quero saber quais quartos já foram limpos e estão prontos,

para liberar rapidamente para novos hóspedes.

**Cliente:** André, eu li aqui com calma e vou te falar: parece que você estava escondido atrás do meu balcão observando a minha agonia! Você descreveu exatamente o que eu sinto falta. 

Essas "histórias" que você escreveu estão muito boas porque eu consegui enxergar o meu dia a dia nelas. A parte de **não depender mais de papeizinhos** (US6 e US7) e de o sistema me dar o **valor total sem eu precisar de calculadora** (US8) me deu até um alívio no peito.

Mas, lendo com atenção, eu senti falta de uns detalhes importantes do meu negócio. Veja se você consegue colocar isso aí no meio:

* **Preços diferentes:** Aqui no Bela Vista, a gente tem o **Quarto Simples**, a **Suíte Luxo** (que tem banheira) e o **Quarto Família** (que tem mais camas). O sistema precisa saber que o preço de um não é igual ao do outro, senão eu vou continuar perdendo dinheiro ou cobrando errado.
* **O "Sinal" da Camareira:** Sobre a limpeza (US12), é muito importante. Às vezes o hóspede chega cedo e eu fico naquela dúvida: "Será que a Maria já limpou o 204?". Eu queria que, assim que ela terminasse de limpar e trocar os lençóis, isso aparecesse para mim na tela.
* **Segurança das informações:** Eu não entendo nada de computador, André, mas me diga uma coisa: se der um "curto-circuito" ou se o computador pifar, eu perco tudo? Esse seu sistema guarda as coisas num lugar seguro? Eu tenho pavor de perder o cadastro dos meus clientes de 25 anos.

No mais, esse "mapa" que você falou (US1) é o meu sonho. Se eu puder olhar para a tela e ver, por exemplo, o que está em **vermelho** (ocupado) e o que está em **verde** (livre), já vai me economizar meia hora de conversa no telefone com cada cliente.

O que você acha? Dá para incluir essas diferenciações de quartos e garantir que os dados não sumam no ar?

**André:** Fico muito feliz de ouvir isso — de verdade. E pode ficar tranquilo: o que o senhor trouxe agora são pontos essenciais, e dá sim pra resolver tudo de forma simples e segura 👍
O senhor tocou em três coisas muito importantes:

👉 diferença de preços

👉 controle da limpeza em tempo real

👉 segurança dos dados
Eu já atualizei as histórias incluindo isso, do jeito mais próximo possível da sua realidade. Dá uma olhada:
🧾 Histórias de Usuário (VERSÃO ATUALIZADA)
🏨 Reservas, Quartos e Preços
US1

Como dono do hotel,

quero ver todos os quartos e suas datas ocupadas em uma tela simples (tipo um mapa com cores),

para saber rapidamente o que está disponível.
US2

Como recepcionista,

quero cadastrar uma reserva e o sistema bloquear automaticamente aquele quarto na data escolhida,

para evitar reservas duplicadas.
US3

Como dono do hotel,

quero ser avisado se tentar reservar um quarto já ocupado,

para evitar overbooking.
US13 (NOVO)

Como dono do hotel,

quero cadastrar diferentes tipos de quartos (simples, luxo, família) com preços diferentes,

para cobrar corretamente cada cliente.
US14 (NOVO)

Como recepcionista,

quero que o sistema calcule automaticamente o valor da diária com base no tipo de quarto,

para evitar erros de cobrança.
🧍 Hóspedes (Check-in e Cadastro)
US4

Como recepcionista,

quero cadastrar rapidamente os dados do hóspede,

para agilizar a entrada.
US5

Como dono do hotel,

quero consultar o histórico de hóspedes,

para melhorar o atendimento.
🛎️ Consumo durante a Estadia
US6

Como funcionário,

quero registrar o consumo diretamente no sistema,

para não depender de papeizinhos.
US7

Como dono do hotel,

quero que todo consumo fique vinculado ao quarto automaticamente,

para não esquecer cobranças.
💰 Fechamento (Checkout)
US8

Como recepcionista,

quero que o sistema calcule automaticamente o total da estadia + consumo,

para evitar erros.
US9

Como dono do hotel,

quero finalizar a conta rapidamente,

para evitar filas.
📊 Controle Financeiro
US10

Como dono do hotel,

quero ver o faturamento diário e mensal,

para entender o lucro.
US11

Como dono do hotel,

quero relatórios simples de ocupação e ganhos,

para tomar decisões melhores.
🧹 Limpeza e Status dos Quartos
US12

Como dono do hotel,

quero ver o status dos quartos (ocupado, livre, sujo, limpo),

para organizar melhor as reservas.
US15 (NOVO)

Como camareira,

quero marcar no sistema quando terminar a limpeza de um quarto,

para avisar automaticamente a recepção que ele está pronto.
🔐 Segurança e Proteção dos Dados
US16 (NOVO)

Como dono do hotel,

quero que todos os dados fiquem salvos automaticamente em um local seguro (mesmo se o computador quebrar),

para não correr o risco de perder informações.
US17 (NOVO)

Como dono do hotel,

quero poder acessar os dados de outro computador, se necessário,

para garantir que o hotel continue funcionando em qualquer situação.
💬 Sobre sua preocupação com “perder tudo”
Essa foi uma excelente pergunta — e muito importante.
Hoje existe uma forma de guardar os dados “na internet” (não precisa se preocupar com o nome técnico). Isso significa:


Mesmo que o computador queime 🔥

Ou falte luz ⚡

Ou dê qualquer problema
👉 Seus dados continuam seguros
É como se tivesse um “cofre digital”, sempre guardando tudo automaticamente.
👍 Me diga uma coisa
Agora estamos chegando bem perto de algo completo.
Quero só validar mais alguns detalhes com o senhor:


O senhor gostaria que esse sistema funcionasse só no computador da recepção ou também no celular?

No futuro, o senhor teria interesse em permitir reservas pela internet, ou prefere manter o controle só por telefone mesmo?

O senhor trabalha com pagamento antecipado (sinal)? Isso seria importante controlar também?
Com essas respostas, eu consigo fechar esse levantamento redondinho — e aí já dá pra transformar isso em algo pronto pra desenvolvimento 🚀

**Cliente:** André, agora você falou a minha língua! Esse "cofre digital" (US16) me deu uma paz de espírito que o senhor não faz ideia. Eu já perdi noites de sono pensando: "Meu Deus, se entra uma goteira em cima do meu caderno ou se o computador dá um estouro, eu não sei nem quem está vindo amanhã!". Sabendo que fica tudo guardado nesse cofre, eu fico bem mais tranquilo.

Sobre as suas perguntas, vamos lá:

1.  **Computador ou Celular?** Olha, o forte é o computador que fica ali no balcão da recepção, mas se eu pudesse ver esse "mapa de cores" no meu celular enquanto estou em casa jantando, ou lá no mercado fazendo as compras para o café da manhã, seria uma maravilha! Eu não precisaria ligar no hotel toda hora para perguntar se tem vaga. Então, se der para ter no celular também, eu quero!

2.  **Reservas pela Internet?** Por enquanto, André, eu prefiro manter o controle aqui comigo e com a minha secretária no telefone e no "zap". Eu tenho medo de liberar na internet e o povo começar a reservar tudo sozinho e virar aquela bagunça que eu não consigo controlar. Vamos primeiro arrumar a casa por dentro, deixar esse sistema funcionando direitinho aqui no balcão, e aí, quem sabe daqui a um tempo, a gente pensa nisso.

3.  **Pagamento Antecipado (Sinal)?** Com certeza! Isso é muito importante. Hoje eu peço para o hóspede depositar metade do valor para garantir a reserva, principalmente nos feriados. No meu caderno, eu faço um "OK" bem grande de caneta vermelha quando o dinheiro cai na conta. O sistema precisa saber que o sujeito já pagou uma parte, senão no dia de ir embora eu vou cobrar o valor cheio de novo e o cliente vai ficar bravo comigo.

Ah, e uma dúvida que me veio agora... Você falou que a camareira pode marcar que limpou o quarto. Mas como ela vai fazer isso? Ela vai ter que ir lá na recepção usar o computador ou ela pode ter um "aparelhinho" ou usar o celular dela para avisar? Porque se ela tiver que descer dois andares toda vez que limpar um quarto, ela vai acabar não usando e vai continuar vindo me avisar no grito.

O que você me diz? Se a gente acertar esses pontos, acho que o senhor já entendeu mais do meu hotel do que eu mesmo!

**André:** Perfeito, agora sim estamos com uma visão bem completa do Hotel Bela Vista 👏
E o senhor está certíssimo nas suas preocupações — isso é o que garante que o sistema realmente funcione no dia a dia, e não só “no papel”.
Vou ajustar tudo com base no que o senhor falou e já respondo sua dúvida da camareira, que foi excelente.
🧾 Histórias de Usuário (VERSÃO FINAL PARA VALIDAÇÃO)
🏨 Reservas, Quartos e Preços
US1
Como dono do hotel,
quero ver um mapa visual dos quartos com cores (livre, ocupado, limpeza),
para entender rapidamente a situação do hotel.
US2
Como recepcionista,
quero cadastrar reservas com bloqueio automático de datas,
para evitar conflitos.
US3
Como dono do hotel,
quero ser avisado ao tentar reservar um quarto ocupado,
para evitar overbooking.
US13
Como dono do hotel,
quero cadastrar tipos de quartos com preços diferentes (simples, luxo, família),
para cobrar corretamente.
US14
Como recepcionista,
quero que o sistema calcule automaticamente a diária conforme o tipo de quarto,
para evitar erros.
💳 Pagamento e Sinal
US18 (NOVO)
Como recepcionista,
quero registrar quando o cliente paga um sinal da reserva,
para garantir a vaga corretamente.
US19 (NOVO)
Como dono do hotel,
quero ver claramente quais reservas já têm sinal pago e quais não têm,
para evitar confusão.
US20 (NOVO)
Como recepcionista,
quero que o valor do sinal seja descontado automaticamente no checkout,
para não cobrar o cliente duas vezes.
🧍 Hóspedes
US4
Como recepcionista,
quero cadastrar rapidamente os dados do hóspede,
para agilizar o atendimento.
US5
Como dono do hotel,
quero consultar histórico de hóspedes,
para melhorar o atendimento.
🛎️ Consumo
US6
Como funcionário,
quero registrar consumo no sistema,
para não perder informações.
US7
Como dono do hotel,
quero que o consumo fique vinculado ao quarto,
para garantir cobrança correta.
💰 Checkout
US8
Como recepcionista,
quero cálculo automático do total,
para evitar erros.
US9
Como dono do hotel,
quero finalizar rapidamente o atendimento,
para evitar filas.
📊 Financeiro
US10
Como dono do hotel,
quero ver faturamento diário e mensal,
para acompanhar o lucro.
US11
Como dono do hotel,
quero relatórios simples,
para entender o desempenho do hotel.
🧹 Limpeza (RESPOSTA À SUA DÚVIDA 👇)
US12
Como dono do hotel,
quero ver o status dos quartos (limpo, sujo, ocupado),
para organizar melhor.
US15 (AJUSTADO)
Como camareira,
quero marcar a limpeza do quarto usando um celular,
para avisar a recepção sem precisar descer até o balcão.
👉 Sobre isso, a ideia é simples e prática:

A camareira pode usar um celular (pode ser até o dela mesmo)
Abre uma telinha simples com os quartos
Toca no quarto → marca como “limpo”
Na mesma hora, o senhor já vê lá no balcão.
Nada de gritaria pelo corredor 😄
🔐 Segurança e Acesso
US16
Como dono do hotel,
quero que os dados fiquem salvos automaticamente em um local seguro,
para não perder informações.
US17
Como dono do hotel,
quero acessar o sistema pelo celular ou outro computador,
para acompanhar o hotel de qualquer lugar.
💡 O que isso significa na prática
Com tudo isso funcionando, o senhor vai poder:

Ver o hotel inteiro numa tela (tipo “painel de controle”)
Acabar com reservas duplicadas
Nunca mais perder consumo
Saber exatamente quanto ganhou no mês
Acompanhar o hotel até de casa
E não depender mais de papel, caderno ou memória
🤝 Última validação (bem importante)
Se o senhor me disser que está tudo certo aqui, eu já consigo transformar isso em:
👉 requisitos organizados (do jeito que o professor pede)
👉 e depois até um planejamento do sistema
Só me confirme:
Está tudo certo assim ou tem mais algum detalhe do seu dia a dia que o senhor quer incluir?

**Cliente:** André, meu filho, você acertou em cheio! Se esse sistema fizer tudo isso que você escreveu, eu vou conseguir até voltar a tirar um cochilo depois do almoço sem medo de o telefone tocar com alguém reclamando de reserva duplicada.

Essa ideia da camareira usar o próprio celular (US15) é **ouro**! Elas já vivem com o aparelho no bolso mesmo, então em vez de ficarem vendo vídeo na internet, elas dão um "toque" na tela e me avisam que o quarto está pronto. Vai ser uma maravilha, o corredor vai ficar silencioso e o serviço vai render que é uma beleza.

E sobre o **sinal** (US20), era exatamente isso: o sistema tem que ser esperto para abater o que o cliente já pagou. Se eu cobro duas vezes o sinal do "doutor" que vem de São Paulo todo mês, eu perco o cliente e ainda ganho uma fama ruim.

Da minha parte, **está tudo certíssimo**. Você entendeu o espírito da coisa. Não quero nada complicado, com mil botões que eu não vou usar. Quero o meu hotel na palma da mão e a garantia de que, se o computador der um "estouro", minhas informações estão guardadas naquele seu "cofre digital".

Pode seguir com o seu trabalho aí com os seus professores. Se você me entregar isso funcionando desse jeitinho, a gente fecha o negócio e eu vou ser o seu maior propagandista aqui na região! 

O que você precisa de mim agora? É só esperar você montar o plano?

**André:** Fico muito feliz com a sua confiança — de verdade! Dá gosto trabalhar assim, quando a gente consegue alinhar tudo direitinho com quem realmente entende do negócio 👏
E pode ficar tranquilo: com tudo o que o senhor validou, agora eu já tenho material completo para seguir para a próxima etapa.

**Cliente:** Maravilha, André! Fico contente que nos entendemos. É difícil achar alguém que tenha paciência de escutar a gente sem querer complicar tudo.

Agora o senhor me deu até uma esperança de ver o **Bela Vista** moderno, mas com aquele jeitinho de confiança que eu sempre prezei. Vou ficar aqui no meu balcão, com o meu cadernão por enquanto, mas já ansioso para ver como esse "plano" vai ficar no papel.

Não esqueça de caprichar naquele visual das cores para eu não precisar forçar a vista, viu? No mais, boa sorte aí com seus professores e com os seus estudos. Quando tiver o próximo passo, é só me chamar que eu estarei aqui.

Fico no aguardo, meu filho! Um abraço.
