# 🏆 Portfólio de Projetos: Microsoft Certification Challenge #4 - DP-100 (DIO)

Este repositório contém os projetos práticos desenvolvidos como parte do **Microsoft Certification Challenge #4 (DP-100)** da **DIO (Digital Innovation One)**.

O objetivo principal é demonstrar proficiência na criação, gerenciamento e implantação de soluções de **Machine Learning (ML)** usando o **Azure Machine Learning** (referência principal para o exame DP-100) e ferramentas essenciais de MLOps, como o **MLflow**.

---

## 🎯 Sobre a Certificação DP-100

A certificação **DP-100: Designing and Implementing a Data Science Solution on Azure** valida a habilidade de cientistas de dados em aplicar os serviços do Azure Machine Learning para implementar e executar projetos de *data science*, desde a preparação dos dados até o *deployment* e monitoramento de modelos.

### Habilidades Demonstraas

* **Preparação e Análise de Dados:** Manipulação de dados com Pandas e NumPy.
* **Modelagem Preditiva:** Criação e treinamento de modelos de Regressão e Classificação com Scikit-learn.
* **MLOps (Machine Learning Operations):** Rastreamento de experimentos e registro de modelos usando **MLflow**.
* **Pipeline de ML:** Estruturação de código reprodutível para treinamento e teste.
* **Cloud Computing:** Simulação/documentação do *deployment* de modelos em ambientes como Azure Kubernetes Service (AKS).

---

## 📂 Projetos Desenvolvidos

Este repositório está estruturado em pastas numeradas, onde cada pasta corresponde a um projeto prático do desafio. Cada diretório contém seu próprio `README.md` detalhado sobre a implementação, resultados e *insights* específicos.

| # | Projeto | Objetivo Principal | Tecnologias Chave | Status |
| :--- | :--- | :--- | :--- | :--- |
| **01** | [Previsão de Vendas de Sorvete](01-previsao-vendas-sorvete/README.md) | Modelo de **Regressão** para prever vendas com base na temperatura. Foco em **MLflow**. | Python, Scikit-learn, MLflow, Regressão Linear. | **Em Andamento** |
| **02** | [Aguardando o Próximo Desafio] | [Breve objetivo do Projeto 2] | [Tecnologias do Projeto 2] | Pendente |
| **03** | [Aguardando o Último Desafio] | [Breve objetivo do Projeto 3] | [Tecnologias do Projeto 3] | Pendente |

---

## 🚀 Como Executar os Projetos

Para navegar e reproduzir os resultados de qualquer projeto, siga estas etapas básicas:

1.  **Clone o Repositório:**
    Utilize o comando `git clone` para baixar o repositório para sua máquina local.

    ```bash
    git clone [https://github.com/Cantalixto/dio-dp100-microsoft-certification.git](https://github.com/Cantalixto/dio-dp100-microsoft-certification.git)
    cd dio-dp100-microsoft-certification
    ```

2.  **Acesse a Pasta do Projeto:**
    Mude para o diretório do projeto que deseja explorar.

    ```bash
    cd 01-previsao-vendas-sorvete
    ```

3.  **Instale as Dependências:**
    Recomenda-se criar um ambiente virtual e instalar as bibliotecas necessárias (como `pandas`, `scikit-learn`, `mlflow`) usando o arquivo de requisitos do projeto.

    ```bash
    # Exemplo (se houver um requirements.txt dentro da pasta do projeto)
    pip install -r requirements.txt
    ```

4.  **Execute o Script de Treinamento:**
    Execute o arquivo principal (`train_model.py` na pasta `src/`) para treinar o modelo, gerar métricas e registrar a execução no MLflow.

---

## 🤝 Autor

| Detalhe | Informação |
| :--- | :--- |
| **Desenvolvedor** | **Núbia Cantalixto de Melo Alves** |
| **GitHub** | [@Cantalixto](https://github.com/Cantalixto) |
| **LinkedIn** | [Núbia Cantalixto de Melo Alves](https://www.linkedin.com/in/nubia-cantalixto-de-melo-alves/) |

*Este portfólio está em constante atualização. Ficarei feliz em receber feedback ou discutir os projetos!*
