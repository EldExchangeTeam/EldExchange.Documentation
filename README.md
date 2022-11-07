# Eld Exchange 

Está é uma atividade de treinamento apresentada a estagiária do instituto de pesquisa eldorado de Brasília com o objetivo de ensinar na prática elementos de desenvolvimento de software para Web. Busca se realizar um processo completo desde a análise do projeto, passando pelo planejamento de arquitetura e modelagem, escrita de histórias, e finalmente o desenvolvimento do software propriamente dito. Ao final temos como objetivo desenvolver um sistema que possa servir de base de estudos e de exemplo de código. 

Temos como objetivo nesse estudo produzir um MVP (produto mínimo viável) de um sistema de agência de de câmbio (Exchange). 

## Horário

Quartas e Sextas de 13h até as 17h

## Ferramentas

* [git](https://git-scm.com/)
* [Github](https://github.com/)
* [Git-flow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
* [Github Actions](https://docs.github.com/en/actions)
* [DotNet 6](https://dotnet.microsoft.com)
* [Visual Studio](https://visualstudio.microsoft.com)
* [Visual Studio code](https://code.visualstudio.com/)
* [Astah](https://astah.net/)
* [BrModel](https://www.brmodeloweb.com/lang/pt-br/index.html)
* [Versionize](https://github.com/versionize/versionize)
* [conventional commit messages](https://conventionalcommits.org/)

## links Uteis 

* [Confluence](https://flpinheiro.atlassian.net/wiki/spaces/ELDEXCHANG/overview)
* [Jira](https://flpinheiro.atlassian.net/jira/software/projects/EEX/pages)
* [Backend](https://github.com/EldExchange/Backend.git)

## O Problema 

Você e sua equipe de desenvolvedores foram contratados por uma empresa pra fazer o sistema administrativo de uma empresa de câmbio. Será necessário desenvolver o sistema, com artefatos de modelagem do sistema e controle do backlog do desenvolvimento via sistema jira. Espera se que pelo menos a primeira versão seja entregue em no máximo 4 sprints ( 8 semanas), ou seja, até o início do ano. Todo o software deve ser escrito em inglês, incluindo documentação, artefatos, backlog e demais atividades executadas. Todos os artefatos devem ser adicionados em repositórios específicos do GitHub, a fim de buscar a organização e possibilitar a separação das estruturas do projeto. Os desenvolvedores devem utilizar gitflow como workflow de implementação de código, sendo vedado o push direto na master e na dev. 

A empresa de câmbio possuí diversas agências com cada agência possuindo um endereço físico e podendo ter vários telefones fixos ou celulares, a agência também possuí um caixa único que deve registrar todas as transações de entrada e saída de dinheiro do sistema contabilizando cada nota bancária de forma individual, pois se deseja saber quanto de cada nota existe disponível em cada agência a qualquer momento.

As agências trabalham com sistemas financeiros de diversas partes do mundo, em especial Real brasileiro, Dólar Americano, Euro, libra esterlina e yen japonês e demais moedas podem ser adicionadas posteriormente ao sistema. 

No processo de criação de uma nova agência, ela deve receber como saldo inicial 1000 unidades de cada unidade (moda e moeda) de cada sistema financeiro principal, destacado no parágrafo anterior, não devendo receber nenhum centavo de novos sistemas financeiros que venham a ser adicionados posteriormente. 

Deve existir um sistema de expurgo e aporte de saldos de (moedas e notas) para as agências, retirando se o excesso de valores ou adicionando valores adicionais necessário.

Cada sistema financeiro deve ter pelo menos: nome, símbolo da nota, símbolo da moeda, listagem com valores de notas e moedas existentes, código internacional do sistema financeiro que deve ser único, entre outras propriedades. 

Ao um usuário efetuar uma transação de um sistema financeiro para outro deve se calcular automaticamente os valores de conversão, subtrair as taxas de imposto e o lucro da empresa retornando ao usuário o valor devido no sistema financeiro requisitado com a menor quantidade de notas e moedas possível. Caso a agência não tenha saldo suficiente pra efetuar a operação a transação deve ser cancelada e uma notificação de falta de fundos deve ser levantada. 

Cada transação deve ser registrada em tabela a parte, para posterior auditoria, anotando o valor inicial pago pelo usuário, o valor devolvido, o imposto pago, o lucro da empresa, data e hora da transação, documento de identificação do usuário (número e tipo do documento), identificador da agência, valor de conversão utilizado, e demais informação pertinentes ao processo. 

Deve ser implementado sistema de testes unitário para se testar as principais funcionalidades do sistema. 

O sistema será todo desenvolvido em dotnet 6 LTS (versão atual mais nova), devendo ser um sistema RESTFull api, o frontend poderá ser desenvolvido em momento posterior por outra equipe, em outra atividade. 

## referência

* [Começando com .NET Core, com Arquitetura em Camadas](https://alexalvess.medium.com/criando-uma-api-em-net-core-baseado-na-arquitetura-ddd-2c6a409c686)

* [Cross-cutting concern](https://en.m.wikipedia.org/wiki/Cross-cutting_concern)

* [Clear Cross-Cutting Concerns with Aspect Oriented Programming in .NET](https://visualstudiomagazine.com/articles/2011/05/12/wccsp_aspect-oriented-programming.aspx?m=1)

* [Aspect-Oriented Programming : Aspect-Oriented Programming with the RealProxy Class](https://learn.microsoft.com/en-us/archive/msdn-magazine/2014/february/aspect-oriented-programming-aspect-oriented-programming-with-the-realproxy-class)

* [Full Guide on How to Build an MVP](
https://orangesoft.co/blog/how-to-build-mvp)
