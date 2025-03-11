<p align="center"> 
  <img src="./assets/img/machine-learning-logo.png" alt="Sorvetes" width="150" /> 
  <br /> 
  <b>Previsão de Vendas de Sorvetes</b> 
  <br /> 
  <sub><sup><b>(Projeto de Machine Learning)</b></sup></sub> 
  <br /> 
</p> 

<p align="center"> 
  Este projeto utiliza Machine Learning e o Microsoft Azure para prever a quantidade de vendas de sorvetes com base na temperatura ambiente. 
  <br /> 
</p>

---

## 🗃️ Estrutura do Projeto 

### Arquivos Principais
- `Sorvetes.ipynb`: Notebook Jupyter contendo o código para treinamento do modelo de Machine Learning.
- `vendas_sorvete.csv`: Arquivo CSV com os dados históricos de vendas de sorvetes e temperaturas.
- `src/vendas-sorvete.xlsx`: Arquivo com os dados da sorveteria, para usar como Data Asset dentro do Azure.

### Estrutura de Pastas

```
Previsão de Vendas de Sorvetes/
├── readme.md
└── ml_project/
    ├── Sorvetes.ipynb
    ├── vendas_sorvete.csv
    └── src/
        └── vendas_sorvete.xlsx
```

### ⚙️ Funcionalidades
- **Previsão de Vendas**: Utiliza um modelo de regressão linear para prever a quantidade de vendas de sorvetes com base na temperatura.
- **Treinamento no Azure**: O projeto inclui scripts em Python, em um arquivo Jupyter para treinar o modelo utilizando os serviços de Machine Learning do Microsoft Azure.

---
## 💬 Sobre o Projeto

### Contexto
O dono de uma sorveteria queria saber se era possível tentar prever a quantidade de vendas de sorvetes. Com a experiência, ele percebeu que em dias mais quentes, a quantidade de vendas aumentava, enquanto que em dias mais frios, diminuía.

Isso era um problema, em dias mais quentes, as vezes, o sorvete acabava e ele perdia algumas vendas. Enquanto que em dias frios, sobrava sorvete e ele perdia produção.

Então propus treinar um modelo de IA, utilizando a linguagem Python, Machine Learning e o Microsoft Azure. Então, usaríamos uma base de dados da sorveteria para treinar nosso modelo, baseado em algoritmo de regressão linear, para que fosse possível prever a quantidade de vendas de acordo com a temperatura ambiente.

### 🎯 Objetivo

Para solucionar esse problema, usamos Machine Learning e Azure para prever quantos sorvetes serão vendidos com base na temperatura. Com esse modelo, será possível antecipar a demanda e planejar a produção de maneira eficiente.

### Desafios a Serem Cumpridos 
- Prever a quantidade de vendas de sorvetes com base na temperatura.
- Treinar e validar o modelo utilizando os serviços de Machine Learning do Microsoft Azure.


### Base de Dados da Sorveteria 


