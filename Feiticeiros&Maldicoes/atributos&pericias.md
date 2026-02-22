
# Atributos derivados base

Usam valor(es) determinado(s) pelo jogador para serem calculados

## Modificadores

mod_atributo
```rmacro
[[floor((@{atributo}-10)/2)]]
```

## Proficiência

proficiencia_bonus
```rmacro
[[floor((@{nivel}-1)/4) + 2]]
```

# Atributos derivados secundários

Usam ao menos um atributo derivado base em seu cálculo

## Vida

Essa vida não conta multiclasse e rodar dado quando subindo de nível. O 1+@{nivel} é para cobrir o extra de vida no primeiro nível.
Se quiser inserir valores de dados rodados, só incluir o modificador relativo ao vidaPorNivel no outros_vida

vida
```rmacro
[[((1+@{nivel})*@{vidaPorNivel})[Vida da classe] + (@{nivel}*@{mod_constituicao})[Bônus de Constituição] + @{outros_vida}[Outros bônus] ]]
```

## Energia Amaldiçoada

Essa energia não conta multiclasse.

energia
```rmacro
[[((@{nivel})*@{energiaPorNivel})[Energia da classe] + ({{@{selected|classe}, 0}=3}*@{tecnica_atributo})[Energia inicial] + @{outros_energia}[Outros bônus] ]]
```

## Defesa

```rmacro
[[10 + @{mod_destreza} + @{outros_defesa}]]
```

## Perícias

