# Godot 4.7.2 para o MVP

O mata-mata local precisa de um motor que exporte Linux, Windows e macOS, com primeira pessoa e bots num mapa, para quem nunca fez um jogo. A spec adota Godot 4.7.2 estável e GDScript. Godot é MIT, não pede conta, e o editor documenta distribuições Linux recentes. Unity 6.6 e Unreal 5.8 também exportam os três desktops; o peso de conta, launcher e editor no Linux pesou mais do que o template de FPS que eles já trazem.

## Considered options

- Unity 6.6, com C# e o plano Personal.
- Unreal Engine 5.8, com Blueprint ou C++ e o template First Person.

## Consequences

Os três builds saem do editor no Linux: Linux x86_64, Windows x86_64 e um ZIP de macOS Universal 2 com assinatura ad-hoc. O código do jogo fica em GDScript. Primeira pessoa e o caminho dos bots usam o olhar com o mouse, `CharacterBody3D` e `NavigationAgent3D`. Cada build leva um arquivo com o copyright, a licença MIT e o link para https://godotengine.org/license. A sessão não tem tela de créditos.

O detalhe está em [Qual motor a spec adota](../../.scratch/mata-mata-mvp/issues/02-qual-motor-a-spec-adota.md).
