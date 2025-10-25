# 3. Confiabilidade

## 3.1 Introdução
A **confiabilidade** representa a capacidade de um software operar **de forma estável, precisa e contínua**, mesmo diante de condições adversas. Em sistemas como o **Guardiões da Saúde**, essa característica é importante para assegurar que os serviços funcionem corretamente.

Nesta etapa da análise, a confiabilidade é avaliada com base em aspectos como **disponibilidade, tolerância a falhas e maturidade**, buscando compreender em que medida o sistema mantém seu desempenho esperado ao longo do tempo.  

---

## 3.2 Objetivo GQM

<table>
  <tr><th>Analisar</th><td>o Guardiões da Saúde</td></tr>
  <tr><th>Para o propósito de</th><td>Entender</td></tr>
  <tr><th>Com respeito a</th><td>confiabilidade</td></tr>
  <tr><th>Do ponto de vista da</th><td>equipe de desenvolvimento</td></tr>
  <tr><th>No contexto da</th><td>disciplina de Qualidade de Software</td></tr>
</table>

<div align="center">
  <span style="font-size: 12px; font-style: italic;">
    Autor: <a href="https://github.com/MatheusHenrickSantos">Matheus Henrick</a>
  </span>
</div>

---

## 3.3 Questões
As questões definidas para uma característica visam direcionar a avaliação e verificar se o objetivo de medição está sendo atingido. Foram definidas com base nas subcaracterísticas selecionadas na Fase 1.

**Disponibilidade / Tolerância a Falhas / Maturidade**
<br>

**Q1.** O sistema está disponível para uso na maior parte do tempo?  
**Q2.** O sistema continua operando diante de falhas parciais sem queda total?  
**Q3.** O sistema apresenta baixa incidência de bugs que impactem a operação?

---

