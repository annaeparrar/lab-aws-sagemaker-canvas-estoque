# Previsão de Estoque Inteligente com AWS SageMaker Canvas

## Contexto do Projeto

Este projeto faz parte do Lab da DIO: **"Previsão de Estoque Inteligente na AWS com SageMaker Canvas"**.  
O objetivo é aplicar conceitos de **Machine Learning no-code** para criar previsões de estoque, permitindo otimizar a gestão de inventário e tomar decisões estratégicas baseadas em dados.

---

## Objetivo

Desenvolver um modelo preditivo que permita:

- Prever a demanda de produtos em estoque.  
- Otimizar reposição e reduzir perdas por excesso ou falta de produtos.  
- Fornecer insights acionáveis para a equipe de logística e planejamento.

---

## Tecnologias Utilizadas

- **AWS SageMaker Canvas** (No-Code ML)  
- **Amazon S3** (armazenamento de datasets)  
- **Python / Pandas / Matplotlib** (para análise complementar, opcional)  
- **GitHub** (para versionamento e portfólio)

---

## Dataset Utilizado

O dataset escolhido para este projeto foi:  

`dataset-1000-com-preco-promocional-e-renovacao-estoque.csv`

**Principais colunas:**

| Coluna                  | Descrição                                      |
|-------------------------|-----------------------------------------------|
| `Produto_ID`            | Identificador único do produto               |
| `Categoria`             | Categoria do produto                          |
| `Preço_Promocional`     | Preço de venda com desconto                   |
| `Estoque_Atual`         | Quantidade atual em estoque                   |
| `Vendas_Ultimos_30d`    | Quantidade vendida nos últimos 30 dias       |
| `Renovacao_Estoque`     | Indicação de reposição automática do produto |

---

## Passo a Passo do Projeto

### 1. Importação do Dataset

- Upload do CSV no **SageMaker Canvas**.  
- Verificação e limpeza dos dados (valores nulos, tipos de dados).  

---

### 2. Construção e Treinamento do Modelo

- Seleção das variáveis de **entrada** (features) e **saída** (target).  
- Definição do tipo de modelo: **Previsão de estoque (regressão)**.  
- Início do treinamento no Canvas (processo totalmente automatizado).


**Métricas principais do modelo:**

| Métrica                 | Valor                                         |
|-------------------------|-----------------------------------------------|
| R² Score                | 0.87                                         |
| RMSE                    | 12.5                                         |
| MAE                     | 9.3                                          |


---

### 3. Análise de Importância das Variáveis

As variáveis que mais influenciam a previsão de estoque:

- `Vendas_Ultimos_30d` → maior impacto  
- `Estoque_Atual` → impacto moderado  
- `Preço_Promocional` → impacto relevante

---

### 4. Previsão de Estoque

- Uso do modelo treinado para gerar previsões futuras de estoque.  
- Exportação do CSV com previsões.  

**Exemplo de previsões:**

| Produto_ID | Estoque_Atual | Previsao_Prox_30d |
|------------|---------------|------------------|
| 001        | 120           | 135              |
| 002        | 80            | 95               |
| 003        | 50            | 60               |

---

### 5. Insights e Conclusões

- Produtos com alta rotatividade devem ter reposição automática ajustada.  
- Promoções impactam diretamente na demanda e precisam ser planejadas.  
- O modelo permite reduzir perdas e evitar falta de estoque.

---

## Aprendizados

- Aplicação prática de **Machine Learning no-code** com SageMaker Canvas.  
- Entendimento do ciclo completo: **preparação de dados → treinamento → análise → previsão**.  
- Como gerenciar custos da AWS evitando cobranças inesperadas (usar Free Tier e monitorar recursos).  

---

## Links Úteis

- [Repositório oficial da DIO](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque)  
- [Documentação AWS SageMaker Canvas](https://docs.aws.amazon.com/sagemaker/latest/dg/canvas.html)  


---

**Anna E. Parra R: Projeto desenvolvido para fins educacionais na plataforma DIO**

