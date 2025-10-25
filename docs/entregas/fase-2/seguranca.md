# 4. Segurança

## 4.1 Introdução
*(Esta seção apresentará o contexto da segurança como um fator essencial na qualidade de software, especialmente em sistemas que lidam com dados sensíveis de usuários. Será descrita a importância de avaliar vulnerabilidades, autenticação e rastreabilidade no Guardiões da Saúde.)*

---

## 4.2 Objetivo GQM

<table>
  <tr><th>Analisar</th><td>o Guardiões da Saúde</td></tr>
  <tr><th>Para o propósito de</th><td>entender e avaliar a qualidade de software quanto à proteção contra vulnerabilidades</td></tr>
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
*(Questões que orientam a avaliação da segurança no contexto do sistema Guardiões da Saúde.)*

**Q1.** O sistema protege adequadamente os dados sensíveis dos usuários?  
**Q2.** O sistema garante que os dados não sejam alterados indevidamente?  
**Q3.** As ações dos usuários e do sistema são rastreáveis e auditáveis?  
**Q4.** O sistema verifica corretamente a identidade dos usuários?

---

## 4.4 Hipóteses
*(Expectativas sobre o comportamento do sistema em relação à segurança.)*

- **H1:** Os dados sensíveis estão protegidos por mecanismos de criptografia e controle de acesso.  
- **H2:** Os dados são protegidos contra alterações não autorizadas, com validações e registros de auditoria.  
- **H3:** O sistema registra ações relevantes com identificação clara do autor e timestamp, permitindo auditoria.  
- **H4:** O sistema utiliza mecanismos seguros de autenticação, evitando acessos indevidos.

---

## 4.5 Métricas
*(Métricas selecionadas para medir a segurança, segundo a abordagem GQM.)*

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
*(Definição dos intervalos de desempenho e critérios de avaliação de segurança.)*

| Métrica | Insuficiente | Satisfatório | Bom | Excelente |
|----------|---------------|--------------|------|------------|
| _Vulnerabilities Count_ | > 10 vulnerabilidades médias ou qualquer crítica | ≤ 10 médias | ≤ 5 médias | 0 críticas / ≤ 3 médias |
| _Security Hotspots Reviewed (%)_ | < 50% | 50–79% | 80–99% | 100% |
| _Conformidade OWASP (%)_ | < 60% | 60–79% | 80–89% | ≥ 90% |

---

## 4.7 Tabela GQM – Segurança
*(Resumo das métricas aplicadas e periodicidade de coleta.)*

| Objetivo | Questão | Métrica | Fonte | Periodicidade | Alvo |
|-----------|----------|----------|--------|----------------|------|
| Entender e avaliar a qualidade de software quanto à proteção contra vulnerabilidades. | Existem vulnerabilidades conhecidas ou críticas? | _Vulnerabilities Count_ | SonarQube | Mensal | 0 críticas / ≤ 3 médias |
| | Há “_security hotspots_” pendentes de revisão? | _Security Hotspots Reviewed_ (%) | SonarQube | Mensal | 100% revisados |
| | O sistema segue boas práticas OWASP Top 10? | Conformidade OWASP (%) | Checklist interno / SonarQube | Trimestral | ≥ 90% |

---

## 4.8 Diagrama GQM
*(Representação hierárquica das relações entre objetivo, questões e métricas.)*


## 4.9 Referências

> BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, Hans Dieter. *The Goal Question Metric (GQM) Approach.* In: MARCINIAK, J. J. (ed.). *Encyclopedia of Software Engineering.* New York: John Wiley & Sons, 1994. cap. 6, p. 51–55.  
> INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. *ISO/IEC 25023:2011.* Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models. Genebra: ISO, 2011.

---

## 4.10 Histórico de Versões

| Versão | Data | Descrição | Autor(es) |
|--------|------|------------|------------|
| `1.0` | 14/10/2025 | Criação do documento | [Uires Carlos de Oliveira](https://github.com/uires2023), [Matheus Henrick](https://github.com/MatheusHenrickSantos) |
| `1.1` | 15/10/2025 | Formatação do texto, remoção de informações redundantes | [Gabriela Tiago](https://github.com/GabrielaTiago) |
