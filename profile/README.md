# Monitoramento de Fluxo em Supermercados com IoT

Projeto interdisciplinar desenvolvido na São Paulo Tech School (SPTech), no curso de Ciência da Computação.

## O que é o projeto

O sistema monitora o fluxo de consumidores dentro de um supermercado usando sensores ultrassônicos (HC-SR04) conectados a um microcontrolador. A ideia é coletar dados de três pontos da loja:

- **Entrada:** registra quantas pessoas entram no estabelecimento.
- **Corredores:** registra a circulação nas aberturas de cada corredor, permitindo comparar quais áreas da loja recebem mais fluxo.
- **Caixas (após o pagamento):** um sensor posicionado depois da área de pagamento registra a passagem do consumidor que acabou de ser atendido. Como o sensor está posicionado fisicamente após o caixa, a passagem indica que uma compra foi concluída, sem que o sistema precise se integrar ao PDV ou a qualquer sistema financeiro da loja.

Com esses três dados, o sistema calcula a proporção entre quem entrou na loja e quem efetivamente passou pelo caixa, gerando uma taxa de conversão medida pelo próprio sistema.

## Como funciona

Cada ponto monitorado recebe um sensor ultrassônico. O sensor mede a distância até a superfície à sua frente de forma contínua. Quando uma pessoa passa, a distância cai bruscamente e o microcontrolador registra uma contagem. Os sensores disparam em sequência para evitar interferência entre leituras próximas.

Os dados são enviados a um banco de dados MySQL e exibidos em um dashboard web com gráficos de fluxo por área, ocupação das filas e histórico de alertas.

O sistema trabalha com contagens agregadas. Não há identificação individual de consumidores, reconhecimento facial ou rastreamento de trajetória.

## Tecnologias

- Arduino e sensores HC-SR04
- HTML, CSS e JavaScript (Chart.js)
- MySQL em máquina virtual Linux
- Git e GitHub para versionamento

## Equipe

- ANDREY SEBASTIAN JUSTINO
- GUILHERME ALCOVA
- LUCAS MEIRELES
- MATHEUS GODOY
- RODRIGO AZEVEDO DE ANDRADE
- VICTOR MANSUR


## Contexto acadêmico

Disciplina de Pesquisa e Inovação, Sprint 2.
Docente: Fernanda Caramico, MSc.
