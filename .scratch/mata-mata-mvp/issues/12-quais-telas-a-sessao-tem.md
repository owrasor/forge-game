# Quais telas a sessão tem

Type: grilling
Label: wayfinder:grilling
Status: resolved
Assignee: owrasor
Blocked by: 03, 09

## Question

Quais telas existem entre abrir o jogo e o fim de uma partida?

O ciclo já fechado é: iniciar a partida, combater, a partida terminar, o resultado aparecer, jogar de novo. Sem conta, ranking, desbloqueio, progressão, customização ou tela de opções além de sair da partida. Teclado e mouse.

Como a partida termina está em [Como uma partida termina](./03-como-uma-partida-termina.md). Quantos bots entram está em [Quantos bots entram na partida](./09-quantos-bots-entram-na-partida.md). Fechar a sequência de telas e o que cada uma precisa mostrar. Não desenhar o HUD do combate. Se a partida acaba durante uma queda, o resultado toma o lugar da vista parada. A queda em si está em [O que acontece quando um combatente morre](./06-o-que-acontece-quando-um-combatente-morre.md). Não criar uma tela só para ela.

O aviso de licença do Godot não é uma tela. Ele viaja num arquivo ao lado do build, decidido em [Qual motor a spec adota](./02-qual-motor-a-spec-adota.md).

## Answer

A sessão tem a abertura, a luta e o resultado.

A abertura mostra duas ações, escolhidas com o mouse: iniciar e sair do jogo. Iniciar começa a partida com o jogador e 3 bots, e o olhar do mouse passa a valer. Sair do jogo fecha o jogo. Esc na abertura sai do jogo.

Na luta, o tempo corre os 5 minutos. Esc, também durante a queda, leva à abertura e a partida acaba ali. O resultado entra quando os 5 minutos se cumprem. Se o jogador está na vista parada da queda, o resultado toma o lugar dela, como a queda está em [O que acontece quando um combatente morre](./06-o-que-acontece-quando-um-combatente-morre.md). O que a luta mostra do tempo, do placar, das armas, da vida, da mira e da munição fica em [O que o jogador vê do tempo e do placar](./14-o-que-o-jogador-ve-do-tempo-e-do-placar.md), [O que o jogador vê das armas que carrega](./17-o-que-o-jogador-ve-das-armas-que-carrega.md), [O que o jogador vê da vida, da mira e do acerto](./20-o-que-o-jogador-ve-da-vida-da-mira-e-do-acerto.md) e [A arma gasta munição](./16-a-arma-gasta-municao.md).

O resultado lista os combatentes como está em [Como uma partida termina](./03-como-uma-partida-termina.md). Duas ações, com o mouse. Jogar de novo começa outra partida na hora, com os mesmos 3 bots, e o olhar do mouse volta a valer. Voltar leva à abertura. Esc no resultado volta à abertura.

Na abertura e no resultado, o mouse é cursor. Na luta, o olhar segue o mouse.

O aviso de licença continua num arquivo ao lado do build, como está em [Qual motor a spec adota](./02-qual-motor-a-spec-adota.md).
