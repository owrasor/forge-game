# O que um bot precisa saber fazer

Type: grilling
Label: wayfinder:grilling
Status: open
Blocked by: 05, 06, 07, 08

## Question

O que um bot precisa saber fazer para a partida mata-mata contar como jogável contra bots?

Há um jogador e o restante são bots, no mesmo mapa, com as mesmas três armas. A spec não pede uma IA de jogo final. Pede o mínimo para o mata-mata funcionar de verdade: o jogador enfrenta combatentes, não alvos parados.

Respeitar como as armas são obtidas ([Como o combatente obtém as armas](./05-como-o-combatente-obtem-as-armas.md)): o bot entra só com a pistola e pega shotgun e metralhadora nos pontos de arma. Também respeitar a queda ([O que acontece quando um combatente morre](./06-o-que-acontece-quando-um-combatente-morre.md)): 3 segundos fora, volta num ponto de volta livre, só com a pistola, sem vista. Também respeitar o movimento ([Qual é o movimento do combatente](./07-qual-e-o-movimento-do-combatente.md)): o bot desloca, olha e pula na mesma velocidade, atravessa outros combatentes, e não agacha nem corre. Também respeitar como o tiro resolve ([Como um tiro resolve](./08-como-um-tiro-resolve.md)): os mesmos raios, tempos e leque, com a shotgun decidindo no perto quando o olhar está no corpo. Não criar níveis de dificuldade nesta decisão, a menos que o mínimo jogável exija mais de um.
