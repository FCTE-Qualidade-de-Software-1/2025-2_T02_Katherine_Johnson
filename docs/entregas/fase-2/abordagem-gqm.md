# Abordagem GQM

## Objetivos de Medição

### **META GLOBAL**

Analisar **o sistema Guardiões da Saúde**
com o propósito de **entender e avaliar a sua qualidade de software,**
com respeito às características de **manutenibilidade, confiabilidade e segurança,**
do ponto de vista **da equipe de desenvolvimento e qualidade,**
no contexto da **disciplina de Qualidade de Software.**

### Manutenibilidade

<table>
  <tr>
    <th>Analisar</th>
    <td>o Guardiões da Saúde</td>
  </tr>
  <tr>
    <th>Para o propósito de</th>
    <td>entender a facilidade de manutenção e evolução do código</td>
  </tr>
  <tr>
    <th>Com respeito a</th>
    <td>manutenibilidade</td>
  </tr>
  <tr>
    <th>Do ponto de vista da</th>
    <td>equipe de desenvolvimento</td>
  </tr>
  <tr>
    <th>No contexto da</th>
    <td>disciplina de Qualidade de Software</td>
  </tr>
</table>

<div align="center">
    <span style="font-size: 12px; font-style: italic;">
        Autor: <a href="https://github.com/MatheusHenrickSantos">Matheus Henrick</a>
    </span>
</div>

### Confiabilidade

<table>
  <tr>
    <th>Analisar</th>
    <td>o Guardiões da Saúde</td>
  </tr>
  <tr>
    <th>Para o propósito de</th>
    <td>entender o nível de confiança do software em operar corretamente e de forma estável</td>
  </tr>
  <tr>
    <th>Com respeito a</th>
    <td>confiabilidade</td>
  </tr>
  <tr>
    <th>Do ponto de vista da</th>
    <td>equipe de desenvolvimento</td>
  </tr>
  <tr>
    <th>No contexto da</th>
    <td>disciplina de Qualidade de Software</td>
  </tr>
</table>

<div align="center">
    <span style="font-size: 12px; font-style: italic;">
        Autor: <a href="https://github.com/MatheusHenrickSantos">Matheus Henrick</a>
    </span>
</div>

### Segurança

<table>
  <tr>
    <th>Analisar</th>
    <td>o Guardiões da Saúde</td>
  </tr>
  <tr>
    <th>Para o propósito de</th>
    <td>entender e avaliar a qualidade de software quanto à proteção contra vulnerabilidades</td>
  </tr>
  <tr>
    <th>Com respeito a</th>
    <td>segurança</td>
  </tr>
  <tr>
    <th>Do ponto de vista da</th>
    <td>equipe de desenvolvimento</td>
  </tr>
  <tr>
    <th>No contexto da</th>
    <td>disciplina de Qualidade de Software</td>
  </tr>
</table>

<div align="center">
    <span style="font-size: 12px; font-style: italic;">
        Autor: <a href="https://github.com/MatheusHenrickSantos">Matheus Henrick</a>
    </span>
</div>

## Questões, Hipóteses e Métricas

### Manutenibilidade

**Q1**. Qual é o grau de acoplamento entre os módulos do sistema?  
**Hipótese**: O grau de acoplamento entre os módulos é baixo, com poucas dependências diretas, permitindo modificações locais sem impacto significativo em outros componentes.

**Q2**. Há dependências cíclicas entre pacotes ou módulos?  
**Hipótese**: Não há ciclos de dependência entre pacotes ou módulos, o que garante uma arquitetura modular e facilita refatorações e reuso de código.

**Q3**. As responsabilidades dos módulos estão bem separadas?  
**Hipótese**: Cada módulo possui uma responsabilidade única e bem definida, o que implica em alta coesão e evita sobreposição funcional.

**Q4**. O código está suficientemente coberto por testes automatizados?  
**Hipótese**: O código possui cobertura de testes automatizados de pelo menos 70%.

| Nível          | Elemento                                                                                                                                                                                                            |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **_Goal_**     | Analisar o código-fonte do Guardiões da Saúde com o propósito de **entender a manutenibilidade do software**, com respeito à estrutura, documentação e duplicação de código, do ponto de vista dos desenvolvedores. |
| **Questão 1**  | O código possui estrutura modular e complexidade adequada para manutenção?                                                                                                                                          |
| **Métrica 1**  | _Cognitive Complexity_ média ≤ 10 (SonarQube).                                                                                                                                                                      |
| **Hipótese 1** | Espera-se que a média de complexidade esteja ≤ 10, indicando boa modularização.                                                                                                                                     |
| **Questão 2**  | Existem duplicações que dificultam a manutenção?                                                                                                                                                                    |
| **Métrica 2**  | _Duplicated Lines (%)_ ≤ 5% (SonarQube).                                                                                                                                                                            |
| **Hipótese 2** | Espera-se duplicação abaixo de 5%.                                                                                                                                                                                  |
| **Questão 3**  | O código está devidamente comentado e compreensível?                                                                                                                                                                |
| **Métrica 3**  | _Comment Density_ ≥ 20% (SonarQube).                                                                                                                                                                                |
| **Hipótese 3** | Espera-se densidade de comentários ≥ 20%.                                                                                                                                                                           |

