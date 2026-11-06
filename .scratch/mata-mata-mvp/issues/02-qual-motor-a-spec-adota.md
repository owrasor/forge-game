# Qual motor a spec adota

Type: grilling
Label: wayfinder:grilling
Status: resolved
Assignee: owrasor
Blocked by: 01

## Question

Qual motor a spec do MVP adota?

A partida é local, em primeira pessoa, com bots num único mapa, teclado e mouse, e build para Linux, Windows e macOS. Quem implementa nunca fez um jogo. Visual simples. Sem rede.

Usar os achados de [Quais motores cabem neste MVP](./01-quais-motores-cabem-neste-mvp.md), no branch `research/motores`, arquivo `docs/research/motores-fps-mvp.md`. Fechar um motor e o que essa escolha obriga a spec a respeitar. Não reabrir rede, controle ou arte final.

## Answer

A spec adota Godot 4.7.2 estável, o editor padrão, com o código do jogo só em GDScript. A versão é a estável lida em 29 de outubro de 2026 em [Quais motores cabem neste MVP](./01-quais-motores-cabem-neste-mvp.md).

Os builds do MVP são Linux x86_64, Windows x86_64 e macOS Universal 2. Os três saem do editor no Linux, com os export templates oficiais do 4.7.2. O macOS é um ZIP com o .app e assinatura ad-hoc.

Cada build leva, num arquivo ao lado do executável, o aviso de copyright do Godot, o texto da licença MIT e o link para https://godotengine.org/license. A sessão não tem tela de créditos. [Quais telas a sessão tem](./12-quais-telas-a-sessao-tem.md) continua no ciclo já fechado.

A spec descreve a primeira pessoa e o caminho dos bots como comportamento do mata-mata. O caminho de implementação são o olhar com o mouse, `CharacterBody3D` e `NavigationAgent3D`. Renderizador e backend de física ficam nos padrões do Godot 4.7.2.

Ficam de fora deste fechamento: notarização Apple, DMG, 32 bits, Linux ARM, C#, GDExtension e Godot 4.8.

ADR: [Godot 4.7.2 para o MVP](../../../docs/adr/0001-godot-4-7-2-para-o-mvp.md).
