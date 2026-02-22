

Isso é um simples arquivo com algumas instruções sobre como usar macros (e coisas gerais do roll 20)

# Como referenciar 

Forma básica: @{referenciado|atributo}

O referenciado pode ser feito de 4 formas:
- Deixado em branco (também removendo a barra vertical): isso funciona quando é referenciado dentro da ficha do personagem, então não funciona em macros, mas funciona em atributos e habiidades;
- O nome de um personagem específico: isso sempre vai referenciar o personagem especificado pelo nome;
- 'selected': o atributo será conferido no token que estiver selecionado atualmente;
- 'target': o roll20 irá pedir um alvo a ser clicado após rodar o macro. Basta clicar no alvo desejado. Não é necessário clicar múltiplas vezes no mesmo alvo. Para ter múltiplos alvos, colocar uma barra adicional e dar um nome a esse alvo (por exemplo target|Alvo1), assim se houver mais de um nome sendo referenciado por target, irá mostrar o nome desses.

# Atributos padrão

Existem coisas que podem ser referenciadas independentemente do atributo existir:
- token_name
- token_id

# Comandos

/em: É basicamente uma ação, sempre sendo precedido pelo nome do personagem selecionado. ('em' vem de emote)
/desc: Uma descrição sem personagem responsável, normalmente sendo o GM descrevendo uma cena.
/fx: Permite usar efeitos especiais (descrito mais na sua sub-sessão)

## Efeitos especiais

Forma básica: /fx tipo-cor id_source id_target

tipo: Muda a animação em si.
- beam
- bomb
- breath
- bubbling
- burn
- burst
- explode
- glow
- missile
- nova
- splatter

cor: Como indicado pelo nome, vai mudar a cor do efeito especial, dando a impressão de elementos diferentes.
- acid
- blood
- charm
- death
- fire
- frost
- holy
- magic
- slime
- smoke
- water

id_target: É opcional a depender do tipo

# Escolhas

É possível dar ao usuário escolhas sobre o macro no seu uso.
Esses são feito precedendo um par de chaves com uma interrogação.

## Escolher ação

Se houver várias barras verticais, é possível escolher dentre diversas opções quando usar o macro

?{Pergunta|NomeOpcao1, comandoOpcao1|NomeOpcao2, comandoOpcao2|...|NomeOpcaoN, comandoOpcaoN}

## Escolher valor

Se não houver barras verticais

# Nomear valores

Suceder um valor com um nome entre chaves permite que esse seja nomeado nos resultados para melhor identificação e clareza
Ex:
```rmacro
@{selected|proficiencia_bonus}[Bônus de Proficiência]
```

# Links

- https://gist.github.com/esron/ce919d95306097e10c911713617a238b
- https://wiki.roll20.net/Macros
- https://wiki.roll20.net/Character#Attributes
- https://wiki.roll20.net/Chat_Menus
- https://wiki.roll20.net/Roll_Template
- https://wiki.roll20.net/5E_Macros
- https://cybersphere.me/roll20-sheet-author-master-list/

## Códigos que talvez use no futuro

- https://www.reddit.com/r/Roll20/comments/7jsbf2/macro_questions_logic_summing/
- https://wiki.roll20.net/Macros#Using_a_variable_with_a_Macro
- https://app.roll20.net/forum/post/12261393/compare-the-values-of-a-role-to-a-variable-with-math-to-determine-a-success
- https://wiki.roll20.net/Reusing_Rolls
