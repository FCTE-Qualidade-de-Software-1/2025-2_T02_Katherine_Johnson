# 4. Segurança

## 4.1 Introdução
A **segurança de software** é uma importante característica da qualidade, especialmente em sistemas que tratam **informações sensíveis e dados pessoais dos usuários**, como o **Guardiões da Saúde**. Ela assegura que o sistema proteja seus dados contra **acessos não autorizados, alterações indevidas e falhas de confidencialidade, integridade e disponibilidade**.

Nesta etapa, a análise concentra-se na identificação e prevenção de **vulnerabilidades**, na verificação de **mecanismos de autenticação e controle de acesso**, e na garantia de **rastreabilidade e auditoria das ações do sistema**. 


---

## 4.2 Objetivo GQM

<table>
  <tr><th>Analisar</th><td>o Guardiões da Saúde</td></tr>
  <tr><th>Para o propósito de</th><td>Entender e Avaliar</td></tr>
  <tr><th>Com respeito a</th><td>segurança</td></tr>
  <tr><th>Do ponto de vista da</th><td>equipe de desenvolvimento</td></tr>
  <tr><th>No contexto da</th><td>disciplina de Qualidade de Software</td></tr>
</table>

<div align="center">
  <span style="font-size: 12px; font-style: italic;">
    Autor: <a href="https://github.com/MatheusHenrickSantos">Matheus Henrick</a>
  </span>
</div>

---

## 4.3 Questões
As questões definidas para uma característica visam direcionar a avaliação e verificar se o objetivo de medição está sendo atingido.  

<br>

**Q1.** O sistema protege adequadamente os dados sensíveis dos usuários?  
**Q2.** O sistema garante que os dados não sejam alterados indevidamente?  
**Q3.** As ações dos usuários e do sistema são rastreáveis e auditáveis?  
**Q4.** O sistema verifica corretamente a identidade dos usuários?

---

## 4.4 Hipóteses
As hipóteses representam **expectativas sobre o comportamento ideal do software** em relação às [questões formuladas](#43-questões).  
Elas orientam a interpretação dos resultados das medições e permitem comparar o desempenho real do sistema com o esperado, fornecendo base para o julgamento qualitativo.

<br>

- **H1:** Os dados sensíveis estão protegidos por mecanismos de criptografia e controle de acesso.  
- **H2:** Os dados são protegidos contra alterações não autorizadas, com validações e registros de auditoria.  
- **H3:** O sistema registra ações relevantes com identificação clara do autor e timestamp, permitindo auditoria.  
- **H4:** O sistema utiliza mecanismos seguros de autenticação, evitando acessos indevidos.

---

## 4.5 Métricas
As métricas foram selecionadas com base nas questões e [hipóteses propostas](#44-hipóteses), seguindo o princípio do GQM de alinhar cada medida a um objetivo claro.  

Essas métricas foram extraídas da ferramenta **SonarQube**, amplamente utilizada para avaliação automática de qualidade de código, e permitem quantificar fatores como **vulnerabilidades, hotspots de segurança e conformidade com padrões**.

| Nível | Elemento |
|-------|-----------|
| **Goal** | Analisar o Guardiões da Saúde com o propósito de **entender e avaliar a sua qualidade de software**, com respeito à **segurança**, do ponto de vista da equipe de desenvolvimento e gestores de TI. |
| **Questão 1** | O código apresenta vulnerabilidades conhecidas ou potenciais? |
| **Métrica 1** | _Vulnerabilities Count_ – SonarQube. |
| **Hipótese 1** | Espera-se 0 vulnerabilidades críticas e ≤ 3 médias. |
| **Questão 2** | Existem "_security hotspots_" pendentes de revisão? |
| **Métrica 2** | _Security Hotspots Reviewed (%)_ – SonarQube. |
| **Hipótese 2** | Espera-se 100% dos hotspots revisados. |
| **Questão 3** | O sistema segue boas práticas de segurança (ex: OWASP Top 10)? |
| **Métrica 3** | _Compliance com OWASP checklist (%)._ |
| **Hipótese 3** | Espera-se conformidade ≥ 90%. |

<div align="center">
  <span style="font-size: 12px; font-style: italic;">
    Autor: <a href="https://github.com/uires2023">Uires Carlos de Oliveira</a>
  </span>
</div>

---

## 4.6 Níveis de Pontuação e Critérios de Julgamento
Os **níveis de pontuação** foram definidos para possibilitar uma **interpretação padronizada dos resultados** das [medições](#45-métricas).  
Cada métrica é associada a uma escala de valores que varia de *insuficiente* a *excelente*, permitindo avaliar o grau de atendimento das boas práticas de qualidade de software.

| Métrica | Insuficiente | Satisfatório | Bom | Excelente |
|----------|---------------|--------------|------|------------|
| _Vulnerabilities Count_ | > 10 vulnerabilidades médias ou qualquer crítica | ≤ 10 médias | ≤ 5 médias | 0 críticas / ≤ 3 médias |
| _Security Hotspots Reviewed (%)_ | < 50% | 50–79% | 80–99% | 100% |
| _Conformidade OWASP (%)_ | < 60% | 60–79% | 80–89% | ≥ 90% |

---

## 4.7 Tabela GQM – Segurança
A tabela GQM consolida as relações entre **objetivos, questões, métricas, fontes de dados e periodicidade de coleta**.  
Essa visão integrada facilita o acompanhamento das medições e a verificação contínua da qualidade, garantindo que as decisões sejam tomadas com base em evidências quantitativas e consistentes.

| Objetivo | Questão | Métrica | Fonte | Periodicidade | Alvo |
|-----------|----------|----------|--------|----------------|------|
| Entender e avaliar a qualidade de software quanto à proteção contra vulnerabilidades. | Existem vulnerabilidades conhecidas ou críticas? | _Vulnerabilities Count_ | SonarQube | Mensal | 0 críticas / ≤ 3 médias |
| | Há “_security hotspots_” pendentes de revisão? | _Security Hotspots Reviewed_ (%) | SonarQube | Mensal | 100% revisados |
| | O sistema segue boas práticas OWASP Top 10? | Conformidade OWASP (%) | Checklist interno / SonarQube | Trimestral | ≥ 90% |

---

## 4.8 Diagrama GQM
*(Representação hierárquica das relações entre objetivo, questões e métricas.)*

---

## 4.9 Referências

> BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, Hans Dieter. *The Goal Question Metric (GQM) Approach.* In: MARCINIAK, J. J. (ed.). *Encyclopedia of Software Engineering.* New York: John Wiley & Sons, 1994. cap. 6, p. 51–55.  
> INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. *ISO/IEC 25023:2011.* Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models. Genebra: ISO, 2011.

---

## 4.10 Histórico de Versões

| Versão | Data | Descrição | Autor(es) |
|--------|------|------------|------------|
| `1.0` | 14/10/2025 | Criação do documento | [Uires Carlos de Oliveira](https://github.com/uires2023), [Matheus Henrick](https://github.com/MatheusHenrickSantos) |
| `1.1` | 15/10/2025 | Formatação do texto, remoção de informações redundantes | [Gabriela Tiago](https://github.com/GabrielaTiago) |
| `1.2` | 24/10/2025 | Reestruturação do artefato, adição da introdução e dos links de navegação | [Arthur Carneiro](https://github.com/trindadea) |
| `1.3` | 25/10/2025 | Ajuste dos itens 2.2 - 3.2 - 4.2 (propósitos somente o verbo no infinitivo) | [Uires Carlos de Oliveira](https://github.com/uires2023) |