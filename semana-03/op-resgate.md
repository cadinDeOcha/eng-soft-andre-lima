# Missão Crítica: Operação Resgate

## Introdução

A Chaos-IT, uma software house brasileira, enfrenta sérios problemas devido à falha de seu último projeto de drones para entregas, resultado da ignorância de riscos técnicos e da ausência de processos padronizados. Este documento apresenta uma análise e soluções baseadas no Modelo Espiral de Boehm e no CMMI para auxiliar a empresa a resgatar seus projetos e melhorar sua maturidade em engenharia de software.

---

# Parte 1: O Labirinto de Boehm

## Análise de Riscos no Modelo Espiral

O Modelo Espiral, proposto por Barry Boehm, é um modelo de processo de desenvolvimento de software iterativo e baseado em risco. Diferente de modelos sequenciais, ele incorpora a análise e mitigação de riscos em cada uma de suas iterações (voltas da espiral). Essa característica é fundamental para projetos complexos e inovadores, como o sistema de controle de drones da Chaos-IT.

Em cada volta da espiral, a **Análise de Riscos** é uma atividade central que ocorre no segundo quadrante do ciclo. Se a Chaos-IT tivesse aplicado o Modelo Espiral, a análise de riscos em cada iteração teria evitado a queda dos drones da seguinte forma:

1.  **Identificação Proativa de Riscos:** Em vez de ignorar riscos técnicos, o Modelo Espiral forçaria a equipe a identificar e analisar potenciais problemas (técnicos, de cronograma, de custo, operacionais) desde as fases iniciais do projeto. Por exemplo, riscos relacionados à integração de hardware e software dos drones, à segurança do voo, à autonomia da bateria, ou à complexidade do software de IA subaquática seriam levantados. [1]
2.  **Mitigação e Resolução de Riscos:** Após a identificação, seriam desenvolvidas estratégias para mitigar ou resolver esses riscos. Isso poderia incluir a realização de protótipos para testar tecnologias críticas, a pesquisa de alternativas, a contratação de especialistas, ou a redefinição de requisitos. A falha do projeto de drones da Chaos-IT foi atribuída à ignorância de riscos técnicos e falta de processos padronizados. O Modelo Espiral impõe um processo estruturado para lidar com riscos, o que teria evitado essa negligência. [2]
3.  **Feedback Contínuo e Adaptação:** Cada iteração do Modelo Espiral gera um protótipo ou uma versão funcional do sistema, que é avaliada pelos stakeholders. Esse feedback permite que o projeto se adapte a novas informações e riscos emergentes, ajustando o planejamento para as próximas fases. A falta de processos padronizados na Chaos-IT indica uma ausência de mecanismos de feedback e adaptação, o que o Modelo Espiral teria corrigido. [3]
4.  **Redução da Incerteza:** Ao abordar os riscos de forma incremental, o Modelo Espiral reduz a incerteza do projeto ao longo do tempo. Os riscos mais críticos são tratados primeiro, garantindo que as decisões importantes sejam tomadas com base em informações mais sólidas. Isso é crucial para um projeto inovador como o de IA subaquática, onde muitos aspectos podem ser desconhecidos no início. [4]

Em resumo, a aplicação da Análise de Riscos em cada volta da espiral teria permitido à Chaos-IT identificar, analisar e mitigar os riscos técnicos e de processo de forma contínua, evitando a falha catastrófica do projeto de drones.

## Ciclo Espiral para o Projeto de Drones de IA Subaquática

Considerando o projeto de IA subaquática da Chaos-IT, um ciclo específico do Modelo Espiral poderia ser detalhado nos quatro quadrantes da seguinte forma:

### Quadrante 1: Determinação de Objetivos, Alternativas e Restrições

*   **Objetivos:** Definir claramente os objetivos da iteração atual. Por exemplo, desenvolver um protótipo funcional do sistema de navegação autônoma subaquática para os drones, com capacidade de detecção de obstáculos básicos. Estabelecer métricas de desempenho para o protótipo (e.g., precisão da navegação, tempo de resposta da detecção).
*   **Alternativas:** Identificar diferentes abordagens para alcançar os objetivos. Isso pode incluir a escolha de algoritmos de IA para navegação, sensores subaquáticos específicos, ou plataformas de hardware para os drones. Avaliar a viabilidade técnica e o custo de cada alternativa.
*   **Restrições:** Listar as restrições do projeto, como orçamento disponível para a iteração, prazo de entrega do protótipo, recursos humanos, e requisitos regulatórios para operação de drones subaquáticos.

