# Busca A* para resolução de labirintos
Busca A* para resolução de labirintos em python, com função de plot e testes de performance.

A algoritmo A* decide qual caminho seguir baseado no custo de cada uma das células do labirinto e o algoritmo seleciona o caminho com custo mínimo. O custo de uma célula $n$ tem duas partes e é definido como:

![formula](https://render.githubusercontent.com/render/math?math=f(n)=g(n)%2Bh(n))

Onde ![formula](https://render.githubusercontent.com/render/math?math=f(n)) é o custo total para atingir a céula ![formula](https://render.githubusercontent.com/render/math?math=n) e ![formula](https://render.githubusercontent.com/render/math?math=g(n)) e ![formula](https://render.githubusercontent.com/render/math?math=h(n)) são definidos como:

![formula](https://render.githubusercontent.com/render/math?math=g(n)) É o custo real para alcançar a célula ![formula](https://render.githubusercontent.com/render/math?math=n) a partir da célula inicial.

![formula](https://render.githubusercontent.com/render/math?math=h(n)) É o custo heurístico para chegar à célula objetivo a partir da célula ![formula](https://render.githubusercontent.com/render/math?math=n). Seleção adequada da função heurística é um parâmetro-chave do algoritmo A*. Foi utilizada a distância de Manhattan como a função heurística:

![formula](https://render.githubusercontent.com/render/math?math=d(x%2Cy)%20%3D%20\sum_{i=1}^{n}\left|x_{i}-y_{i}\right|)

É a inclusão do custo Heurístico no algoritmo A* que o torna eficiente em comparação ao BFS ou DFS, pois o algoritmo seleciona as células com custo mínimo (custo real + custo estimado) e, portanto, se aproxima do objetivo rapidamente.

Exemplo de labirinto com 8x8 células gerado:

![Boxplot](labirinto.png)

Exemplo de labirinto resolvido:

![Boxplot](labirinto_sol.png)

Avaliação do algoritmo com 174 labirintos, 6 labirintos para cada dimensão que vão de  4×4  a  32×32  células:

![Boxplot](boxplot.png)

[Referência](https://levelup.gitconnected.com/a-star-a-search-for-solving-a-maze-using-python-with-visualization-b0cae1c3ba92) 
