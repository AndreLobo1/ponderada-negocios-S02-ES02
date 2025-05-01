# Atividade ponderada: Questão de Negócios Parte 1 - Tarefa de modelagem de processos

Este repositório abriga a atividade ponderada da Semana 2 do curso de Engenharia de Software do Inteli (Instituto de Tecnologia e Liderança), pertencente ao segundo módulo.

A atividade intitulada "Questão de Negócios – Parte 1: Tarefa de Modelagem de Processos" tem como objetivo aplicar os conceitos fundamentais de modelagem de processos de negócio utilizando a notação BPMN (Business Process Model and Notation).

## Desafio Apresentado

O desafio proposto foi o seguinte:

Elabore o modelo de processos a partir da descrição abaixo, utilizando a notação BPMN e a ferramenta ARIS.

Um cliente compra um ou mais produtos no site Mercado Livre. O pagamento é realizado por meio dos serviços PayPal ou Mercado Pago. Após a confirmação do pagamento, o vendedor realiza a postagem do produto, que é entregue ao cliente pelos Correios. Ao receber o produto, o cliente verifica se ele atende às expectativas. Caso esteja tudo conforme combinado, o cliente qualifica positivamente o vendedor, e o valor da venda é liberado ao vendedor pelo Mercado Livre. Se houver algum problema com o produto, o cliente entra em contato com o vendedor para negociar uma solução ou devolver o item. Nessa situação, o valor pago será restituído ao comprador.

## Modelo BPMN Desenvolvido

Abaixo está o modelo de processo desenvolvido com base na descrição fornecida:

<div align = center>
<img src="diagram (14).svg" alt="Mapeamento do fluxo atual de negócio em BPMN">
</div>

O modelo BPMN desenvolvido representa o processo completo de compra de produtos no site do Mercado Livre, desde a escolha do produto pelo cliente até a liberação ou restituição do pagamento ao vendedor ou ao comprador, respectivamente. O fluxo foi criado utilizando a ferramenta bpmn.io (https://demo.bpmn.io/) e levou em conta a descrição fornecida no desafio proposto, embora algumas decisões de modelagem tenham sido tomadas com base em critérios de clareza e simplicidade.

#### Visão Geral do Processo

O processo se inicia com o cliente acessando o site do Mercado Livre e adquirindo um ou mais produtos. Após selecionar os itens desejados, ele realiza o pagamento por meio de uma das duas opções disponíveis: PayPal ou Mercado Pago. O pagamento é processado e confirmado, gerando uma notificação para o vendedor, que então se responsabiliza por postar o produto. A entrega é realizada pelos Correios e, ao recebê-lo, o cliente verifica se o produto atende às suas expectativas. Caso esteja tudo conforme combinado, ele qualifica positivamente o vendedor, e o valor correspondente à venda é liberado. Por outro lado, caso haja algum problema, o cliente entra em contato com o vendedor para negociar uma solução ou devolver o produto, acionando assim o processo de restituição do valor pago.

#### Principais Atores do Processo

Ao longo do fluxo modelado, cinco atores principais foram identificados, cada um com funções específicas e bem definidas dentro do cenário descrito. 
- O **cliente** é o protagonista do processo, pois é quem inicia a transação e toma as decisões finais quanto à aceitação ou não do produto recebido. Ele também é responsável por realizar o pagamento e por informar ao sistema do Mercado Livre se deseja qualificar o vendedor de maneira positiva.
- O **vendedor**, por sua vez, responde pela disponibilização dos produtos e pela postagem após a confirmação do pagamento. Além disso, mantém interação direta com o cliente em situações de negociação ou devolução.
- O **Mercado Livre** age como intermediador entre as partes, controlando o fluxo de informações, gerenciando a liberação de pagamentos e garantindo a integridade do processo.
- Os **meios de pagamento**, representados por PayPal e Mercado Pago, têm papel essencial na validação e processamento financeiro da transação.
- Os **Correios** são responsáveis pela logística da entrega, compreendendo desde a postagem até a entrega final ao cliente.

#### Esquema de Cores Adotado

Com o objetivo de tornar o diagrama mais intuitivo e fácil de interpretar, foi utilizado um esquema de cores estratégico para diferenciar os tipos de atividades e elementos do processo. As cores escolhidas ajudam a destacar aspectos importantes e a facilitar a leitura visual do modelo. 
- A cor **amarela** indica pontos de decisão críticos, onde um ator precisa avaliar e escolher qual caminho seguir. Nesse contexto, aparecem como condições no fluxo, como a verificação da conformidade do produto pelo cliente e a escolha entre seguir com a avaliação positiva ou iniciar uma negociação ou devolução.
- A cor **vermelha**, por sua vez, marca os possíveis pontos de término do processo, isto é, os desfechos possíveis do fluxo principal — seja a conclusão com sucesso (liberação do pagamento), seja a devolução do valor ao cliente. 

#### Subprocessos e Complexidade Logística

Algumas etapas do processo envolvem uma série de ações internas que, embora não estejam explicitadas no diagrama principal, são representadas como subprocessos. Isso contribui para a legibilidade do modelo geral, evitando sobrecarregar o observador com detalhes excessivos. Um exemplo relevante é o fluxo relacionado aos **Correios**, que engloba diversas atividades como a catalogação do pacote, verificação no sistema de rastreamento, geração de código, transporte físico e entrega ao destinatário. Ao agrupar todas essas ações em um único subprocesso, mantemos o foco no fluxo global do negócio, enquanto deixamos aberta a possibilidade de expandir esse bloco em uma análise mais granular.

#### Simplificações Realizadas

Embora o modelo busque retratar fielmente o processo descrito, algumas simplificações foram adotadas devido a limitações no escopo do desafio. Por exemplo, não foram incluídas todas as possíveis variações de comportamento, como situações em que o vendedor recusa uma devolução ou quando há impasse nas negociações com o cliente. Outro ponto omitido refere-se ao retorno do produto pelos Correios ao vendedor, bem como os impactos desse evento no andamento do pagamento. Esses casos podem ser explorados em futuras extensões do modelo, caso se deseje aprofundar a análise de exceções e caminhos alternativos dentro do processo. Além disso, fluxos secundários, como disputas de pagamento ou intervenções externas (como órgãos reguladores ou sistemas de proteção ao consumidor), também não foram considerados, por estarem fora do escopo inicial do exercício.

Em resumo, o modelo BPMN aqui apresentado busca representar de maneira clara e organizada o processo de compra e venda no Mercado Livre, com destaque para os papéis dos diferentes atores, o uso estratégico de cores para auxiliar na interpretação e a abordagem de subprocessos para lidar com complexidades logísticas e operacionais. Apesar das simplificações feitas, o diagrama reflete com fidelidade o fluxo principal proposto, oferecendo uma boa base para análises posteriores e refinamentos adicionais.
