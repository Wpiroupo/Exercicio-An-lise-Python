# Análise de Internações no Sistema de Saúde Brasileiro
Os dados em anexo (case_internacao_SUS.xls) são referentes às internações que
ocorreram no país durante o período de dezembro de 2017 a julho de 2019, separados
por região e unidade de federação (Fonte: Ministério da Saúde - Sistema de Informações
Hospitalares do SUS (SIH/SUS)).


Acesse http://tabnet.datasus.gov.br/cgi/sih/sxdescr.htm para obter uma descrição
detalhada dos dados.


Desafios:

1. Tratamento dos dados

1.1. Muitas vezes, cerca de 70% do tempo de um projeto é despendido na coleta e
tratamento dos dados. Sabendo disso, leia o arquivo e o transforme de modo a
ter mais facilidade em analisar os dados. Lembre-se que essa etapa poderá te
dar bons insumos. Portanto, capriche!


2. Análise

2.1. Dados tratados, bora explorá-los? Faça uma boa EDA e não esqueça de anotar
todos os insights que você obter. Gráficos e informações sem uma boa
interpretação não valem, ok?

3. Modelagem

3.1. Agora que já tem certa intimidade com os dados, cite pelo menos 2 métodos
possíveis para estimar os dados para os meses faltantes. Tente não se complicar
aqui. Utilize os métodos mais simples e mais funcionais possíveis. Neste tópico,
é importante que argumente o porquê dos métodos recomendados.

3.2. Escolha um desses métodos e estime

a) o número de Internações

b) o Valor Total das internações nos períodos faltantes.

3.3. Crie um modelo que preveja 

a) as Internações

b) o número de Óbitos 

c) o Valor Médio de AIH pelos próximos 6 meses. Explique a escolha do modelo e
quais parâmetros utilizou para serem input no modelo.

4. Planejamento estratégico

4.1. Com base nos dados e nas suas análises, que tipo de estratégia você sugeriria
para diminuir o número de internações em hospitais do SUS? E para o Estado
de São Paulo? Quais especificidades deveriam ser levadas em conta?


# analises, insights:

O numero de aprovações de AIH seguem juntas com as internações

A taxa de mortalidade nas internações tem aumentado ao longo do tempo

Fazendo as descrições estatisticas, percebemos que do 75% ao maximo de internações temos um aumento muito maior se comparado com o valor médio de internação deste mesmo periodo

Numero de internações vem crescendo ao longo do tempo

Conseguimos rankear as regioes com maiores numeros e seus comportamentos, sendo elas do maior para o menor: Sudeste, Nordeste, Sul, Norte, Centro-Oeste. Fizemos o mesmo para os estados

Fizemos a correlação entre os dados para possiveis tomadas de decisões onde explico na parte das estratégias

porque dos metodos citados no item 3.1 e 3.2?

É um método simples e bastante eficiente quando nao tem muitos dados faltantes em sequencia, apenas prencher com o valor próximo da frente (que foi o utilizado), ou com uma média tende a ser bastante utilizado

modelagem requerida para predição dos 6 meses:

Foi utilizado o modelo ARIMA usando dois principais recursos:

1- autocorrelação

2- médias móveis

Estratégia para redução nos casos de internações geral:

Reduzir investimento no valor_servicos_hospitalares

Reduzir investimento no valor serviços profissionais

aumentar investimento no serviços hop compl federal

aumentar investimento no serviços hop compl gestor

aumentar investimento no Val serv prof - compl federal

aumentar investimento no Val serv prof - compl gestor

Para São Paulo:

Aumentar o Valor médio Valor médio das AIH aprovadas no período.

Aumentar o Valor médio das AIH aprovadas, computadas como internações, no período.

Dar mais orientações ao tempo de permanencia entre os dias de baixa e alta de internação, para um aumento

O que deve ser considerado?

Deve ser levado em conta onde os valores estão sendo investido no geral, e passar orientação para tentar aumentar o tempo médio de permanencia em internações em São Paulo

