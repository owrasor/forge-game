# Quais motores cabem neste MVP

Type: research
Label: wayfinder:research
Status: resolved
Assignee: research/motores

## Question

Quais motores de jogo, com documentação primária atual, conseguem produzir este MVP, e que limites cada um impõe?

O MVP é um FPS 3D de desktop para Linux, Windows e macOS. Uma partida mata-mata roda inteira no computador do jogador: um jogador humano, bots, até 10 combatentes, um mapa, três armas (pistola, shotgun, metralhadora), teclado e mouse, visual simples. Não há rede, conta, progressão nem arte final. Quem vai implementar nunca desenvolveu um jogo.

A resposta é o fato que a decisão de motor espera: motores viáveis, o que a documentação de cada um garante para exportar os três sistemas, controle em primeira pessoa, navegação de bots no mapa, licença e custo, e o que pesa para um primeiro jogo. A escolha do motor fica em [Qual motor a spec adota](./02-qual-motor-a-spec-adota.md). Não fechar essa escolha aqui.

Achados no branch `research/motores`, arquivo `docs/research/motores-fps-mvp.md`. O branch não é mesclado.

## Answer

Godot 4.7.2, Unity 6.6 (com a LTS 6.3 ainda publicada) e Unreal Engine 5.8 cumprem exportação para Linux, Windows e macOS, primeira pessoa documentada, navigation mesh e licença de jogo indie pequeno. O detalhe de versão, custo, linguagem e o que pesa num primeiro jogo está no arquivo de pesquisa. A escolha do motor continua aberta.

Branch `research/motores`, arquivo `docs/research/motores-fps-mvp.md`. Esse branch não foi mesclado.
