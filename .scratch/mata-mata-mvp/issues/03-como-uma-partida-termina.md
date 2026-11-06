# Como uma partida termina

Type: grilling
Label: wayfinder:grilling
Status: resolved
Assignee: owrasor

## Question

Como uma partida mata-mata termina, e o que o resultado mostra ao jogador?

Há um jogador e bots, até 10 combatentes, sem times. A sessão precisa de um fim e de um resultado, e então a opção de jogar de novo. Não há ranking persistente nem conta.

Fechar a condição de término e quais fatos o resultado precisa exibir para o jogador saber como a partida acabou. Não definir HUD durante o combate, telas de menu, nem o que acontece no instante da morte: isso está em [Quais telas a sessão tem](./12-quais-telas-a-sessao-tem.md) e [O que acontece quando um combatente morre](./06-o-que-acontece-quando-um-combatente-morre.md).

## Answer

A partida dura 5 minutos. Um abate é eliminar outro combatente, e soma um no placar de quem eliminou. Aos 5 minutos a partida acaba; eliminar alguém depois disso não conta.

Vence o combatente com mais abates do que cada um dos outros. Qualquer combatente pode vencer, bot incluído. O jogador é mais um no placar. Se dois ou mais dividem o maior número, o resultado é empate entre eles. Se ninguém abateu ninguém, todos empatam.

O resultado lista todos os combatentes, do maior número de abates ao menor, com esse número ao lado de cada um. Nomeia o vencedor, ou quem dividiu o topo. Combatentes com a mesma contagem não têm ordem obrigatória entre si.

Quem recebe o abate quando mais de um combatente feriu a vítima fica em [Quem recebe o abate](./15-quem-recebe-o-abate.md). O que o jogador vê do tempo e do placar no meio da luta fica em [O que o jogador vê do tempo e do placar](./14-o-que-o-jogador-ve-do-tempo-e-do-placar.md).
