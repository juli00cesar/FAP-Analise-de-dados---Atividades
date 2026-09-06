# 📊 Projetos de Análise de Dados — FAP

Repositório destinado à organização de projetos, exercícios e estudos desenvolvidos durante a **Formação Acelerada em Programação (FAP)**, com foco em análise de dados, exploração de bases, estatística e construção de hipóteses.

---

## 🚦 Análise Exploratória de Dados — Acidentes nas Rodovias Federais | PRF 2025

### Sobre o projeto

Este projeto realiza uma **Análise Exploratória de Dados (EDA)** sobre acidentes registrados nas rodovias federais brasileiras em 2025, utilizando dados abertos da **Polícia Rodoviária Federal (PRF)**.

O objetivo é identificar padrões relacionados à ocorrência de **acidentes com vítimas fatais**, explorando diferenças entre estados, rodovias, causas, tipos de acidentes, períodos do dia e características da via.

### 🎯 Objetivo

Investigar quais características dos acidentes apresentam maior associação com a ocorrência de vítimas fatais, utilizando análises de frequência, rankings, proporções, cruzamentos entre variáveis e correlação.

### 🗂️ Base de dados

- **Fonte:** Dados Abertos da Polícia Rodoviária Federal — DATATRAN
- **Período:** 2025
- **Registros analisados:** 52.099 acidentes
- **Acidentes fatais:** 4.114
- **Taxa global de acidentes fatais:** aproximadamente 7,90%
- **Total de mortes:** 4.789
- **Total de vítimas:** 64.027

### 🔎 Variáveis analisadas

Entre as principais variáveis utilizadas estão:

- `uf`
- `br`
- `data_inversa`
- `dia_semana`
- `horario`
- `causa_acidente`
- `tipo_acidente`
- `classificacao_acidente`
- `fase_dia`
- `condicao_metereologica`
- `tipo_pista`
- `tracado_via`
- `uso_solo`
- `pessoas`
- `mortes`
- `feridos`
- `veiculos`

Também foram criadas variáveis derivadas para facilitar a análise, como o indicador de **acidente fatal** e o **total de vítimas**.

### 📈 Principais análises

#### Frequência e rankings

A análise de frequência permitiu identificar as UFs e rodovias com maior concentração de acidentes.

Entre as BRs com maior número de ocorrências destacam-se:

| Posição | BR | Acidentes |
|---|---|---:|
| 1º | BR-101 | 9.012 |
| 2º | BR-116 | 7.993 |
| 3º | BR-381 | 2.539 |
| 4º | BR-40 | 2.468 |
| 5º | BR-153 | 2.119 |

A análise também considera que **maior volume de acidentes não significa necessariamente maior proporção de acidentes fatais**.

#### Tipo de acidente

Os tipos de acidente com maiores proporções de fatalidade incluem principalmente:

- Atropelamento de Pedestre
- Colisão frontal
- Colisão lateral sentido oposto

Esses resultados indicam que determinados tipos de impacto apresentam associação mais forte com a ocorrência de vítimas fatais.

#### Causas dos acidentes

Entre as causas analisadas, destacam-se situações relacionadas a:

- circulação de pedestres na pista;
- entrada inopinada de pedestres;
- circulação na contramão;
- ultrapassagens indevidas;
- velocidade incompatível.

A análise diferencia **frequência absoluta** de **proporção de acidentes fatais**, evitando interpretar automaticamente as causas mais frequentes como as mais letais.

#### Fase do dia e condições contextuais

Os acidentes apresentam diferenças importantes conforme a fase do dia:

| Fase do dia | Registros | % fatais |
|---|---:|---:|
| Amanhecer | 2.627 | 11,34% |
| Plena Noite | 17.713 | 10,88% |
| Anoitecer | 2.834 | 7,27% |
| Pleno dia | 28.925 | 5,82% |

A taxa global utilizada como referência é de aproximadamente **7,89%**.

As condições de **Nevoeiro/Neblina** também apresentaram proporção superior à taxa global, enquanto categorias como Chuva, Garoa/Chuvisco e Sol ficaram abaixo dela.

#### Características estruturais

O tipo de pista apresentou uma diferença relevante:

| Tipo de pista | Registros | % fatais |
|---|---:|---:|
| Simples | 25.645 | 10,67% |
| Dupla | 21.539 | 5,33% |
| Múltipla | 4.915 | 4,68% |

Como hipótese exploratória, a menor separação entre os fluxos de tráfego em pistas simples pode estar relacionada à maior gravidade de determinados acidentes, especialmente colisões frontais.

### 🔗 Combinação de fatores

Os cruzamentos entre variáveis permitiram identificar padrões mais específicos.

Entre os principais resultados:

- **Amanhecer × pista simples:** 15,03% de acidentes fatais
- **Plena noite × pista simples:** 13,90%
- **Pedestre andava na pista × atropelamento de pedestre:** 45,61%
- **Transitar na contramão × colisão frontal:** 41,30%
- **Ultrapassagem indevida × colisão frontal:** 35,54%

Esses resultados reforçam a importância de analisar os fatores de maneira conjunta, e não apenas individualmente.

### 📊 Correlação

A análise de correlação foi utilizada para investigar relações lineares entre variáveis numéricas.

Um dos principais resultados foi a forte correlação entre **mortes e o indicador de acidente fatal**. Entretanto, essa relação deve ser interpretada como estrutural, pois a presença de mortes está diretamente relacionada à classificação do acidente como fatal.

