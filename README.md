# Análise de Dados sobre Vitórias e Poder Econômico no Futebol

## Autores
- **Willian Fernandes Vieira**  
- **Lucas Pinheiro Machado**  

Este estudo foi desenvolvido para a disciplina de **Gestão do Conhecimento e da Informação** no **CEFET**.

---

## 📌 Objetivo  
O objetivo desta análise é investigar a relação entre o poder econômico das equipes titulares e a frequência de vitórias nos campeonatos de futebol entre os anos de 2014 e 2024. A análise busca identificar se times com maior valor de mercado possuem uma vantagem significativa sobre seus adversários.

---

## 📊 Metodologia  

### **1. Coleta de Dados**  
Os dados foram extraídos de um arquivo CSV contendo informações sobre partidas de futebol. As colunas analisadas incluem:
- Ano do campeonato
- Data do jogo
- Time mandante e visitante
- Valor de mercado das equipes titulares
- Quantidade de gols marcados por cada equipe

### **2. Processamento e Limpeza de Dados**  
Foram aplicados os seguintes filtros e transformações:
- Seleção de partidas realizadas entre **2014 e 2024**
- Remoção de valores ausentes
- Multiplicação dos valores econômicos por **10.000** para ajuste de escala
- Identificação do **vencedor do jogo** (excluindo empates)
- Cálculo da **diferença econômica** entre as equipes

### **3. Análises Estatísticas**  
- **Correlação de Pearson e Spearman** para medir a relação entre valor econômico e número de vitórias  
- **Proporção de vitórias** de equipes com maior poder econômico  
- **Regressão linear** para verificar se a diferença econômica impacta a chance de vitória  

---

## 📈 Resultados

### **1. Correlação entre vitórias e vantagem econômica**
- **Correlação de Pearson**: **0.60** (p-valor: **2.51e-04**)  
- **Correlação de Spearman**: **0.40** (p-valor: **2.28e-02**)  

> 💡 Isso indica uma correlação moderada entre ter um maior valor econômico e vencer mais partidas.

### **2. Proporção de vitórias de times com maior valor econômico**
- **62.97%** das vitórias foram de times com maior valor econômico  

### **3. Modelo de Regressão Linear**
- **Intercepto**: **0.6446**  
- **Coeficiente da diferença econômica**: **5.36e-13**  
- **R² ajustado**: **0.062**  

> 🔍 Apesar de haver uma tendência de times mais valiosos vencerem, o modelo indica que a diferença econômica **não é o único fator determinante**.

---

## 📊 Visualizações

Foram gerados gráficos para melhor interpretar os resultados:

1. **Correlação entre número de vitórias e soma da diferença econômica**  
   ![Correlação](correlacao_vitorias_economia.png)
   
2. **Proporção de vitórias de times com maior valor econômico**  
   ![Proporção de Vitórias](proporcao_vitorias_economia.png)
   
3. **Distribuição da diferença econômica por resultado**  
   ![Boxplot Diferença Econômica](boxplot_diferenca_valores.png)

---

## 📌 Conclusão  
A análise sugere que times com maior poder econômico **tendem a vencer mais frequentemente**, mas essa vantagem **não é absoluta**. Outros fatores, como tática, preparo físico e desempenho em campo, também desempenham um papel essencial nas vitórias.

---

## 📝 Requisitos para Reproduzir a Análise  

Para executar a análise, é necessário ter **Python** instalado e as seguintes bibliotecas:

```bash
pip install pandas seaborn matplotlib scipy statsmodels numpy
