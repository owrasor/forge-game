# Como um tiro resolve

Type: grilling
Label: wayfinder:grilling
Status: resolved
Assignee: owrasor
Blocked by: 02, 04

## Question

Como um tiro acerta um combatente, e como vida e dano se relacionam entre a pistola, a shotgun e a metralhadora?

O papel de cada arma está em [Qual é o papel de cada arma](./04-qual-e-o-papel-de-cada-arma.md). O motor está em [Qual motor a spec adota](./02-qual-motor-a-spec-adota.md). A resposta tem de caber nos dois: a fantasia de cada arma e o que o motor realmente oferece para um tiro em primeira pessoa.

A troca de arma é imediata e interrompe o disparo em curso, como está em [Como o combatente obtém as armas](./05-como-o-combatente-obtem-as-armas.md). Não reabrir a troca. O corpo desloca, olha e pula enquanto pode disparar, na mesma velocidade, como está em [Qual é o movimento do combatente](./07-qual-e-o-movimento-do-combatente.md). Não reabrir o movimento.

Quando a vida acaba, a queda é a de [O que acontece quando um combatente morre](./06-o-que-acontece-quando-um-combatente-morre.md). Não reabrir a queda. Este ticket fecha o que faz a vida acabar.

Não reabrir o papel em abstrato, o motor, nem munição. Munição é [A arma gasta munição](./16-a-arma-gasta-municao.md). Não desenhar o HUD. Não decidir de quem é o abate quando mais de um combatente feriu a vítima: isso é [Quem recebe o abate](./15-quem-recebe-o-abate.md). Fechar o modelo do acerto e a relação de vida e dano que torna os três papéis verdadeiros na partida.

## Answer

O disparo manda raios instantâneos na direção do olhar. O cenário ou o primeiro combatente para cada raio. Raios do mesmo leque podem acertar combatentes diferentes. O raio de quem disparou não o fere. O corpo é um volume só.

A vida é igual para todos, em oito partes, e não se recupera no meio da luta. A pistola e cada raio da shotgun tiram duas partes. A metralhadora tira uma. Ao chegar a zero, começa a queda. Na volta, a vida enche.

A pistola dispara no aperto, um raio exato, e espera meio segundo. Quatro acertos levam um segundo e meio, em qualquer distância.

A shotgun dispara no aperto um leque de 8 raios, até três comprimentos de corpo, e espera oito décimos. Quatro raios no mesmo corpo acabam a vida na hora. Olhar no centro do corpo, nesse perto, põe quatro ou mais raios nele.

A metralhadora dispara no aperto e, com o disparo preso, repete a cada décimo. Oito acertos levam sete décimos. A rajada começa no olhar e anda. Até oito comprimentos, quem mantém o olhar no corpo mantém a rajada nele. Além disso, os raios saem do corpo.

Deslocar e pular não mudam o tiro. O bot usa os mesmos raios, tempos e leque. Munição continua em [A arma gasta munição](./16-a-arma-gasta-municao.md). De quem é o abate quando mais de um feriu a vítima continua em [Quem recebe o abate](./15-quem-recebe-o-abate.md). O que a tela mostra da vida, da mira e do acerto fica em [O que o jogador vê da vida, da mira e do acerto](./20-o-que-o-jogador-ve-da-vida-da-mira-e-do-acerto.md).
