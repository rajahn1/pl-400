# Realizar testes e verificações de desempenho em um aplicativo de tela do Power Apps

- Maior gargalo é a fonte de dados
- Usar LookUp em um rótulo de uma galeria, ideal é já ter uma coleção com os LookUps
- Usar Azure Blobs para armazenar imagens
- Armazenar fonte de dados em Collection para ter o Cache
- Usar Concurrent para carregar dados ao mesmo tempo
- Fórmula para medir o tempo de execução do carregamento de uma fonte de dados:
  `Reset(Timer1);
UpdateContext({StartTimer: true});
Refresh('Workout tracker');
ClearCollect(colWorkoutTracker, Filter('Workout tracker', Status = "Active"));
UpdateContext({StartTimer: false})`
