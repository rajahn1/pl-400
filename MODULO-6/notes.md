# Trabalhar com limites de fonte de dados (limites de delegação) em um aplicativo de tela do Power Apps


## Delegação
- Delegação, exemplo, sharepoint tem 5000 registros de projetos, voce utiliza um função filter,
par apegar apenas os projetos ativos, vai pegar 2500 projetos, neste caso a função filter é delegável,
que vai mandar um Power FX para o Sharepoint e retornar somente os 2500 registros. Power Apps não 
processou nenhum dados e somente os dados requisitados foram mandados para o Power Apps

- Numeros com operacoes aritmetticas nao sao delegaveis, assim como idioma e fuso horario
- cada fonte de dados tem suas funcoes especificas em relacao a delegacao (Sharepoint, SQL)

## Funcoes Nao Delegaveis

`First, FirstN, Last, LastN

    Choices

    Concat

    Collect, ClearCollect (nenhuma dessas funções retorna um aviso de delegação, mas elas não são delegáveis)

    CountIf, RemoveIf, UpdateIf

    GroupBy, Ungroup`


- Utilizar `AddColumns` e `LookUp` para juntar informações em uma fonte de dados

## 	Ao combinar funções delegáveis e não delegáveis em uma fórmula, o que acontece?

- As funções delegáveis podem se tornar não delegáveis reduzindo a quantidade de dados retornados pela fórmula