Também foram observadas correlações relevantes entre variáveis que fazem parte da composição do número de pessoas e vítimas.

> **Correlação não significa causalidade.** Os resultados deste projeto representam associações exploratórias e não permitem afirmar que uma variável seja, isoladamente, responsável pela ocorrência de acidentes fatais.

### 💡 Principais hipóteses levantadas

A análise permitiu levantar hipóteses para investigações futuras:

1. **Menor luminosidade pode estar associada a maior proporção de acidentes fatais.**
2. **Pistas simples podem apresentar maior risco de acidentes de maior gravidade.**
3. **Atropelamentos e colisões frontais podem estar associados a maior letalidade.**
4. **A combinação de determinados comportamentos e tipos de acidente pode aumentar a gravidade das ocorrências.**
5. **Condições de baixa visibilidade podem estar relacionadas a acidentes mais graves.**

---

## 🧠 Módulo 2 — Levantamento de hipóteses

Uma das atividades do módulo trabalhou o desenvolvimento de hipóteses **antes da realização dos cálculos**, estimulando o raciocínio exploratório.

Foram considerados os seguintes fatores:

| Fator | Hipótese inicial |
|---|---|
| Causa do acidente | Determinadas causas podem provocar acidentes mais graves. |
| Tipo de acidente | Colisões frontais e atropelamentos podem apresentar maior letalidade. |
| Fase do dia | A baixa visibilidade e a sonolência podem aumentar o risco no período noturno. |
| Condição meteorológica | Chuva, neblina e outras condições adversas podem aumentar o risco. |
| Tipo de pista | Características diferentes de circulação podem influenciar a gravidade. |
| Traçado da via | Curvas, retas, aclives e declives podem apresentar diferentes níveis de risco. |

A atividade reforça uma etapa importante da análise de dados: **formular hipóteses antes de observar os resultados**, reduzindo a tendência de adaptar explicações aos dados depois de conhecê-los.

---

## 🛒 Módulo 2 — Análise de vendas e hipóteses de cancelamento/devolução

Outro exercício utilizou uma base de **200 vendas**, com informações sobre clientes, produtos, regiões, preços, descontos, formas de pagamento, status de entrega, avaliações e custos de envio.

### Variáveis principais

- Categoria
- Região / Estado
- Preço unitário
- Desconto
- Método de pagamento
- Custo de envio
- Status da entrega
- Avaliação do cliente

### Status das vendas

| Status | Quantidade |
|---|---:|
| Entregue | 185 |
| Cancelado | 6 |
| Devolvido | 4 |
| Em Trânsito | 5 |

### Hipóteses levantadas

- Diferentes categorias podem apresentar diferentes níveis de satisfação e problemas de qualidade.
- Formas de pagamento podem estar associadas a comportamentos diferentes de compra ou desistência.
- Região e estado podem influenciar a experiência logística.
- Produtos de maior valor podem gerar expectativas maiores.
- Descontos elevados podem estimular compras por impulso.
- Custos de envio elevados podem aumentar a possibilidade de desistência ou insatisfação.

O exercício teve como foco principal desenvolver o raciocínio de **hipótese → análise → evidência**, antes de interpretar os resultados.

---

## 🛠️ Ferramentas e tecnologias

As atividades deste repositório envolvem principalmente:

- **Excel / Google Sheets**
- **Python**
- **Pandas**
- **Google Colab**
- **SQL**
- **Git e GitHub**
- Estatística descritiva
- Análise exploratória de dados (EDA)
- Visualização de dados

---

## 📚 Metodologia

A análise dos dados da PRF segue uma abordagem de **Análise Exploratória de Dados (EDA)**, contemplando:

1. Compreensão do problema
2. Conhecimento e preparação da base
3. Análise de frequência
4. Rankings
5. Análise temporal
6. Análise bivariada
7. Combinação de fatores
8. Correlação
9. Formulação de hipóteses
10. Identificação de limitações

O projeto também utiliza princípios da metodologia **CRISP-DM**, especialmente nas etapas de compreensão do problema, preparação dos dados, exploração e interpretação dos resultados.

---

## ⚠️ Limitações

Os resultados devem ser interpretados dentro do contexto da base analisada. Entre as principais limitações estão:

- existência de registros com informações ignoradas ou ausentes;
- diferenças no volume de observações entre categorias;
- impossibilidade de estabelecer causalidade apenas por meio de análises exploratórias;
- possível relação entre algumas variáveis;
- correlações estruturais entre variáveis que fazem parte da definição dos indicadores.

Por isso, as conclusões apresentadas devem ser entendidas como **hipóteses e associações a serem investigadas**, e não como relações causais definitivas.

---

## 📁 Organização sugerida do repositório

```text
📦 projetos-aponti
├── 📂 excel
├── 📂 sql
├── 📂 python
├── 📂 dados
├── 📂 notebooks
├── 📂 dashboards
├── 📂 relatorios
├── 📂 apresentacao
└── README.md
```

---

## 👨‍💻 Sobre

Repositório desenvolvido durante a **4ª edição da Formação Acelerada em Programação (FAP)**, reunindo atividades práticas, exercícios e projetos voltados ao desenvolvimento de competências em análise de dados.

> **Transformando dados em informação, informação em conhecimento e conhecimento em decisões.**