### Quadrante 2: Avaliação de Alternativas; Identificação e Resolução de Riscos

*   **Identificação de Riscos:** Realizar uma análise aprofundada dos riscos associados às alternativas e objetivos definidos. Exemplos de riscos para este projeto:
    *   **Técnicos:** Dificuldade na integração de sensores subaquáticos com o sistema de IA; desempenho insatisfatório dos algoritmos de navegação em ambientes aquáticos complexos; falha de comunicação subaquática.
    *   **De Cronograma:** Atrasos na aquisição de componentes especializados; tempo de desenvolvimento da IA maior que o estimado.
    *   **De Custo:** Superar o orçamento devido a imprevistos no desenvolvimento ou na compra de hardware.
    *   **Operacionais:** Dificuldade na manutenção dos drones subaquáticos; problemas de segurança na operação.
*   **Análise de Riscos:** Avaliar a probabilidade e o impacto de cada risco identificado. Priorizar os riscos mais críticos.
*   **Resolução de Riscos:** Desenvolver planos de mitigação para os riscos prioritários. Por exemplo, para o risco de integração de sensores, pode-se planejar a criação de um protótipo de baixo custo focado apenas na integração e teste dos sensores. Para riscos de desempenho da IA, pode-se realizar simulações extensivas antes da implementação física.

### Quadrante 3: Desenvolvimento e Teste

*   **Engenharia:** Com base nas decisões tomadas na fase de análise de riscos, desenvolver o protótipo ou a parte do sistema planejada para esta iteração. Isso incluiria a codificação dos algoritmos de IA, a montagem dos componentes do drone, e a integração do software com o hardware.
*   **Verificação e Validação:** Realizar testes rigorosos no protótipo. Testes unitários, de integração e de sistema seriam aplicados para garantir que os objetivos da iteração foram alcançados e que os riscos mitigados foram efetivamente controlados. Para o projeto de drones, isso envolveria testes em tanques de água controlados e, posteriormente, em ambientes subaquáticos reais, se o risco for baixo.

### Quadrante 4: Planejamento da Próxima Fase

*   **Avaliação do Ciclo:** Avaliar os resultados da iteração atual, comparando o protótipo com os objetivos definidos. Coletar feedback dos stakeholders e da equipe de desenvolvimento.
*   **Revisão do Plano:** Com base na avaliação e nos riscos remanescentes ou recém-identificados, revisar o plano geral do projeto. Decidir se o projeto deve continuar, ser modificado, ou ser abortado. Definir os objetivos para a próxima iteração da espiral, que pode focar em adicionar novas funcionalidades, melhorar o desempenho, ou abordar outros riscos.

Este ciclo se repetiria, com cada volta da espiral construindo sobre a anterior, adicionando funcionalidades e reduzindo riscos progressivamente, até que o sistema final de drones de IA subaquática fosse entregue com sucesso.

---

# Parte 2: O Diagnóstico CMMI

A Chaos-IT apresenta a seguinte descrição de seu processo de desenvolvimento de software:

> "Na Chaos-IT, cada desenvolvedor trabalha do seu jeito. Não há registro de erros passados, os prazos são 'chutados' e o sucesso depende exclusivamente do esforço heróico de alguns devs que fazem hora extra."

Com base nesta descrição, podemos diagnosticar o Nível de Maturidade CMMI (Capability Maturity Model Integration) da Chaos-IT.

## Nível de Maturidade CMMI Atual da Chaos-IT

A descrição fornecida se encaixa perfeitamente no **Nível 1 – Inicial** do CMMI [5] [6]. As características que sustentam essa conclusão são:

*   **Processos Ad-hoc e Caóticos:** A frase "cada desenvolvedor trabalha do seu jeito" indica a ausência de processos padronizados e documentados. As atividades são realizadas de forma improvisada e dependem do conhecimento individual, não da organização.
*   **Falta de Registro de Erros:** "Não há registro de erros passados" demonstra a ausência de um processo de gerenciamento de defeitos e de uma cultura de aprendizado com as falhas. Isso impede a melhoria contínua e a prevenção de problemas futuros.
*   **Prazos "Chutados":** A estimativa de prazos de forma arbitrária ("prazos são 'chutados'") revela a falta de um processo de planejamento e estimativa formal. Isso leva a atrasos, estouros de orçamento e baixa previsibilidade.
*   **Dependência de Esforço Heróico:** "o sucesso depende exclusivamente do esforço heróico de alguns devs que fazem hora extra" é um sintoma clássico do Nível 1. A organização não possui processos robustos que garantam o sucesso do projeto, dependendo de indivíduos para "apagar incêndios" e compensar as deficiências do processo.

