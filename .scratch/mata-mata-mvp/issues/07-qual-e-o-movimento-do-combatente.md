# Qual é o movimento do combatente

Type: grilling
Label: wayfinder:grilling
Status: resolved
Assignee: owrasor

## Question

Qual é o vocabulário de movimento de um combatente neste FPS?

Teclado e mouse. Primeira pessoa. A spec é de um primeiro jogo, com visual simples: o movimento cabe nesse corte. Controle de gamepad está fora.

Fechar o que o combatente consegue fazer com o corpo (deslocar, olhar, e o que mais for necessário para o mata-mata funcionar). Nenhuma arma muda a velocidade: isso está em [Qual é o papel de cada arma](./04-qual-e-o-papel-de-cada-arma.md). Não fechar campo de visão nem bob de câmera. Não fechar o layout do mapa: isso é [Como é o mapa](./11-como-e-o-mapa.md). Durante a queda o combatente não se move, e a volta o coloca num ponto de volta. Isso está em [O que acontece quando um combatente morre](./06-o-que-acontece-quando-um-combatente-morre.md). Não reabrir a queda.

## Answer

O corpo faz três atos: deslocar, olhar e pular. O bot usa os mesmos. Agachar, correr mais rápido, escorregar e inclinar ficam de fora.

O jogador desloca com W, A, S e D, na direção do olhar, numa velocidade só, no chão e no ar, com qualquer arma. A velocidade entra e sai na hora. O olhar segue o mouse na hora: mouse para cima olha para cima, a horizontal dá a volta inteira, a vertical para ao olhar para cima e para baixo.

O pulo é um aperto de espaço com os pés no chão. Sobe sempre à mesma altura, bastante para um obstáculo baixo, e o mapa se mede por esse pulo. No ar ele ainda desloca. Sem chão, cai, mesmo sem ter pulado, e o próximo pulo espera os pés no chão. Um teto interrompe a subida. Segurar espaço não pula de novo ao aterrissar.

O chão firme, mesmo em ladeira, não escorrega. Parede e teto seguram o corpo: a parede anula só o avanço contra ela. Combatente atravessa combatente. Cair de um piso para outro não tira vida e não é queda.

Campo de visão e movimento de cabeça ficam em [Qual é a câmera durante a luta](./19-qual-e-a-camera-durante-a-luta.md). O que o tiro faz enquanto o corpo se move continua em [Como um tiro resolve](./08-como-um-tiro-resolve.md). Sair do espaço continua em [Sair do mapa causa uma queda](./18-sair-do-mapa-causa-uma-queda.md).