<div align="center">
    <span style="font-size: 12px; font-style: italic;">
        Autor: <a href="https://github.com/uires2023">Uires Carlos de Oliveira</a>
    </span>
</div>

### Confiabilidade

**Q1**. O sistema está disponível para uso na maior parte do tempo?  
**Hipótese**: O sistema está disponível durante 99% do tempo de operação, com interrupções mínimas e planejadas.

**Q2**. O sistema consegue continuar operando mesmo diante de falhas pontuais?  
**Hipótese**: O sistema possui mecanismos de tolerância a falhas que evitam interrupções totais.

**Q3**. O sistema consegue se recuperar rapidamente após uma falha?  
**Hipótese**: O tempo médio de recuperação é inferior a 5 minutos em falhas comuns, com processos automatizados de restauração.

| Nível          | Elemento                                                                                                                                                                                                                               |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **_Goal_**     | Analisar o código-fonte do Guardiões da Saúde com o propósito de **entender a confiabilidade do software**, com respeito à ocorrência de falhas e robustez do sistema, do ponto de vista dos desenvolvedores e analistas de qualidade. |
| **Questão 1**  | O sistema apresenta _bugs_ que comprometem sua execução?                                                                                                                                                                               |
| **Métrica 1**  | _Reliability Rating (A–E)_ – SonarQube (baseado em número de _bugs_).                                                                                                                                                                  |
| **Hipótese 1** | Espera-se _Reliability Rating = A_, indicando ausência de falhas críticas.                                                                                                                                                             |
| **Questão 2**  | Existem vulnerabilidades que afetam a confiabilidade do sistema?                                                                                                                                                                       |
| **Métrica 2**  | _Security Rating (A–E)_ – SonarQube.                                                                                                                                                                                                   |
| **Hipótese 2** | Espera-se _Security Rating = A_.                                                                                                                                                                                                       |
| **Questão 3**  | Há "_code smells_" que possam levar a falhas futuras?                                                                                                                                                                                  |
| **Métrica 3**  | _Number of Code Smells_ e _Maintainability Rating (A–E)_.                                                                                                                                                                              |
| **Hipótese 3** | Espera-se _Maintainability Rating = A_ e menos de 50 _code smells_.                                                                                                                                                                    |

<div align="center">
    <span style="font-size: 12px; font-style: italic;">
        Autor: <a href="https://github.com/uires2023">Uires Carlos de Oliveira</a>
    </span>
</div>

### Segurança

**Q1**. O sistema protege adequadamente os dados sensíveis dos usuários?  
**Hipótese**: Os dados sensíveis estão protegidos por mecanismos de criptografia e controle de acesso.

**Q2**. O sistema garante que os dados não sejam alterados indevidamente?  
**Hipótese**: Os dados são protegidos contra alterações não autorizadas, com validações e registros de auditoria.

**Q3**. As ações dos usuários e do sistema são rastreáveis e auditáveis?  
**Hipótese**: o sistema registra ações relevantes com identificação clara do autor e timestamp, permitindo auditoria.

**Q4**. O sistema verifica corretamente a identidade dos usuários?  
**Hipótese**: O sistema utiliza mecanismos seguros de autenticação, evitando acesso indevido por usuários não autorizados.

| Nível          | Elemento                                                                                                                                                                                            |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **_Goal_**     | Analisar o Guardiões da Saúde com o propósito de **entender e avaliar a sua qualidade de software**, com respeito à **segurança**, do ponto de vista da equipe de desenvolvimento e gestores de TI. |
| **Questão 1**  | O código apresenta vulnerabilidades conhecidas ou potenciais?                                                                                                                                       |
| **Métrica 1**  | _Vulnerabilities Count_ – SonarQube.                                                                                                                                                                |
| **Hipótese 1** | Espera-se 0 vulnerabilidades críticas e ≤ 3 médias.                                                                                                                                                 |
| **Questão 2**  | Existem "_security hotspots_" pendentes de revisão?                                                                                                                                                 |
| **Métrica 2**  | _Security Hotspots Reviewed (%)_ – SonarQube.                                                                                                                                                       |
| **Hipótese 2** | Espera-se 100% dos hotspots revisados.                                                                                                                                                              |
| **Questão 3**  | O sistema segue boas práticas de segurança (ex: OWASP Top 10)?                                                                                                                                      |
| **Métrica 3**  | _Compliance com OWASP checklist (%)._                                                                                                                                                               |
| **Hipótese 3** | Espera-se conformidade ≥ 90%.                                                                                                                                                                       |

