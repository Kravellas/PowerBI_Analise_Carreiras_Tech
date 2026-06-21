# Projeto Final: Análise de Fatores de Valorização Salarial em Tecnologia (carreiras_tech)

## 1. Descrição do Projeto e Problema de Negócio Resumido

Este projeto foi desenvolvido para a disciplina de Business Intelligence II com o objetivo de integrar os conceitos de modelagem dimensional, transformações em Power Query, cálculos em linguagem DAX, Row-Level Security (RLS) e versionamento em formato de código aberto (.pbip).

A solução atua no domínio corporativo de People Analytics para responder de forma quantitativa e visual à pergunta central: **"What Factors Increase Salary?" (Quais fatores aumentam o salário?)**. O escopo abrange a identificação das competências técnicas (primary_skill), cargos e níveis de experiência com maior impacto na folha salarial. Adicionalmente, audita a distribuição demográfica e investiga disparidades salariais e de representatividade entre gêneros para subsidiar decisões estratégicas de contratação, remuneração isonômica e mitigação de picos de esforço que geram turnover voluntário.

---

## 2. Principais Indicadores-Chave de Desempenho (KPIs)

O modelo calcula de forma automatizada os seguintes indicadores analíticos estruturados na documentação do projeto:

* **KPI 1: Prêmio Salarial por Habilidade (Skill Premium Score)** Fórmula: `((Média Salarial com a Skill X - Média Salarial sem a Skill X) / Média Salarial sem a Skill X) * 100`  
  Objetivo: Isolar o valor percentual que o mercado adiciona à remuneração por competências específicas.
* **KPI 2: Disparidade Salarial de Gênero (Gender Pay Gap)** Fórmula: `((Média Salarial Homens - Média Salarial Mulheres) / Média Salarial Homens) * 100`  
  Objetivo: Identificar desvios de equidade salarial global e por segmento profissional.
* **KPI 3: Representatividade Feminina em Cargos Avançados (Senior Gender Ratio)** Fórmula: `(Nº Mulheres em Liderança ou Sênior / Total de Profissionais em Liderança ou Sênior) * 100`  
  Objetivo: Diagnosticar se as variações de médias gerais decorrem de barreiras hierárquicas (teto de vidro).
* **KPI 4: Fator de Valorização por Senioridade (Experience Leverage Factor)** Fórmula: `Média Salarial Nível Sênior / Média Salarial Nível Júnior`  
  Objetivo: Mensurar o multiplicador financeiro gerado pelo tempo de carreira e senioridade na área.
* **KPI 5: Índice de Relevância de Cargo (Job Salary Index)** Fórmula: `Média Salarial do Cargo X / Média Salarial Geral do Dataset`  
  Objetivo: Identificar quais funções operam acima ou abaixo da média salarial geral do mercado tecnológico.

---

## 3. Origem e Link do Dataset Utilizado

Os dados reais utilizados nesta solução foram extraídos de fonte pública, íntegra e auditável, em estrita conformidade com os requisitos da disciplina.
* **Link de Acesso ao Dataset:** [Inserir o link direto do Kaggle, Hugging Face ou Portal Oficial escolhido pela dupla]
* **Documentação de Origem:** Os metadados, licenças de uso e o dicionário de dados detalhado encontram-se registrados no arquivo local localizado em `[data/README.md](https://www.kaggle.com/datasets/mabubakrsiddiq/salary-and-skills-ds-what-factors-increases-salary)`.

---

## 4. Estrutura do Reposiório GitHub

O repositório foi organizado exatamente conforme a árvore de diretórios sugerida na Seção 4.8 do edital, segregando os artefatos de documentação, dados brutos, arquivos de metadados do Power BI e apresentação executiva:

```text
.
├── README.md                           # Este arquivo de documentação principal do projeto
├── docs/
│   ├── problema_de_negocio.md          # Contextualização do cenário e stakeholders (máx. 2 páginas)
│   ├── kpis_okrs.md                    # Definições analíticas e Matriz de Rastreabilidade Estratégica
│   ├── modelo_dimensional.png          # Diagrama visual do Star Schema implementado
│   └── decisoes_de_modelagem.md        # Justificativa técnica de granularidade, tabelas fato e dimensões
├── data/
│   └── README.md                       # Explicação detalhada da origem, link e licença do dataset real
├── pbip/
│   ├── carreiras_tech.pbip             # Arquivo raiz do projeto salvo em formato Power BI Project
│   ├── carreiras_tech.Dataset/         # Pasta contendo o modelo de dados e definições de tabelas (BIM/TMDL)
│   └── carreiras_tech.Report/          # Pasta contendo os metadados visuais das páginas e layouts do relatório
└── apresentacao/
    └── slides.pdf                      # Arquivo PDF contendo os slides da apresentação executiva corporativa