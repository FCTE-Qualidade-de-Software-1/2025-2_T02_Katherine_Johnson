

# FASE 4 – Confiabilidade - Executar o Planejamento (Execução + Análise + Interpretação)

Nesta fase são exibidos os **dados coletados** e a **interpretação dos resultados**
referentes à análise da característica **Confiabilidade** do projeto **Guardiões da Saúde – App**.

---

# 4. Confiabilidade – Execução da Avaliação

## 4.1 Introdução

Esta fase descreve a execução prática do planejamento definido na Fase 3, com foco em:

- coleta das métricas via **SonarQube Community Edition**;  
- organização e registro dos dados;  
- interpretação dos resultados à luz do modelo **GQM**;  
- resposta às questões de Confiabilidade (maturidade, disponibilidade e tolerância a falhas).

Conforme estabelecido na Fase 3:

- métricas que dependem de **ambiente de produção** foram classificadas como **não mensuráveis** neste estudo;  
- métricas obtidas por **análise estática do código-fonte** foram efetivamente coletadas e analisadas.

---

## 4.2 Execução da Análise

A análise foi realizada em ambiente **Ubuntu**, utilizando o servidor local do SonarQube e o SonarScanner.

### Procedimentos executados

1. Clonar o repositório do app Guardiões da Saúde – Frontend.  
2. Iniciar o SonarQube no Ubuntu (`./sonar.sh start`).  
3. Acessar o painel web em `http://localhost:9000`.  
4. Criar o projeto no SonarQube e configurar o token de acesso.  
5. Executar o **SonarScanner** no repositório clonado.  
6. Aguardar o processamento de aproximadamente **21.000 linhas de código**.  
7. Registrar os dashboards e métricas gerados pelo SonarQube.

As figuras (prints de tela) dos dashboards podem ser armazenadas em  
`/docs/assets/images/` e referenciadas nesta fase como evidências da execução.

---

## 4.3 Métricas Coletadas (SonarQube)

Nesta seção são apresentadas as métricas efetivamente coletadas no SonarQube, com:

- valor numérico obtido;  
- conceito associado à Confiabilidade;  
- interpretação do resultado;  
- avaliação qualitativa (bom, regular, ruim).

### 4.3.1 Reliability Rating – D

- **Valor obtido:**
  - *Reliability Rating*: **D**  
  - *Bugs totais*: **206**  
  - *High issue*: **1**

- **Conceito:**  
  O *Reliability Rating* resume a confiabilidade do sistema com base na
  **quantidade** e **severidade** dos _bugs_ detectados.

- **Interpretação:**  
  A nota **D** indica uma probabilidade significativa de ocorrência de falhas em
  execução, devido à presença de bugs relevantes.

- **Avaliação:**  
  - Classificação: **Ruim**  
  - Impacto: sugere **baixa maturidade** e maior risco de falhas em produção.

---

### 4.3.2 Bugs – 206

- **Valor obtido:**  
  - **206 _bugs_** detectados pelo SonarQube.

- **Conceito:**  
  _Bugs_ representam erros de lógica, fluxo ou uso incorreto de recursos que
  podem causar comportamento inesperado ou falha na aplicação.

- **Interpretação:**  
  Para um projeto de aproximadamente **21k linhas de código**, a presença de
  206 _bugs_ é considerada **elevada**, evidenciando fragilidades no código.

- **Avaliação:**  
  - Classificação: **Ruim**  
  - Impacto: compromete diretamente a **confiabilidade** e a **robustez** do sistema.

---

### 4.3.3 Maintainability Rating – A

- **Valor obtido:**  
  - *Maintainability Rating*: **A**

- **Conceito:**  
  Mede o esforço estimado para **manter** e **refatorar** o código, levando em
  conta dívida técnica, complexidade e organização do projeto.

- **Interpretação:**  
  Mesmo com problemas estruturais (smells, duplicação), o SonarQube indica que
  o esforço para corrigir o código é relativamente **baixo**.

- **Avaliação:**  
  - Classificação: **Excelente**  
  - Impacto: facilita a implementação de correções e melhorias futuras.

---

### 4.3.4 Code Smells – 355

- **Valor obtido:**  
  - **355 _code smells_**

- **Conceito:**  
  _Code smells_ são indícios de **má qualidade interna** (métodos longos,
  nomes pouco claros, estruturas confusas, etc.) que não causam falha
  imediata, mas prejudicam a **manutenibilidade** e podem introduzir erros no futuro.

- **Interpretação:**  
  A quantidade de 355 _smells_ é considerada **alta**, sugerindo necessidade
  de refatoração em diversos pontos do código.

- **Avaliação:**  
  - Classificação: **Regular → Ruim**  
  - Impacto: afeta a **tolerância a falhas** e a **evolução** do sistema.

---

### 4.3.5 Duplications – 39,1%

- **Valor obtido:**  
  - **39,1%** de linhas duplicadas.

- **Conceito:**  
  A métrica de *duplication* indica o percentual de código repetido.  
  Boas práticas recomendam valores **abaixo de 5%**; valores acima de **20%**
  já são considerados críticos.

- **Interpretação:**  
  O valor de **39,1%** é **muito superior** ao limite desejável, indicando forte
  dependência de trechos copiados e colados. Isso aumenta a probabilidade de erros
  repetidos e dificulta a manutenção.

