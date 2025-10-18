# Executar atualizações personalizadas em um aplicativo de tela do Power Apps

## Função Patch

- Criar e editar um registro diretamente, quand voce nao quer usar um formulario

- ex: `Patch(CustomerOrders, Defaults(CustomerOrders), {Region: "Americas", Country: "Canada"})`
- nao é necessário setar o ID, função Defaults seta os valores defaults das colunas na hora da criação
- para editar um registro, utilizar a função `LookUp` para pegar o valor
- ex: `Patch(CustomerOrders, LookUP(CustomerOrders, ID = 1), {Region: "Asia", Country: "China"})`


## Funções de Remoção

- Remove
- RemoveIf
- Clear - remove todos os registros de uma colecao
- Alteraçoes em massa: utilizar uma funcao ForAll
- Tambem é possível utilizar essas funções em coleções
- * Funcao remove nao solicita confirmacao, entao eh ideal criar um PopUp antes da exclusao do registro

- Para excluir mais de UM registro com base em uma condicao, podemos usar RemoveIf:
- `RemoveIf(CustomerOrders, Status = "Expired")`
- Para excluir TODOS os registros:
- `RemoveIf(CustomerOrders, true)`
- obs: podemos utilizar filter para definir o "true" no RemoveIf


