# O que acontece quando um combatente morre

Type: grilling
Label: wayfinder:grilling
Status: resolved
Assignee: owrasor
Blocked by: 05

## Question

O que acontece com um combatente no instante em que ele morre, até voltar a lutar?

A partida continua para os outros. O placar e a condição de vitória pertencem a [Como uma partida termina](./03-como-uma-partida-termina.md); não redecidir isso aqui. Como as armas entram na partida pertence a [Como o combatente obtém as armas](./05-como-o-combatente-obtem-as-armas.md): ele entra só com a pistola e, durante a vida, guarda o que pegou. A volta ao combate tem de caber nisso.

Fechar o que o combatente perde, onde ele volta e quanto tempo fica fora. A mesma regra vale para o jogador e para o bot.

## Answer

A queda tira o combatente do mapa na hora. Não fica ninguém no lugar. A shotgun e a metralhadora somem com ele. O abate entra no placar nesse instante.

Por 3 segundos ele está fora da luta: não dispara, não é atingido e não pega arma. O relógio da partida continua. O jogador vê o lugar da queda com a câmera parada, a luta segue nessa vista, e vê os segundos inteiros que faltam. O bot não tem vista.

A volta é num ponto de volta, só com a pistola empunhada. O sorteio prefere um ponto sem combatente em cima. Se todos estão ocupados, sorteia qualquer um. Se os 5 minutos acabam durante a espera, ele não volta. No instante da volta ele já pode ser atingido e já pode disparar. Esses 3 segundos são a única proteção.

A partida começa com cada combatente num ponto de volta diferente. O mapa tem pelo menos um ponto por combatente, e ponto sobrando fica vazio. Quantos pontos existem, onde ficam e o cuidado de colocá-los fora do centro da troca de tiros continuam em [Como é o mapa](./11-como-e-o-mapa.md). O que causa a queda continua em [Como um tiro resolve](./08-como-um-tiro-resolve.md). De quem é o abate quando mais de um feriu a vítima continua em [Quem recebe o abate](./15-quem-recebe-o-abate.md). A munição da pistola na volta continua em [A arma gasta munição](./16-a-arma-gasta-municao.md). Sair do espaço da luta continua em [Sair do mapa causa uma queda](./18-sair-do-mapa-causa-uma-queda.md).
