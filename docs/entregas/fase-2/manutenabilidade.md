# 2. Manutenibilidade

## 2.1 Introdução
A **manutenibilidade** é uma característica fundamental para garantir a evolução contínua e a longevidade de um software. Ela reflete a facilidade com que o sistema pode ser **compreendido, modificado, corrigido e evoluído** ao longo do tempo. 

Para o Guardiões da Saúde — uma plataforma usada em monitoramento participativo de sintomas — assegurar uma boa manutenibilidade é crucial para evolução contínua do código e rápida resposta às demandas de saúde pública.

Nesta fase, a manutenibilidade será avaliada com base em três subcaracterísticas priorizadas na Fase 1: **analisabilidade**, **modificabilidade** e **testabilidade**.

A análise de manutenibilidade busca identificar aspectos estruturais e técnicos que influenciam a facilidade de manutenção, como **modularidade, complexidade, duplicação de código, documentação e cobertura de testes**

## 2.2 Objetivo GQM

<table>
  <tr><th>Analisar</th><td>o Guardiões da Saúde</td></tr>
  <tr><th>Para o propósito de</th><td>Entender</td></tr>
  <tr><th>Com respeito a</th><td>manutenibilidade</td></tr>
  <tr><th>Do ponto de vista da</th><td>equipe de desenvolvimento</td></tr>
  <tr><th>No contexto da</th><td>disciplina de Qualidade de Software</td></tr>
</table>

<div align="center">
  <span style="font-size: 12px; font-style: italic;">
    Autor: <a href="https://github.com/MatheusHenrickSantos">Matheus Henrick</a>
  </span>
</div>

---

## 2.3 Questões
As questões definidas para uma característica visam direcionar a avaliação e verificar se o objetivo de medição está sendo atingido.

As questões avaliativas foram definidas com base nas subcaracterísticas selecionadas na Fase 1.

<br>

**Q1**. Qual é o grau de acoplamento entre os módulos do sistema?  
**Q2**. Há dependências cíclicas entre pacotes ou módulos?  
**Q3**. As responsabilidades dos módulos estão bem separadas?  
**Q4**. O código está suficientemente coberto por testes automatizados?

---

