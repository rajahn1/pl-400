# Usar colunas de opção do Dataverse com fórmulas

- Quando os dados de uma opção são armazenados em uma linha do Dataverse, apenas o valor númerico
é armazenado, não o texto

## Opção Global vs Local 
- Opção global permite que os valores da opções sejam usadas em qualquer lugar do Dataverse
- Opção Local permite que seja usada somente na coluna criada da tabela em especifico
## Opção vs Pesquisa(LookUp)

- 

## Filtrar Colunas de Options com Power FX

- ex, filtrar clientes por categoria:
`Filter(
  Accounts,
  Category = 'Category (Accounts)'.'Preferred Customer'
)`

- Função `Choices`, mostrar as opções de um determinado campo Option, ex:
- `Choices(Accounts.Category)`

- Ao tentar filtrar dados por uma option selecionada especifica, irá ter problema de delegação
- Para contornar isso, podemos criar uma view, aplicando o filtro e depois só adicionar no Power Apps
- usar Views:
`Filter(
  Accounts,
  'Accounts (Views)'.'Monday Delivery'
)`

- podemos utilizar um formula `Switch` para controlar a cor do retangulo dos registros com base na opcao:
ex: `Switch(ThisItem.'Product visibility', chProductVisibility.Private, Color.Red, chProductVisibility.Public, Color.Green, chProductVisibility.Invite, Color.Blue, Color.Black)`


