# Fatores Salariais em Tecnologia

> **Pergunta Central:** *Quais fatores (habilidades, experiência, gênero, localização) realmente aumentam o salário no mercado de tecnologia?*

## Sobre o Projeto

Este projeto de **Business Intelligence e People Analytics** foi desenvolvido com o objetivo de mapear e quantificar os fatores que influenciam a remuneração de profissionais de tecnologia. 

Através da análise de um dataset complexo, o modelo investiga não apenas o prêmio salarial gerado por competências técnicas (Skills), mas também realiza uma auditoria demográfica profunda para identificar possíveis disparidades salariais de gênero (Gender Pay Gap) e o impacto de modelos de trabalho na retenção de talentos.

---

## Tecnologias e Técnicas Aplicadas

Para entregar um modelo robusto, escalável e alinhado às melhores práticas de governança de dados, foram aplicadas as seguintes técnicas:

* **ETL (Power Query):** Limpeza de dados, tratamento de colunas multivaloradas (skills delimitadas por ponto e vírgula) e criação de Surrogate Keys numéricas.
* **Modelagem Dimensional (Star Schema):** Estruturação do modelo em Fato (`fato_skills`) e Dimensões temáticas (`dim_employee`, `dim_job`, etc.) para otimização do motor VertiPaq.
* **Linguagem DAX Avançada:** Criação de mais de 12 medidas explícitas, utilizando modificadores de contexto (`CALCULATE`, `ALL`, `ALLSELECTED`) e funções de Time Intelligence (`TOTALYTD`, `SAMEPERIODLASTYEAR`).
* **Governança e Segurança (RLS):** Implementação de *Row-Level Security* para restringir o acesso aos dados salariais com base em papéis de negócios (ex: *Gestor de Backend*, *Recrutador Índia*).
* **Versionamento:** O projeto está salvo no formato `.pbip` (Power BI Project), permitindo versionamento de código e colaboração otimizada via Git.

---

## Estrutura do Repositório

O repositório está organizado utilizando o padrão ouro para projetos de dados:

* 📁 **`docs/`**: Documentação técnica detalhada do projeto.
  * [`problema_de_negocio.md`](docs/problema_de_negocio.md) - Contexto e perguntas de negócio.
  * [`kpis_okrs.md`](docs/kpis_okrs.md) - Matriz de rastreabilidade (Fórmulas e Metas).
  * [`decisoes_de_modelagem.md`](docs/decisoes_de_modelagem.md) - Arquitetura de dados e esquema em estrela.
* 📁 **`data/`**: Informações sobre a origem dos dados (Dataset).
* 📁 **`pbip/`**: Código-fonte estruturado do painel do Power BI.
* 📁 **`apresentacao/`**: Slides com o resumo executivo dos *insights* gerados.

