# Comparação Interativa do PIB dos Estados Brasileiros

Este projeto oferece uma ferramenta interativa para comparar a evolução do Produto Interno Bruto (PIB) de diferentes estados do Brasil ao longo do tempo. Utilizando bibliotecas como Pandas, NumPy, Matplotlib e Ipywidgets, os usuários podem selecionar anos de início e fim, além de dois estados para comparação, visualizando a evolução do PIB em um gráfico de linha e estatísticas comparativas em um gráfico de barras.

## Funcionalidades Principais

* **Seleção Interativa de Período:** Utilize sliders para definir o intervalo de anos para análise.
* **Comparação de Estados:** Escolha dois estados diferentes através de dropdowns para comparar seus PIBs.
* **Gráfico de Evolução do PIB:** Visualize a tendência do PIB dos dois estados selecionados ao longo do tempo em um gráfico de linha claro e informativo.
* **Gráfico de Estatísticas Comparativas:** Compare as estatísticas descritivas (Média, Mediana, Moda e Desvio Padrão) do PIB dos dois estados no período selecionado através de um gráfico de barras lado a lado.
* **Formatação de Valores:** Os valores do PIB são formatados de forma legível (em Bilhões ou Milhões) nos gráficos e nas anotações.
* **Exibição de Tabela de Estatísticas:** Abaixo dos gráficos, são exibidas tabelas com as estatísticas detalhadas para cada estado no período selecionado.
* **Mensagens de Erro:** O sistema inclui uma mensagem de erro caso o ano de início seja maior que o ano final.

## Bibliotecas Utilizadas

* **Pandas:** Para manipulação e análise de dados tabulares (carregar e filtrar os dados do PIB).
* **NumPy:** Para operações numéricas eficientes, especialmente na criação de arrays para os gráficos.
* **Matplotlib:** Para a criação de gráficos de linha (evolução do PIB) e de barras (estatísticas comparativas).
* **Ipywidgets:** Para criar os controles interativos (sliders e dropdowns) que permitem aos usuários personalizar a análise.
* **IPython.display:** Para exibir elementos HTML (como mensagens de erro formatadas) e os gráficos interativos no ambiente Jupyter.
* **scipy.stats:** Utilizado para o cálculo da moda estatística.

## Como Utilizar

1.  **Pré-requisitos:**
    * Python 3 instalado no seu sistema.
    * As seguintes bibliotecas Python instaladas (você pode instalá-las usando o `pip`):
        ```bash
        pip install pandas numpy matplotlib ipywidgets ipython scipy
        ```
    * Certifique-se de que você está executando o código em um ambiente Jupyter Notebook ou JupyterLab para aproveitar a interatividade dos widgets.

2.  **Executar o Notebook:**
    * Abra o arquivo `PIB dos Estados.ipynb` no Jupyter Notebook ou JupyterLab.
    * Execute as células de código em sequência.
    * Na última célula, você verá os widgets interativos (sliders para os anos e dropdowns para os estados).

3.  **Interagir com os Controles:**
    * **Ano Início:** Use o slider para selecionar o ano de início da análise.
    * **Ano Fim:** Use o slider para selecionar o ano de fim da análise. Certifique-se de que o ano de início não seja maior que o ano de fim.
    * **Estado 1:** Selecione o primeiro estado para comparação no dropdown.
    * **Estado 2:** Selecione o segundo estado para comparação no dropdown.

4.  **Visualizar os Resultados:**
    * Após selecionar os parâmetros desejados, o gráfico de evolução do PIB e o gráfico de estatísticas comparativas serão gerados e exibidos abaixo dos widgets.
    * As tabelas com as estatísticas detalhadas para cada estado no período selecionado também serão impressas.

## Estrutura do Projeto

O projeto consiste em um único arquivo Jupyter Notebook (`PIB dos Estados.ipynb`) que contém:

* **Importação de Bibliotecas:** As bibliotecas necessárias são importadas no início do notebook.
* **Carregamento de Dados:** (Assumindo que os dados são carregados no notebook).
* **Funções Auxiliares:**
    * `formatar_valor`: Formata os valores do PIB para exibição.
    * `calcular_estatisticas`: Calcula as estatísticas descritivas do PIB para um determinado conjunto de dados.
* **Função Principal (`plotar_comparacao`):**
    * Recebe os anos de início e fim, e os nomes dos dois estados como entrada.
    * Filtra os dados para o período e estados selecionados.
    * Calcula as estatísticas do PIB para cada estado.
    * Cria e exibe os gráficos de linha e de barras utilizando Matplotlib.
    * Exibe as tabelas de estatísticas utilizando Pandas.
* **Widgets Interativos:** Utiliza `ipywidgets.interact` para criar os controles interativos que chamam a função `plotar_comparacao` com os valores selecionados pelo usuário.

## Próximos Passos (Ideias para Melhorias)

* **Normalização do PIB:** Adicionar a opção de normalizar o PIB por algum fator (como população) para uma comparação mais justa.
* **Visualizações Adicionais:** Implementar outros tipos de gráficos, como box plots para comparar a distribuição do PIB.
* **Mais Estatísticas:** Incluir outras estatísticas relevantes na comparação.
* **Opção de Selecionar Mais Estados:** Permitir a comparação de mais de dois estados simultaneamente.
* **Exportação dos Gráficos:** Adicionar a funcionalidade de salvar os gráficos gerados.
* **Interface de Usuário Mais Elaborada:** Desenvolver uma interface de usuário mais completa utilizando bibliotecas como `streamlit` ou `dash`.

## Contribuição

Contribuições para este projeto são bem-vindas! Se você tiver ideias para melhorias, correções de bugs ou novas funcionalidades, sinta-se à vontade para abrir uma issue ou enviar um pull request.