| Data       | Temperatura (°C) | Vendas (Unidades) |
|------------|------------------|-------------------|
| 2024-12-01 | 11.2             | 21                |
| 2024-12-02 | 10.7             | 19                |
| 2024-12-03 | 12.5             | 24                |
| 2024-12-04 | 13.0             | 26                |
| 2024-12-05 | 13.5             | 27                |
| 2024-12-06 | 14.3             | 30                |
| 2024-12-07 | 14.7             | 31                |
| 2024-12-08 | 15.5             | 34                |
| 2024-12-09 | 15.9             | 35                |
| 2024-12-10 | 16.3             | 37                |
| 2024-12-11 | 17.1             | 39                |
| 2024-12-12 | 17.4             | 40                |
| 2024-12-13 | 17.9             | 42                |
| 2024-12-14 | 18.3             | 43                |
| 2024-12-15 | 18.7             | 44                |
| 2024-12-16 | 19.2             | 46                |
| 2024-12-17 | 19.6             | 47                |
| 2024-12-18 | 20.3             | 50                |
| 2024-12-19 | 20.7             | 51                |
| 2024-12-20 | 21.4             | 54                |
| 2024-12-21 | 21.9             | 56                |
| 2024-12-22 | 22.5             | 58                |
| 2024-12-23 | 22.8             | 59                |
| 2024-12-24 | 23.3             | 61                |
| 2024-12-25 | 23.7             | 62                |
| 2024-12-26 | 24.1             | 64                |
| 2024-12-27 | 24.7             | 66                |
| 2024-12-28 | 25.0             | 67                |
| 2024-12-29 | 25.6             | 69                |
| 2024-12-30 | 26.0             | 70                |
| 2024-12-31 | 26.4             | 72                |
| 2025-01-01 | 26.8             | 73                |
| 2025-01-02 | 27.3             | 75                |
| 2025-01-03 | 27.7             | 76                |
| 2025-01-04 | 28.1             | 78                |
| 2025-01-05 | 28.4             | 79                |
| 2025-01-06 | 28.9             | 81                |
| 2025-01-07 | 29.3             | 82                |
| 2025-01-08 | 29.7             | 84                |
| 2025-01-09 | 30.2             | 85                |
| 2025-01-10 | 30.6             | 87                |
| 2025-01-11 | 30.9             | 88                |
| 2025-01-12 | 31.3             | 89                |
| 2025-01-13 | 31.7             | 91                |
| 2025-01-14 | 32.1             | 92                |
| 2025-01-15 | 32.5             | 94                |
| 2025-01-16 | 32.9             | 95                |
| 2025-01-17 | 33.2             | 97                |
| 2025-01-18 | 33.6             | 98                |
| 2025-01-19 | 34.0             | 100               |
| 2025-01-20 | 34.4             | 101               |
| 2025-01-21 | 34.7             | 103               |
| 2025-01-22 | 35.0             | 104               |
| 2025-01-23 | 33.5             | 97                |
| 2025-01-24 | 32.2             | 93                |
| 2025-01-25 | 31.0             | 89                |
| 2025-01-26 | 29.5             | 83                |
| 2025-01-27 | 28.3             | 78                |
| 2025-01-28 | 27.1             | 74                |
| 2025-01-29 | 25.8             | 68                |
| 2025-01-30 | 24.6             | 63                |
| 2025-01-31 | 23.2             | 60                |
| 2025-02-01 | 21.8             | 55                |
| 2025-02-02 | 20.4             | 50                |
| 2025-02-03 | 19.1             | 45                |
| 2025-02-04 | 18.0             | 42                |
| 2025-02-05 | 16.8             | 38                |
| 2025-02-06 | 15.5             | 34                |
| 2025-02-07 | 14.3             | 30                |
| 2025-02-08 | 13.1             | 26                |
| 2025-02-09 | 11.9             | 22                |
| 2025-02-10 | 10.6             | 19                |
| 2025-02-11 | 12.3             | 23                |
| 2025-02-12 | 14.0             | 29                |
| 2025-02-13 | 16.0             | 36                |
| 2025-02-14 | 17.8             | 41                |
| 2025-02-15 | 19.6             | 47                |
| 2025-02-16 | 21.3             | 53                |
| 2025-02-17 | 23.1             | 60                |
| 2025-02-18 | 24.9             | 66                |
| 2025-02-19 | 26.7             | 73                |
| 2025-02-20 | 28.5             | 79                |
| 2025-02-21 | 30.3             | 86                |
| 2025-02-22 | 32.1             | 92                |
| 2025-02-23 | 33.9             | 99                |
| 2025-02-24 | 35.0             | 104               |
| 2025-02-25 | 34.5             | 102               |
| 2025-02-26 | 32.8             | 95                |
| 2025-02-27 | 31.1             | 90                |
| 2025-02-28 | 29.4             | 84                |
| 2025-03-01 | 27.6             | 77                |
| 2025-03-02 | 25.9             | 69                |
| 2025-03-03 | 24.2             | 62                |
| 2025-03-04 | 22.5             | 57                |
| 2025-03-05 | 20.8             | 51                |
| 2025-03-06 | 19.1             | 45                |
| 2025-03-07 | 17.4             | 40                |
| 2025-03-08 | 15.7             | 35                |
| 2025-03-09 | 14.0             | 29                |
| 2025-03-10 | 12.3             | 23                |

