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

<div>
