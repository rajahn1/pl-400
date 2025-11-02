# Otimizar o tempo de carregamento do aplicativo

- Ferramenta de revisao do Power Apps
- Cuidar, conexões, on visible, e on start

- Configurações -> Geral -> Depurar o Aplicativo Publicado
- Usar o Microsoft Azure Monitor para monitorar a performance do aplicativo
- É possível utilizar a função `Trace()` para monitorar os logs

- Navegar na inicialização do aplicativo: `App.StartScreen()`;
- Posso utilizar uma logica condicional para definir qual a primeira tela que vai aparecer para o usuario
dependendo dos valores dos campos
- Avaliar se é possivel trocar carregamentos do OnStart para OnVisible

- Associação direta de fonte de dados:
    Fazer um filtro em uma galeria se conectando diretamente com a fonte de dados, assim não terá aviso de delegração, 
    e os itens serão aparecidos conforme o usuário rolar pela galeria
- Utilizar Refresh(table) para atualizar os dados posteriormente

- Pré carregar dados em uma coleção para depois utilizar em uma galeria
- Utilizar LoadDate() para pre-carregar dados do dispostivo
- verificar se a coleção está vazia antes de re-carregar os dados