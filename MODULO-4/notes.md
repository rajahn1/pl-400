# Reduzir a complexidade no modelo de dados com os relacionamentos de tabela do Dataverse

## Relacionamento um Para Muitos

- Um Local -> Varias Mesas 
- Função `Relate` e `Unrelate`

## Relacionamento Muito para Muitos

- Muitas mesas podem ter muitos recursos de mesa
- Para mostrar mais de um valor, podemos utilizar a funcao Concat da seguinte forma:
- `Concat(ThisItem.'Desk Features', Name, ",")`