## 2.4 Hipóteses
As hipóteses representam **expectativas sobre o comportamento ideal do software** em relação às [questões formuladas](#23-questões).  
Elas orientam a interpretação dos resultados das medições e permitem comparar o desempenho real do sistema com o esperado, fornecendo base para o julgamento qualitativo.

<br>

- **H1:** O grau de acoplamento entre os módulos é baixo, com poucas dependências diretas, permitindo modificações locais sem impacto significativo.  
- **H2:** Não há ciclos de dependência entre pacotes ou módulos, garantindo arquitetura modular e reusável.  
- **H3:** Cada módulo possui uma responsabilidade única e bem definida, implicando alta coesão e evitando sobreposição funcional.  
- **H4:** O código possui cobertura de testes automatizados de pelo menos 70%.

---

## 2.5 Métricas
As métricas foram selecionadas com base nas questões e [hipóteses propostas](#24-hipóteses), seguindo o princípio do GQM de alinhar cada medida a um objetivo claro.  

Essas métricas foram extraídas da ferramenta **SonarQube**, amplamente utilizada para avaliação automática de qualidade de código, e permitem quantificar fatores como **complexidade cognitiva, duplicação de código e densidade de comentários**.


| Nível | Elemento |
|-------|-----------|
| **Goal** | Analisar o código-fonte do Guardiões da Saúde com o propósito de **entender a manutenibilidade do software**, com respeito à estrutura, documentação e duplicação de código, do ponto de vista dos desenvolvedores. |
| **Questão 1** | O código possui estrutura modular e complexidade adequada para manutenção? |
| **Métrica 1** | _Cognitive Complexity_ média ≤ 10 (SonarQube). |
| **Hipótese 1** | Espera-se que a média de complexidade esteja ≤ 10, indicando boa modularização. |
| **Questão 2** | Existem duplicações que dificultam a manutenção? |
| **Métrica 2** | _Duplicated Lines (%)_ ≤ 5% (SonarQube). |
| **Hipótese 2** | Espera-se duplicação abaixo de 5%. |
| **Questão 3** | O código está devidamente comentado e compreensível? |
| **Métrica 3** | _Comment Density_ ≥ 20% (SonarQube). |
| **Hipótese 3** | Espera-se densidade de comentários ≥ 20%. |

<div align="center">
  <span style="font-size: 12px; font-style: italic;">
    Autor: <a href="https://github.com/uires2023">Uires Carlos de Oliveira</a>
  </span>
</div>

---

## 2.6 Níveis de Pontuação e Critérios de Julgamento
Os **níveis de pontuação** foram definidos para possibilitar uma **interpretação padronizada dos resultados** das [medições](#25-métricas).  
Cada métrica é associada a uma escala de valores que varia de *insuficiente* a *excelente*, permitindo avaliar o grau de atendimento das boas práticas de qualidade de software.

| Métrica | Insuficiente | Satisfatório | Bom | Excelente |
|----------|---------------|--------------|------|------------|
| _Cognitive Complexity_ | > 15 | 11–15 | 8–10 | ≤ 7 |
| _Duplicated Lines (%)_ | > 10% | 6–10% | 3–5% | ≤ 2% |
| _Comment Density (%)_ | < 10% | 10–19% | 20–25% | ≥ 25% |
| _Cobertura de Testes (%)_ | < 50% | 50–69% | 70–85% | > 85% |

---

## 2.7 Tabela GQM – Manutenibilidade
A tabela GQM consolida as relações entre **objetivos, questões, métricas, fontes de dados e periodicidade de coleta**.  
Essa visão integrada facilita o acompanhamento das medições e a verificação contínua da qualidade, garantindo que as decisões sejam tomadas com base em evidências quantitativas e consistentes.

| Objetivo | Questão | Métrica | Fonte | Periodicidade | Alvo |
|-----------|----------|----------|--------|----------------|------|
| Entender a facilidade de manutenção e evolução do código do Guardiões da Saúde. | O código apresenta complexidade adequada para manutenção? | _Cognitive Complexity_ média ≤ 10 | SonarQube | Mensal | ≤ 10 |
| | Há duplicações que prejudicam a manutenção? | _Duplicated Lines (%)_ | SonarQube | Mensal | < 5 % |
| | O código está bem comentado? | _Comment Density (%)_ | SonarQube | Mensal | ≥ 20 % |

---

## 2.8 Diagrama GQM
*(Representação hierárquica entre objetivo, questões e métricas.)*

---

## 2.9 Referências

> BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, Hans Dieter. *The Goal Question Metric (GQM) Approach.* In: MARCINIAK, J. J. (ed.). *Encyclopedia of Software Engineering.* New York: John Wiley & Sons, 1994. cap. 6, p. 51–55.  
> INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. *ISO/IEC 25023:2011.* Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models. Genebra: ISO, 2011.

---

## 2.10 Histórico de Versões

| Versão | Data | Descrição | Autor(es) |
|--------|------|------------|------------|
| `1.0` | 14/10/2025 | Criação do documento | [Uires Carlos de Oliveira](https://github.com/uires2023), [Matheus Henrick](https://github.com/MatheusHenrickSantos) |
| `1.1` | 15/10/2025 | Formatação do texto, remoção de informações redundantes | [Gabriela Tiago](https://github.com/GabrielaTiago) |
| `1.2` | 24/10/2025 | Reestruturação do artefato, adição da introdução e dos links de navegação | [Arthur Carneiro](https://github.com/trindadea) |
| `1.3` | 25/10/2025 | Ajuste dos itens 2.2 - 3.2 - 4.2 (propósitos somente o verbo no infinitivo) | [Uires Carlos de Oliveira](https://github.com/uires2023) |