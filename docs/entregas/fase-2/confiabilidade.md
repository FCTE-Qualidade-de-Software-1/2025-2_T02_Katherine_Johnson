# 3. Confiabilidade

## 3.1 Introdução
A **confiabilidade** representa a capacidade de um software operar **de forma estável, precisa e contínua**, mesmo diante de condições adversas. Em sistemas como o **Guardiões da Saúde**, essa característica é importante para assegurar que os serviços funcionem corretamente.

Nesta etapa da análise, a confiabilidade é avaliada com base em aspectos como **estabilidade, disponibilidade, tolerância a falhas e recuperação de erros**, buscando compreender em que medida o sistema mantém seu desempenho esperado ao longo do tempo.  

---

## 3.2 Objetivo GQM

<table>
  <tr><th>Analisar</th><td>o Guardiões da Saúde</td></tr>
  <tr><th>Para o propósito de</th><td>entender o nível de confiança do software em operar corretamente e de forma estável</td></tr>
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
As questões definidas para uma característica visam direcionar a avaliação e verificar se o objetivo de medição está sendo atingido. 

<br>

**Q1.** O sistema está disponível para uso na maior parte do tempo?  
**Q2.** O sistema consegue continuar operando mesmo diante de falhas pontuais?  
**Q3.** O sistema consegue se recuperar rapidamente após uma falha?

---

## 3.4 Hipóteses
As hipóteses representam **expectativas sobre o comportamento ideal do software** em relação às [questões formuladas](#33-questões).  
Elas orientam a interpretação dos resultados das medições e permitem comparar o desempenho real do sistema com o esperado, fornecendo base para o julgamento qualitativo.

<br>

- **H1:** O sistema está disponível durante 99% do tempo de operação, com interrupções mínimas e planejadas.  
- **H2:** O sistema possui mecanismos de tolerância a falhas que evitam interrupções totais.  
- **H3:** O tempo médio de recuperação é inferior a 5 minutos em falhas comuns, com processos automatizados de restauração.

---

## 3.5 Métricas
As métricas foram selecionadas com base nas questões e [hipóteses propostas](#34-hipóteses), seguindo o princípio do GQM de alinhar cada medida a um objetivo claro.  

Essas métricas foram extraídas da ferramenta **SonarQube**, amplamente utilizada para avaliação automática de qualidade de código, e permitem quantificar fatores como **estabilidade, robustez e tolerância a falhas**.

| Nível | Elemento |
|-------|-----------|
| **Goal** | Analisar o código-fonte do Guardiões da Saúde com o propósito de **entender a confiabilidade do software**, com respeito à ocorrência de falhas e robustez do sistema, do ponto de vista dos desenvolvedores e analistas de qualidade. |
| **Questão 1** | O sistema apresenta _bugs_ que comprometem sua execução? |
| **Métrica 1** | _Reliability Rating (A–E)_ – SonarQube (baseado em número de _bugs_). |
| **Hipótese 1** | Espera-se _Reliability Rating = A_, indicando ausência de falhas críticas. |
| **Questão 2** | Existem vulnerabilidades que afetam a confiabilidade do sistema? |
| **Métrica 2** | _Security Rating (A–E)_ – SonarQube. |
| **Hipótese 2** | Espera-se _Security Rating = A_. |
| **Questão 3** | Há "_code smells_" que possam levar a falhas futuras? |
| **Métrica 3** | _Number of Code Smells_ e _Maintainability Rating (A–E)_. |
| **Hipótese 3** | Espera-se _Maintainability Rating = A_ e menos de 50 _code smells_. |

<div align="center">
  <span style="font-size: 12px; font-style: italic;">
    Autor: <a href="https://github.com/uires2023">Uires Carlos de Oliveira</a>
  </span>
</div>

---

## 3.6 Níveis de Pontuação e Critérios de Julgamento
Os **níveis de pontuação** foram definidos para possibilitar uma **interpretação padronizada dos resultados** das [medições](#35-métricas).  
Cada métrica é associada a uma escala de valores que varia de *insuficiente* a *excelente*, permitindo avaliar o grau de atendimento das boas práticas de qualidade de software.

| Métrica | Insuficiente | Satisfatório | Bom | Excelente |
|----------|---------------|--------------|------|------------|
| _Reliability Rating_ | D–E | C | B | A |
| _Security Rating_ | D–E | C | B | A |
| _Maintainability Rating_ | D–E | C | B | A |
| _Code Smells (quantidade)_ | > 100 | 51–100 | 26–50 | ≤ 25 |

---

## 3.7 Tabela GQM – Confiabilidade
A tabela GQM consolida as relações entre **objetivos, questões, métricas, fontes de dados e periodicidade de coleta**.  
Essa visão integrada facilita o acompanhamento das medições e a verificação contínua da qualidade, garantindo que as decisões sejam tomadas com base em evidências quantitativas e consistentes.

| Objetivo | Questão | Métrica | Fonte | Periodicidade | Alvo |
|-----------|----------|----------|--------|----------------|------|
| Entender o nível de confiança do software em operar corretamente e de forma estável. | O sistema apresenta _bugs_ críticos? | _Reliability Rating (A–E)_ | SonarQube | Mensal | A |
| | Existem _code smells_ que comprometem a estabilidade? | _Code Smells Count_ | SonarQube | Mensal | < 50 |
| | A confiabilidade está alinhada à segurança? | _Security Rating (A–E)_ | SonarQube | Mensal | A |

---

## 3.8 Diagrama GQM
*(Representação hierárquica das relações entre objetivo, questões e métricas.)*

---


## 3.9 Referências

> BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, Hans Dieter. *The Goal Question Metric (GQM) Approach.* In: MARCINIAK, J. J. (ed.). *Encyclopedia of Software Engineering.* New York: John Wiley & Sons, 1994. cap. 6, p. 51–55.  
> INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. *ISO/IEC 25023:2011.* Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models. Genebra: ISO, 2011.

---

## 3.10 Histórico de Versões

| Versão | Data | Descrição | Autor(es) |
|--------|------|------------|------------|
| `1.0` | 14/10/2025 | Criação do documento | [Uires Carlos de Oliveira](https://github.com/uires2023), [Matheus Henrick](https://github.com/MatheusHenrickSantos) |
| `1.1` | 15/10/2025 | Formatação do texto, remoção de informações redundantes | [Gabriela Tiago](https://github.com/GabrielaTiago) |
| `1.2` | 24/10/2025 | Reestruturação do artefato, adição da introdução e dos links de navegação | [Arthur Carneiro](https://github.com/trindadea) |
