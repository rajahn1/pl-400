# DECLARAÇÃO IMPERATIVA X DECLARATIVA

## Tipos de Variáveis
- Variáveis são temporárias, quando fecha o App os valores são perdidos

### Global
- Disponível no App inteiro, utilizando *Set*

### De Contexto
- Disponível apenas na tela em que você a cria
- posso ter duas variáveis com o mesmo nome em telas diferentes, não vao ter os mesmos valores
- é possível declarar mais de uma variável por vez
- `UpdateContext({})`

### Coleções
- Armazenar tabela de dados
- ideal para armazenar dados de uma fonte de dados que você vai utilizar várias vezes, para diminuir o custo de chamar
sempre da fonte de dados
- não delegável, apenas 500 registros da coleção serão recuperados
- também é possível criar coleções customizadas para popular dados
**User()** - Recupera as informações do usuário diretamente do Azure Active Directory

- usar a propriedade OnVisible para armazenar condições atráves do Set

- Variáveis podem ter autoreferência
- uma váriavel só pode armazenar UM registro
- teste
