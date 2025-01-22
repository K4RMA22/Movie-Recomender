# Movie-Recomender
# Sistema de Recomendação de Filmes

Este repositório contém um sistema de recomendação de filmes baseado em algoritmos de aprendizagem automática e análise de dados. O objetivo do projeto é criar um sistema interativo que sugira filmes com base em inputs fornecidos pelos utilizadores.

---

## Funcionalidades

- **Recomendações Baseadas em Títulos**: Permite ao utilizador introduzir títulos de filmes para obter recomendações semelhantes.
- **Desambiguação de Títulos**: Em casos de títulos ambíguos, o sistema solicita ao utilizador que selecione a opção correta.
- **Visualizações Gráficas**: Gráficos interativos que apresentam análises sobre géneros, popularidade e avaliações.
- **Treino de Modelos**: Inclui algoritmos como `SVD` para prever avaliações e `NearestNeighbors` para sugerir filmes semelhantes.
- **Interface Intuitiva**: Tabelas e inputs estilizados para uma melhor experiência de utilização.

---

## Estrutura do Repositório

- **`Projecto_Filmes.ipynb`**: O notebook principal contendo o código do sistema de recomendação e as análises gráficas.
- **`README.md`**: Este ficheiro, que documenta o projeto.

---

## Requisitos

Certifique-se de que tem as bibliotecas necessárias instaladas antes de executar o .ipynb.

### Bibliotecas

As seguintes bibliotecas que foram utilizadas:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `surprise`
- `IPython`

Pode instalar todas as dependências com o comando:
```
pip install pandas numpy matplotlib seaborn scikit-learn surprise
```

Como Utilizar
Clone este repositório:
```
git clone https://github.com/K4RMA22/Movie-Recomender.git
cd Movie-Recomender
```
Abra o notebook num ambiente como Google Colab, Jupyter Notebook ou VS Code.

# Execute as células sequencialmente para:

- Pré-processar os dados.
- Visualizar gráficos e análises.
- Treinar os modelos de recomendação.
- Interagir com o sistema para obter recomendações.

# Para casos de desambiguação de títulos:

O sistema exibirá opções para que escolha o filme pretendido.

# Análises Realizadas
**Análise Exploratória**
- Evolução Temporal de Filmes: Gráfico de linha que mostra a quantidade de filmes lançados ao longo dos anos.
- Contagem por Género: Gráfico de barras que apresenta a popularidade de cada género.
- Média de Avaliação por Género: Comparação das avaliações médias de diferentes géneros.
- Top 10 Filmes com Mais Votos: Lista dos filmes com maior número de votos no IMDb.
- Matriz de Correlação: Análise de correlação entre variáveis numéricas, como rating e votes.
# Modelagem
**Nearest Neighbors:**
- Recomendação de filmes semelhantes com base em características combinadas.
- Não depende de classificações fornecidas pelo utilizador.
**SVD:**
- Previsão de avaliações para títulos com base em padrões históricos.
- Permite comparação de métricas como RMSE e Precision@K.

# Exemplos de Utilização
**Entrada**
O utilizador pode introduzir títulos de filmes:

```
user_input = ['Inception', 'Avatar']
```
**Saída**
O sistema retorna uma tabela estilizada com recomendações relevantes.


# Métricas de Avaliação
**Precision@K:**
Mede a proporção de filmes relevantes entre os K primeiros recomendados.
Considerado relevante se o rating >= 6.0.
**RMSE (Root Mean Squared Error):**
Avalia a precisão do modelo SVD nas previsões de ratings.


# Resultados
**Nearest Neighbors:**
- Modelo mais adequado para recomendações baseadas em títulos, já que não requer input de ratings.
  
**SVD:**
- Útil para cenários onde dados de avaliações de utilizadores estão disponíveis.
- RMSE alcançado: 0.0615.

# Visualizações Disponíveis
**Gráficos Exploratórios:**
- Evolução temporal de filmes.
- Relação entre votos e ratings (escala logarítmica).
- Matriz de correlação.

**Gráficos de Recomendação:**
- Similaridade entre filmes recomendados (1 - distância).
- Distribuição de géneros entre recomendações.