---

## 🔧 Configuração do Modelo no Azure Machine Learning

Este guia descreve passo a passo como configurar um modelo de Machine Learning utilizando o **Azure Machine Learning**, desde a criação do ambiente até o treinamento e avaliação com AutoML e Designer.

### 🖇️ Etapas de Configuração

#### 1. Criar Grupo de Recursos
- Acesse o portal do Azure.
- Crie um **grupo de recursos**.
- Nomeie e selecione a **região** desejada.

#### 2. Criar o Azure Machine Learning Workspace
- No grupo de recursos, crie um novo recurso do tipo **Azure Machine Learning**.
- Nomeie o workspace e mantenha a **mesma região**.
- Após criado, clique em **Launch** para abrir o estúdio.

#### 3. Enviar Projeto para o Workspace
- No estúdio, acesse a seção de arquivos.
- Crie uma nova pasta (se necessário).
- Envie a pasta `ml_project` contendo os scripts e o arquivo de base de dados.

#### 4. Criar Instância de Computação (Notebooks)
- Crie uma instância de computação para testes em notebooks.
- Nomeie e selecione o **tamanho da máquina virtual** apropriado.

#### 5. Criar Cluster de Computação (Treinamento)
- Crie um cluster dedicado com **CPU** (sem uso de GPU).
- Escolha o **tamanho da VM**, o **número de nós** e nomeie o cluster.

#### 6. Criar Data Asset
- Acesse a seção de **Data** e crie um novo asset.
- Nomeie, selecione o formato **Tabular**, e envie o arquivo:  
  `ml_project/src/vendas_sorvete.xlsx`.

#### 7. Verificar e Ajustar Dados
- Confirme que os dados foram processados corretamente.
- Desative o uso de **datas**, pois o modelo será baseado apenas na **temperatura** e **vendas**.

---

### 🤖 Criando o Modelo com AutoML

#### 8. Criar um AutoML Job
- Inicie um novo job AutoML.
- Nomeie o job e selecione o tipo: **Regression**.
- Selecione o **Data Asset** criado.
- Defina `vendas` como **target column**.
- Em **Additional Configuration**:
  - Desmarque todos os modelos, exceto **XGBoostRegressor**.
  - Configure os limites de tempo e iterações conforme necessário.
- Escolha o **cluster de computação** e submeta o job.

---

### 🧱 Criando um Pipeline com Designer

#### 9. Montar o Pipeline
1. **Dataset**  
   Selecione o dataset carregado.

2. **Select Columns in Dataset**  
   Selecione apenas as colunas `vendas` e `temperatura`.

3. **Split Data**  
   Configure `Fraction of rows in the first output dataset` como `0.8`.

4. **Train Model**  
   Defina a coluna `vendas` como label.

5. **Linear Regression**  
   Conecte ao módulo Train Model.

6. **Score Model**  
   Conecte ao Train Model e à saída de teste do Split Data.

7. **Evaluate Model**  
   Conecte ao Score Model.

#### 10. Submeter Pipeline
- Após montar o pipeline, clique em **Submit** para treinar e avaliar o modelo.

---

### ✅ Resultado Esperado

Ao final deste processo, você terá:
- Um modelo treinado com regressão (AutoML ou Designer).
- Métricas de avaliação para análise de performance.
- Ambiente Azure configurado para futuras execuções.

---

## Tecnologias e Ferramentas Utilizadas
- **Python**: Linguagem de programação utilizada para desenvolver o modelo.
- **Pandas e NumPy**: Bibliotecas para manipulação e análise de dados.
- **Scikit-Learn**: Biblioteca para construção e avaliação de modelos de Machine Learning.
- **Microsoft Azure**: Plataforma de nuvem utilizada para treinar e hospedar o modelo.

## Licença
Este software é licenciado sob os termos da MIT License.

---
<div align="center">

⌨️ Desenvolvido por [Vitor Bittencourt](https://github.com/vitorVBD) ☕

<div>#   m a c h i n e - l e a r n i n g - p a r a - p r e v e r - v e n d a s  
 #   m a c h i n e - l e a r n i n g - p a r a - p r e v e r - v e n d a s  
 