## 3.4 Hipóteses
As hipóteses representam **expectativas sobre o comportamento ideal do software** em relação às [questões formuladas](#33-questões).  
Elas orientam a interpretação dos resultados das medições e permitem comparar o desempenho real do sistema com o esperado, fornecendo base para o julgamento qualitativo.

<br>

- **H1:** A taxa de disponibilidade é ≥ 99% no período de observação.
- **H2:** Eventos de falha não resultam em indisponibilidade total; o sistema mantém ≥ 95% de sessões sem crash (Crash-Free Sessions). 
- **H3:** O rating de confiabilidade (baseado em bugs) é A, com ≤ 5 bugs abertos relevantes.

---

## 3.5 Métricas
As métricas foram selecionadas com base nas questões e [hipóteses propostas](#34-hipóteses), seguindo o princípio do GQM de alinhar cada medida a um objetivo claro.  

Essas métricas foram extraídas da ferramenta **SonarQube**, amplamente utilizada para avaliação automática de qualidade de código, e permitem quantificar fatores como **estabilidade, robustez e tolerância a falhas**.

M1.1 (Q1): Availability Rate (%) — proporção do tempo em que o sistema esteve funcional.
M2.1 (Q2): Erros sem queda (contagem) — falhas internas que não causam interrupção.
M2.2 (Q2): Erros com queda (contagem) — falhas que causam indisponibilidade total.
M3.1 (Q3): Reliability Rating (A–E) — classificação da estabilidade no SonarQube.
M3.2 (Q3): Bugs Count (por severidade) — contagem de erros críticos detectados.

---

## 3.6 Plano de Medição  
Cada métrica é associada a uma escala de valores que varia de *insuficiente* a *excelente*, permitindo avaliar o grau de atendimento das boas práticas de qualidade de software.

|   ID | Métrica                    | Tipo     | Escala   | Fonte de Coleta  | Ferramenta                    | Procedimento                                                           |
| ---: | -------------------------- | -------- | -------- | ---------------- | ----------------------------- | ---------------------------------------------------------------------- |
| M1.1 | Availability Rate (%)      | Direta   | Razão    | Monitoramento    | **Planilha de monitoramento** | Registrar manualmente períodos de indisponibilidade e calcular uptime. |
| M2.1 | Erros sem queda (contagem) | Direta   | Contagem | Logs de execução | **Registro manual**           | Registrar falhas observadas durante testes e execução normal.          |
| M2.2 | Erros com queda (contagem) | Direta   | Contagem | Logs de execução | **Registro manual**           | Contar falhas que causam interrupção do sistema.                       |
| M3.1 | Reliability Rating (A–E)   | Indireta | Ordinal  | Código-fonte     | **SonarQube**                 | Realizar análise estática e registrar o rating.                        |
| M3.2 | Bugs Count                 | Indireta | Contagem | SonarQube        | **SonarQube**                 | Coletar quantidade de bugs críticos detectados.                        |


---

## 3.7 Níveis de Pontuação e Critérios de Julgamento
A tabela GQM consolida as relações entre **objetivos, questões, métricas, fontes de dados e periodicidade de coleta**.  
Essa visão integrada facilita o acompanhamento das medições e a verificação contínua da qualidade, garantindo que as decisões sejam tomadas com base em evidências quantitativas e consistentes.

|   ID | Métrica               | Insuficiente | Satisfatório | Bom    | Excelente           |
| ---: | --------------------- | ------------ | ------------ | ------ | ------------------- |
| M1.1 | Availability Rate (%) | < 95%        | 95–97%       | 97–99% | ≥ 99%               |
| M2.1 | Erros sem queda       | 0            | 1–3          | 4–7    | > 7                 |
| M2.2 | Erros com queda       | > 5          | 4–5          | 2–3    | 0–1                 |
| M3.1 | Reliability Rating    | C–E          | B            | A      | A sem bugs críticos |
| M3.2 | Bugs Count            | > 15         | 6–15         | 1–5    | 0                   |


---

## 3.8 Tabela GQM
| Objetivo                                        | Questão | Métrica                        | Fonte         | Periodicidade | Alvo            |
| ----------------------------------------------- | ------- | ------------------------------ | ------------- | ------------- | --------------- |
| Entender a confiabilidade do Guardiões da Saúde | Q1      | Availability Rate (%)          | Monitoramento | Mensal        | ≥ 99%           |
|                                                 | Q2      | Erros sem queda / com queda    | Logs          | Mensal        | ≥ 95% sem queda |
|                                                 | Q3      | Reliability Rating; Bugs Count | SonarQube     | Mensal        | A + ≤ 5 bugs    |

---

## 3.9 Diagrama GQM

```mermaid
graph TD
G(G1: Entender a Confiabilidade)
  G --> Q1(Q1: Disponibilidade?)
  G --> Q2(Q2: Tolerância a falhas?)
  G --> Q3(Q3: Maturidade?)

  Q1 --> M1_1(M1.1: Availability Rate (%))

  Q2 --> M2_1(M2.1: Crash-Free Sessions (%))
  Q2 --> M2_2(M2.2: Erros sem queda - ratio)

  Q3 --> M3_1(M3.1: Reliability Rating (A–E))
  Q3 --> M3_2(M3.2: Incidentes P0/P1)

<div align="center"> <span style="font-size: 12px; font-style: italic;"> Autor: <a href="https://github.com/uires2023">Uires Carlos</a> </span> </div> ```

---

## 3.10 Referências

> BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, Hans Dieter. *The Goal Question Metric (GQM) Approach.* In: MARCINIAK, J. J. (ed.). *Encyclopedia of Software Engineering.* New York: John Wiley & Sons, 1994. cap. 6, p. 51–55.  
> INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. *ISO/IEC 25023:2011.* Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models. Genebra: ISO, 2011.

---

## 3.11 Histórico de Versões

| Versão | Data | Descrição | Autor(es) |
|--------|------|------------|------------|
| `1.0` | 14/10/2025 | Criação do documento | [Uires Carlos de Oliveira](https://github.com/uires2023), [Matheus Henrick](https://github.com/MatheusHenrickSantos) |
| `1.1` | 15/10/2025 | Formatação do texto, remoção de informações redundantes | [Gabriela Tiago](https://github.com/GabrielaTiago) |
| `1.2` | 24/10/2025 | Reestruturação do artefato, adição da introdução e dos links de navegação | [Arthur Carneiro](https://github.com/trindadea) |
| `1.3` | 25/10/2025 | Ajuste dos itens 2.2 - 3.2 - 4.2 (propósitos somente o verbo no infinitivo) | [Uires Carlos de Oliveira](https://github.com/uires2023) |
| `1.4` | 25/10/2025 | Revisão Confiabilidade | [Uires Carlos de Oliveira](https://github.com/uires2023) |
