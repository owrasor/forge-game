# Como o combatente obtém as armas

Type: grilling
Label: wayfinder:grilling
Status: resolved
Assignee: owrasor

## Question

Como um combatente passa a ter a pistola, a shotgun e a metralhadora durante a partida, e como troca de uma para a outra?

Não há progressão, loja nem desbloqueio. São só estas três armas. A resposta vale para o jogador e para o bot.

Não definir o papel de cada arma além do necessário para esta decisão. O papel está em [Qual é o papel de cada arma](./04-qual-e-o-papel-de-cada-arma.md). Não definir munição: isso é [A arma gasta munição](./16-a-arma-gasta-municao.md). Não definir com o que o combatente volta quando morre: isso é [O que acontece quando um combatente morre](./06-o-que-acontece-quando-um-combatente-morre.md), que espera esta resposta.

## Answer

No início da partida o combatente tem só a pistola, já empunhada. O bot entra do mesmo jeito.

Só a shotgun e a metralhadora têm ponto de arma. Cada ponto oferece uma das duas e mostra qual é. A partida abre com os pontos cheios. Quem ainda não tem a arma e chega primeiro leva a única do ponto. O ponto esvazia e, 15 segundos depois, a mesma arma volta. Quem já a tem deixa o ponto como está, sem reiniciar a espera. Quem está em cima quando ela volta, e ainda não a tem, pega na hora e já a empunha. Se dois chegam juntos, um só leva.

Pegar acrescenta, até as três, sem segunda cópia. Durante a vida não há como largar. O jogador troca na hora: 1 pistola, 2 shotgun, 3 metralhadora. A roda percorre essa ordem, só entre as armas que ele já tem. A troca interrompe o disparo em curso. O bot também troca na hora entre as armas que já pegou.

Onde ficam os pontos e quantos são continuam em [Como é o mapa](./11-como-e-o-mapa.md). Munição continua em [A arma gasta munição](./16-a-arma-gasta-municao.md). O que a morte tira continua em [O que acontece quando um combatente morre](./06-o-que-acontece-quando-um-combatente-morre.md). O que o jogador vê das armas que carrega fica em [O que o jogador vê das armas que carrega](./17-o-que-o-jogador-ve-das-armas-que-carrega.md).