<div align="center">
    <span style="font-size: 12px; font-style: italic;">
        Autor: <a href="https://github.com/uires2023">Uires Carlos de Oliveira</a>
    </span>
</div>

## Tabela GQM por Característica

### Manutenibilidade

| Objetivo                                                                        | Questão                                                   | Métrica                           | Fonte                              | Periodicidade | Alvo   |
| ------------------------------------------------------------------------------- | --------------------------------------------------------- | --------------------------------- | ---------------------------------- | ------------- | ------ |
| Entender a facilidade de manutenção e evolução do código do Guardiões da Saúde. | O código apresenta complexidade adequada para manutenção? | _Cognitive Complexity_ média ≤ 10 | SonarQube (_Cognitive Complexity_) | Mensal        | ≤ 10   |
|                                                                                 | Há duplicações que prejudicam a manutenção?               | _Duplicated Lines_ (%)            | SonarQube (_Duplicated Lines_)     | Mensal        | < 5 %  |
|                                                                                 | O código está bem comentado?                              | _Comment Density_ (%)             | SonarQube (_Comment Density_)      | Mensal        | ≥ 20 % |

<div align="center">
    <span style="font-size: 12px; font-style: italic;">
        Autor: <a href="https://github.com/uires2023">Uires Carlos de Oliveira</a>
    </span>
</div>

### Confiabilidade

| Objetivo                                                                             | Questões                                              | Métricas                   | Fonte                                 | Periodicidade | Alvo |
| ------------------------------------------------------------------------------------ | ----------------------------------------------------- | -------------------------- | ------------------------------------- | ------------- | ---- |
| Entender o nível de confiança do software em operar corretamente e de forma estável. | O sistema apresenta _bugs_ críticos?                  | _Reliability Rating_ (A–E) | SonarQube – Métrica _Reliability_     | Mensal        | A    |
|                                                                                      | Existem _code smells_ que comprometem a estabilidade? | _Code Smells Count_        | SonarQube – Métrica _Maintainability_ | Mensal        | < 50 |
|                                                                                      | A confiabilidade está alinhada à segurança?           | _Security Rating_ (A–E)    | SonarQube – Métrica _Security_        | Mensal        | A    |

<div align="center">
    <span style="font-size: 12px; font-style: italic;">
        Autor: <a href="https://github.com/uires2023">Uires Carlos de Oliveira</a>
    </span>
</div>

### Segurança

| Objetivo                                                                              | Questão                                          | Métrica                          | Fonte                                  | Periodicidade | Alvo                    |
| ------------------------------------------------------------------------------------- | ------------------------------------------------ | -------------------------------- | -------------------------------------- | ------------- | ----------------------- |
| Entender e avaliar a qualidade de software quanto à proteção contra vulnerabilidades. | Existem vulnerabilidades conhecidas ou críticas? | _Vulnerabilities Count_          | SonarQube (_Security Vulnerabilities_) | Mensal        | 0 críticas / ≤ 3 médias |
|                                                                                       | Há “_security hotspots_” pendentes de revisão?   | _Security Hotspots Reviewed_ (%) | SonarQube (_Security Hotspots_)        | Mensal        | 100% revisados          |
|                                                                                       | O sistema segue boas práticas OWASP Top 10?      | Conformidade OWASP (%)           | _Checklist_ interno / SonarQube        | Trimestral    | ≥ 90%                   |

<div align="center">
    <span style="font-size: 12px; font-style: italic;">
        Autor: <a href="https://github.com/uires2023">Uires Carlos de Oliveira</a>
    </span>
</div>

## Referências Bibliográficas

> BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, Hans Dieter. The Goal Question Metric (GQM) Approach. In: MARCINIAK, J. J. (ed.). Encyclopedia of Software Engineering. New York: John Wiley & Sons, 1994. cap. 6, p. 51-55.
> INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. ISO/IEC 25023:2011. Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models. Genebra: ISO, 2011.

---

## Histórico de Versões

| Versão | Data       | Descrição                                               | Autor(es)                                                                                                            |
| ------ | ---------- | ------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `1.0`  | 14/10/2025 | Criação do documento                                    | [Uires Carlos de Oliveira](https://github.com/uires2023), [Matheus Henrick](https://github.com/MatheusHenrickSantos) |
| `1.1`  | 15/10/2025 | Formatação do texto, remoção de informações redundantes | [Gabriela Tiago](https://github.com/GabrielaTiago)                                                                   |
