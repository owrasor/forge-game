Label: wayfinder:map
Status: open

## Destination

Uma especificação do MVP de um FPS de desktop para Linux, Windows e macOS. A spec descreve uma partida mata-mata num único mapa, com um jogador e bots, até 10 combatentes, e três armas (pistola, shotgun, metralhadora). O mapa termina quando não resta decisão de produto antes de alguém implementar o jogo.

## Notes

Domínio: FPS mata-mata local, primeiro jogo de quem nunca desenvolveu jogos. Vocabulário em `GLOSSARY.md`. A pasta do repositório se chama `forge-arpg`; isso não é o nome do jogo.

Tracker: markdown local em `.scratch/mata-mata-mvp/`. Não há issue tracker configurado neste repositório.

Cada sessão consulta grilling e domain-modeling. Ticket `research` consulta a skill research. Ticket `prototype` consulta a skill prototype. Texto da spec e dos tickets em português.

Preferências já fechadas: a partida roda inteira no computador do jogador; controles são teclado e mouse; a sessão é iniciar, combater, terminar, ver o resultado e jogar de novo; o visual é simples e legível, de primeiro jogo.

Achados de research ficam num branch `research/<nome>`, com ponteiro no ticket. Esse branch não é mesclado.

## Decisions so far

<!-- the index: one line per closed ticket, enough to judge relevance, then zoom the link for the detail the ticket holds -->

- [Como uma partida termina](issues/03-como-uma-partida-termina.md): dura 5 minutos, vence quem tem mais abates, topo dividido é empate, e o resultado lista todos.
- [Quais motores cabem neste MVP](issues/01-quais-motores-cabem-neste-mvp.md): Godot 4.7.2, Unity 6.6 e Unreal 5.8 exportam o FPS local nos três desktops.
- [Qual é o papel de cada arma](issues/04-qual-e-o-papel-de-cada-arma.md): pistola longe e tiro a tiro, shotgun perto, metralhadora no meio em rajada; nenhuma muda a velocidade.
- [Qual motor a spec adota](issues/02-qual-motor-a-spec-adota.md): Godot 4.7.2 com GDScript; builds Linux e Windows x86_64 e macOS Universal 2 em ZIP, com o arquivo de licença MIT ao lado do executável.
- [Como o combatente obtém as armas](issues/05-como-o-combatente-obtem-as-armas.md): entra só com a pistola; shotgun e metralhadora vêm de pontos de arma que devolvem a mesma arma em 15 segundos; pegar acrescenta e a troca é imediata.
- [O que acontece quando um combatente morre](issues/06-o-que-acontece-quando-um-combatente-morre.md): a queda tira da luta por 3 segundos e a volta é num ponto de volta, só com a pistola; esses 3 segundos são a única proteção.
- [Qual é o movimento do combatente](issues/07-qual-e-o-movimento-do-combatente.md): desloca, olha e pula, numa velocidade só; combatente atravessa combatente; o pulo mede o mapa.
- [Como um tiro resolve](issues/08-como-um-tiro-resolve.md): raios instantâneos; a vida tem oito partes; pistola e shotgun tiram duas, metralhadora uma; perto são três comprimentos de corpo e o meio vai até oito.

## Not yet specified

- O que a tela mostra da munição, se a arma gastar tiros. Depende de [A arma gasta munição](issues/16-a-arma-gasta-municao.md).
- Se o bot tem mais de um nível de dificuldade. Depende do que o bot precisa saber fazer.
- Qual feedback sonoro mínimo a spec exige. Trilha, dublagem e polish já estão fora; o que resta é o som que o combate precisa para ser legível.
- Se a spec precisa de um nome de jogo, distinto do modo mata-mata e do nome da pasta.

## Out of scope

- Implementar o jogo jogável. Este esforço entrega a spec.
- Outros humanos na mesma partida, jogo em rede, servidor, e arquitetura já preparada para uma partida online.
- Mais mapas, mais armas, outros modos, e a evolução do jogo depois do MVP.
- Conta, ranking, desbloqueio, progressão e customização do combatente.
- Suporte a controle.
- Arte final, trilha, dublagem e polish.
- Notarização Apple, DMG e publicação do jogo para outras pessoas. O MVP pede o build exportável. Ver [Qual motor a spec adota](issues/02-qual-motor-a-spec-adota.md).
- Tela de créditos. O aviso da licença é um arquivo junto do build. Ver [Qual motor a spec adota](issues/02-qual-motor-a-spec-adota.md).
