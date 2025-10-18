# Trabalhar com dados relacionais em um aplicativo de tela do Power Apps

## Estabelecer relacoes entre dados distintos

- exemplo, tenho uma tabela com visitas da viagem por cidade, algumas informações se repetem, e outras não
- criar uma tabela para as informações que se repetem, unificando os registros.
- informações que são distintas, criar outra tabela, depois relacionar para o ID da primeira tabela
- utilizar a função LookUp para navegar de cima para baixo ou de baixo para cima, no caso de uma tabela pai e uma tabela filho
- ex: tabela pai cliente, tabela filho fatura que tem uma referencia para cliente, utilizo LookUp para saber qual o cliente
ao acessar a tabela Fatura
- `LookUp(Customer; CustomerId = RegistroFatura.CustomerID)`
- prestar atenção pois isso pode exige alta performance do App, afetando o desempenho
- verificar a quantidade de registros antes de utilizar esta abordagem, e verificar a opção de se utilizar um cache
- utilizar coleções locais 

* Se estiver utilizando o DataVerse, é mais interessante primeiro fazer a relação nas tabelas,
assim irá diminuir o nivel do desempenho