- **Avaliação:**  
  - Classificação: **Péssimo**  
  - Impacto: prejudica a **confiabilidade**, a **tolerância a falhas** e o custo de manutenção.

---

### 4.3.6 Coverage – 0%

- **Valor obtido:**  
  - **0% de cobertura de testes**.

- **Conceito:**  
  *Coverage* mede a porcentagem de código executada por testes automatizados
  (por exemplo, testes unitários).

- **Interpretação:**  
  O valor de **0%** significa que **não há testes automatizados** configurados
  no projeto, impossibilitando a verificação sistemática das funcionalidades.

- **Avaliação:**  
  - Classificação: **Péssimo**  
  - Impacto: reduz drasticamente a **confiabilidade**, pois não há garantia
    automatizada de que o código se comporta como esperado após mudanças.

---

### 4.3.7 Security Rating – A

- **Valor obtido:**  
  - *Security Rating*: **A**

- **Conceito:**  
  Avalia a presença de vulnerabilidades de segurança detectáveis via análise estática.

- **Interpretação:**  
  A nota **A** indica que não foram identificadas vulnerabilidades relevantes no
  código analisado.

- **Avaliação:**  
  - Classificação: **Excelente**  
  - Impacto: sugere um bom nível de **segurança estática**, embora não substitua
    revisões manuais e testes específicos.

---

### 4.3.8 Security Hotspots Reviewed – E

- **Valor obtido:**  
  - Hotspots revisados: **0%**  
  - Classificação: **E**

- **Conceito:**  
  *Security hotspots* são trechos de código potencialmente sensíveis, que exigem
  **revisão manual** para confirmar se representam ou não um risco de segurança.

- **Interpretação:**  
  A nota **E** indica que nenhum hotspot foi revisado. Embora a métrica de
  vulnerabilidades seja A, a ausência de revisão manual deixa riscos em aberto.

- **Avaliação:**  
  - Classificação: **Ruim**  
  - Impacto: aponta necessidade de maior atenção ao processo de revisão de segurança.

---

### 4.3.9 Tamanho do Projeto – ~21.000 linhas

- **Valor obtido:**  
  - Aproximadamente **21k linhas de código**.

- **Conceito:**  
  Representa o tamanho total do código analisado (*ncloc*).

- **Interpretação:**  
  Serve como base para contextualizar as demais métricas.  
  Para esse volume de código, os valores de **206 bugs**, **355 _smells_** e
  **39,1% de duplicação** são considerados **altos**.

---

## 4.4 Respostas às Questões GQM

Nesta seção, os resultados são organizados em função das questões definidas na Fase 2.

### Q1. O sistema está disponível para uso na maior parte do tempo?

- **Resposta:** *Não mensurável neste estudo.*  
- **Justificativa:** a métrica de disponibilidade (_Availability Rate_) depende
  de dados de **ambiente de produção** (como _uptime_ monitorado por ferramentas
  externas), que não estão disponíveis no contexto da análise estática.

---

### Q2. O sistema continua operando diante de falhas parciais sem queda total?

- **Resposta:** **Não.**

- **Justificativa estrutural (análise estática):**
  - duplicação elevada (**39,1%**);  
  - grande quantidade de _code smells_ (**355**);  
  - ausência completa de testes automatizados (**0% de coverage**);  
  - presença de _bugs_ de maior severidade (1 *high issue*);  
  - confiabilidade geral classificada como **D**.

Esses fatores indicam baixa **tolerância estrutural a falhas**, mesmo sem dados de
_execução_ em produção.

---

### Q3. O sistema apresenta baixa incidência de _bugs_ que impactem a operação?

- **Resposta:** **Não.**

- **Evidências:**
  - **206 _bugs_** detectados pelo SonarQube;  
  - 1 _bug_ de severidade alta (*high*);  
  - *Reliability Rating* classificado como **D**.

Tais resultados apontam para **alta probabilidade de falhas** em execução.

---

## 4.5 Conclusão da Fase 4

A análise estática realizada com o SonarQube indica que o nível de **Confiabilidade**
do **Guardiões da Saúde – App** é **insatisfatório** no estado atual do código.

**Síntese dos principais pontos:**

- elevada **quantidade de _bugs_** (206);  
- **duplicação** excessiva (**39,1%**);  
- ausência de **testes automatizados** (0% de cobertura);  
- grande número de **_code smells_** (355);  
- avaliação de **confiabilidade D**;  
- **hotspots de segurança** sem revisão (classificação E).

Apesar da boa avaliação em **segurança estática** (Security Rating A) e em
**manutenibilidade** (Maintainability Rating A), a combinação de muitos _bugs_,
duplicação alta e ausência total de testes leva a um cenário de **baixa confiabilidade**.

### Recomendações

- Implementar uma suíte mínima de **testes automatizados** (unitários e de integração).  
- Priorizar a correção dos **_bugs_ de alta severidade**.  
- Reduzir a **duplicação de código** por meio de refatoração.  
- Tratar os principais **_code smells_** relacionados à complexidade e estrutura.  
- Revisar manualmente os **security hotspots** sinalizados pelo SonarQube.  

---

## 4.6 Histórico de Versões

| Versão | Data       | Descrição                            | Autor(es)          |
| ------ | ---------- | ------------------------------------ | ------------------ |
| `1.0`  | 25/11/2025 | Execução da avaliação – Confiabilidade | Uires Carlos de Oliveira |