Neste nível, o ambiente de desenvolvimento é imprevisível, e o sucesso dos projetos é mais uma questão de sorte ou da capacidade individual de alguns membros da equipe do que de um processo bem definido e controlado.

## O que falta para chegar ao Nível 2 – Gerenciado

Para a Chaos-IT avançar do Nível 1 (Inicial) para o **Nível 2 – Gerenciado** do CMMI, ela precisa estabelecer processos básicos de gerenciamento de projetos. O Nível 2 foca em garantir que os projetos sejam planejados, executados, medidos e controlados [7]. As principais áreas que a Chaos-IT precisa desenvolver incluem:

1.  **Gerenciamento de Requisitos:** Estabelecer um processo para coletar, analisar, documentar e gerenciar os requisitos do projeto. Isso garante que todos os envolvidos tenham um entendimento comum do que precisa ser construído.
2.  **Planejamento de Projeto:** Desenvolver processos formais para estimar o tamanho, custo e cronograma do projeto. Isso inclui a criação de planos de projeto detalhados, que são revisados e aprovados. A prática de "chutar" prazos deve ser substituída por técnicas de estimativa baseadas em dados históricos e metodologias reconhecidas.
3.  **Monitoramento e Controle de Projeto:** Implementar mecanismos para acompanhar o progresso do projeto em relação ao plano. Isso envolve a coleta de dados sobre o desempenho, a identificação de desvios e a tomada de ações corretivas. Reuniões de acompanhamento regulares e relatórios de status são essenciais.
4.  **Gerenciamento de Configuração:** Estabelecer um sistema para identificar, controlar e rastrear as versões dos produtos de trabalho (código-fonte, documentação, etc.). Isso evita problemas de integração e garante a integridade do projeto.
5.  **Garantia da Qualidade do Processo e Produto:** Definir e implementar atividades para garantir que os processos estão sendo seguidos e que os produtos de trabalho atendem aos padrões de qualidade. Isso pode incluir revisões de código, testes e auditorias de processo.
6.  **Gerenciamento de Acordos com Fornecedores:** Se a Chaos-IT utiliza fornecedores externos, precisa estabelecer processos para gerenciar esses acordos, garantindo que os produtos e serviços entregues atendam aos requisitos.

Ao implementar essas práticas, a Chaos-IT começará a ter projetos mais previsíveis e controlados, reduzindo a dependência do "esforço heróico" e construindo uma base sólida para a melhoria contínua de seus processos de desenvolvimento de software.

---

## Referências

[1] Sommerville, I. (2011). *Engenharia de Software*. 9ª Edição. Pearson Education do Brasil. (Referência genérica, pois o capítulo específico não foi fornecido, mas o livro é a fonte)
[2] Boehm, B. W. (1988). A spiral model of software development and enhancement. *Computer*, 21(5), 61-72.
[3] Pressman, R. S. (2010). *Engenharia de Software: Uma Abordagem Profissional*. 7ª Edição. McGraw-Hill.
[4] O Modelo em Espiral de Boehm. (s.d.). *Medium*. Disponível em: [https://medium.com/contexto-delimitado/o-modelo-em-espiral-de-boehm-ed1d85b7df](https://medium.com/contexto-delimitado/o-modelo-em-espiral-de-boehm-ed1d85b7df)
[5] Níveis de Maturidade do CMMI: Entenda!. (s.d.). *Promove Soluções*. Disponível em: [https://promovesolucoes.com/niveis-maturidade-cmmi/](https://promovesolucoes.com/niveis-maturidade-cmmi/)
[6] Maturidade no desenvolvimento de software: CMMI e MPS .... (s.d.). *DevMedia*. Disponível em: [https://www.devmedia.com.br/maturidade-no-desenvolvimento-de-software-cmmi-e-mps-br/27010](https://www.devmedia.com.br/maturidade-no-desenvolvimento-de-software-cmmi-e-mps-br/27010)
[7] CMMI (Integração de Modelos de Maturidade ...). (s.d.). *Microsoft Learn*. Disponível em: [https://learn.microsoft.com/pt-br/azure/devops/boards/work-items/guidance/cmmi/guidance-background-to-cmmi?view=azure-devops](https://learn.microsoft.com/pt-br/azure/devops/boards/work-items/guidance/cmmi/guidance-background-to-cmmi?view=azure-devops)
