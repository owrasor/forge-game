# O que um bot precisa saber fazer

Type: grilling
Label: wayfinder:grilling
Status: resolved
Assignee: owrasor
Blocked by: 05, 06, 07, 08

## Question

O que um bot precisa saber fazer para a partida mata-mata contar como jogável contra bots?

Há um jogador e o restante são bots, no mesmo mapa, com as mesmas três armas. A spec não pede uma IA de jogo final. Pede o mínimo para o mata-mata funcionar de verdade: o jogador enfrenta combatentes, não alvos parados.

Respeitar como as armas são obtidas ([Como o combatente obtém as armas](./05-como-o-combatente-obtem-as-armas.md)): o bot entra só com a pistola e pega shotgun e metralhadora nos pontos de arma. Também respeitar a queda ([O que acontece quando um combatente morre](./06-o-que-acontece-quando-um-combatente-morre.md)): 3 segundos fora, volta num ponto de volta livre, só com a pistola, sem vista. Também respeitar o movimento ([Qual é o movimento do combatente](./07-qual-e-o-movimento-do-combatente.md)): o bot desloca, olha e pula na mesma velocidade, atravessa outros combatentes, e não agacha nem corre. Também respeitar como o tiro resolve ([Como um tiro resolve](./08-como-um-tiro-resolve.md)): os mesmos raios, tempos e leque, com a shotgun decidindo no perto quando o olhar está no corpo. Não criar níveis de dificuldade nesta decisão, a menos que o mínimo jogável exija mais de um.

## Answer

Os três bots fazem o mesmo. Cada um enfrenta todo combatente que não seja ele.

O bot sabe de um combatente quando há uma linha livre até o corpo, em volta do bot inteiro. A parede esconde o corpo. Outro combatente no meio também esconde. Cada bot usa só a própria linha. Ele sabe onde estão os pontos de arma.

O olhar vai na hora para o corpo mais próximo que tem linha. Se a distância empata, o olhar fica em qualquer um desses. Se outro corpo fica mais perto, o olhar muda na hora para ele.

Com a linha, o bot fecha até a distância em que a melhor arma que ele tem acerta, e segura o disparo no caminho. Se já está dentro dessa distância, dispara ali e permanece. Se o corpo sai dessa distância, ele fecha de novo e segura o disparo. Se a linha some, ele deixa de fechar.

Só com a pistola, ele dispara no lugar em que a linha abriu e permanece ali enquanto a linha durar. Com metralhadora e sem shotgun, a distância é oito comprimentos de corpo e a arma do disparo é a metralhadora. Com shotgun, a distância é três comprimentos e a arma do disparo é a shotgun.

No disparo, o olhar fica no corpo. Os raios, os tempos e o leque são os de [Como um tiro resolve](./08-como-um-tiro-resolve.md).

Sem linha, o bot vai ao ponto mais próximo de uma arma que ainda não tem. Shotgun e metralhadora valem igual. Se a distância empata, vale qualquer um desses pontos. No ponto vazio, ele espera. A arma volta como está em [Como o combatente obtém as armas](./05-como-o-combatente-obtem-as-armas.md). Uma linha durante a espera entrega o comando ao corpo.

Com a shotgun e a metralhadora, e sem linha, ele vai ao ponto de arma mais próximo em que não está. Ao chegar, escolhe de novo.

No caminho, um obstáculo baixo leva um pulo, como em [Qual é o movimento do combatente](./07-qual-e-o-movimento-do-combatente.md).

Fora de fechar e de disparar, o olhar aponta para onde ele vai. Parado à espera no ponto, o olhar fica na direção em que chegou.

Na volta da queda ele está só com a pistola, e este mesmo comportamento recomeça. A queda está em [O que acontece quando um combatente morre](./06-o-que-acontece-quando-um-combatente-morre.md). A munição continua em [A arma gasta munição](./16-a-arma-gasta-municao.md).
