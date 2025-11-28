<!-- # Confiabilidade - Execução, Análise e Interpretação

## 1. Introdução
_Objetivo, escopo e relação com o plano da Fase 3. Liste aqui o que é mensurável/não mensurável._

## 2. Ambiente e Recursos
- SO, versões de ferramentas (ex.: SonarQube/Scanner), commit/branch analisado.
- Referência da pasta de dados brutos e evidências no repositório.

## 3. Procedimentos Executados (reprodutibilidade)
1. Passo a passo seguido, alinhado ao plano da Fase 3.
2. Anote qualquer desvio do plano.

## 4. Evidências e Dados Brutos
- Links para prints/relatórios/vídeos usados nas métricas (armazenar em `docs/assets/...`).
- Se houver planilha/CSV/JSON, referenciar o arquivo.

## 5. Métricas Coletadas
| Métrica | Valor | Evidência | Interpretação | Julgamento |
| --- | --- | --- | --- | --- |
| (ex.: Bugs, Reliability Rating, Code Smells, Duplicação, Cobertura) | | | | |

### 5.1 Métricas não mensuráveis (se houver)
- Descrever e justificar.

## 6. Respostas às Questões GQM
- Q1 …
- Q2 …
- Q3 …

## 7. Conclusão e Recomendações
- Síntese do nível de Confiabilidade.
- 3–5 ações priorizadas.

## 8. Histórico de Versões
| Versão | Data       | Descrição                      | Autor(es) |
| ------ | ---------- | ------------------------------ | --------- |
| `1.0`  | 27/11/2025 | Criação do documento | [Arthur Carneiro](https://github.com/trindadea)   | -->



# 4. Confiabilidade – Execução da Avaliação

## 4.1 Introdução

A Fase 4 tem como objetivo executar o planejamento definido na Fase 3,
realizando a coleta real dos dados e a interpretação dos resultados da
característica **Confiabilidade** no projeto **Guardiões da Saúde – App**, por
meio de análise estática do código-fonte.

A avaliação foi conduzida utilizando:

- **SonarQube Community Build v25.11.0.114957**
- Modo **MQR**
- URL de acesso: `http://localhost:9000/dashboard?id=guardioes-app&codeScope=overall`

<div align="center">
    <p><strong>Figura 0.0 – Principal</strong></p>
</div>

<div align="center">
    <img src="../../../assets/images/Principal.jpeg" width="100%" alt="Principal">
</div>

<div align="center" style="font-size: 12px; font-style: italic;">
    Fonte: Captura de tela SONAR v25.11.0.114957.
</div>

---
Conforme estabelecido no planejamento:

- Métricas dependentes de execução em produção → *não mensuráveis*  
- Métricas obtidas por análise estática → *mensuráveis e analisadas nesta fase*

---

## 4.2 Execução da Análise

A execução foi realizada em ambiente Ubuntu.

### Procedimentos executados

1. Inicialização do SonarQube (`./sonar.sh start`)  
2. Execução do SonarScanner no repositório clonado  
3. Processamento de aproximadamente **21.000 linhas de código**  
4. Geração automática dos dashboards  
5. Registro das métricas e capturas de tela  

As evidências da execução (prints) estão armazenadas no diretório:

/docs/assets/images/fase-4/


---

## 4.3 Métricas Coletadas (SonarQube Community Build)

Nesta seção são exibidas as métricas efetivamente coletadas pelo SonarQube.

Cada métrica apresenta:

- valor obtido  
- conceito  
- interpretação  
- avaliação qualitativa  

---

### 4.3.1 Reliability Rating — D

- **Valor obtido**
  - Reliability Rating: **D**
  - Total de _bugs_: **206**
  - _High issues_: **1**

- **Conceito**  
  O *Reliability Rating* representa a probabilidade de falhas em execução, baseada
  na quantidade e severidade de bugs identificados.

- **Interpretação**  
  A nota **D** indica presença de defeitos relevantes que impactam a estabilidade
  e a confiabilidade.

- **Avaliação:** **Ruim**

<div align="center">
    <p><strong>Figura 1 – Reliability_D</strong></p>
</div>

<div align="center">
    <img src="../../../assets/images/Reliability_D.jpeg" width="50%" alt="Reliability_D">
</div>

<div align="center" style="font-size: 12px; font-style: italic;">
    Fonte: Captura de tela SONAR v25.11.0.114957.
</div>


---

### 4.3.2 Bugs — 206

- **Valor obtido:** **206 _bugs_**

- **Conceito**  
  Erros que podem causar comportamentos incorretos, falhas lógicas ou travamentos.

- **Interpretação**  
  Para um sistema de ~21k linhas, este valor é elevado, caracterizando baixa
  maturidade do código.

- **Avaliação:** **Ruim**

---

### 4.3.3 Maintainability Rating — A

- **Valor obtido:** **A**

- **Conceito**  
  Mede a facilidade de manutenção e refatoração, considerando dívida técnica e
  complexidade.

- **Interpretação**  
  Indica que o projeto é tecnicamente fácil de corrigir, apesar de problemas
  estruturais.

- **Avaliação:** **Excelente**

<div align="center">
    <p><strong>Figura 2 – Maintainability_A</strong></p>
</div>

<div align="center">
    <img src="../../../assets/images/Maintainability_A.jpeg" width="50%" alt="Maintainability_A">
</div>

<div align="center" style="font-size: 12px; font-style: italic;">
    Fonte: Captura de tela SONAR v25.11.0.114957.
</div>

---

### 4.3.4 Code Smells — 355

- **Valor obtido:** **355**

- **Conceito**  
  Indicam problemas de organização e clareza que afetam a evolução do sistema.

- **Interpretação**  
  Quantidade elevada de _smells_ sugere estrutura fragilizada.

- **Avaliação:** **Regular → Ruim**

---

### 4.3.5 Duplications — 39.1%

- **Valor obtido:** **39.1%**

- **Conceito**  
  Mede o percentual de trechos de código repetidos.

- **Interpretação**  
  Acima de 20% já é considerado crítico; 39.1% representa altíssimo risco de
  falhas e custo de manutenção.

- **Avaliação:** **Péssimo**

<div align="center">
    <p><strong>Figura 3 – Duplications</strong></p>
</div>

<div align="center">
    <img src="../../../assets/images/Duplications.jpeg" width="50%" alt="Duplications">
</div>

<div align="center" style="font-size: 12px; font-style: italic;">
    Fonte: Captura de tela SONAR v25.11.0.114957.
</div>


---

### 4.3.6 Coverage — 0%

- **Valor obtido:** **0%**

- **Conceito**  
  Mede a porcentagem de código coberto por testes automatizados.

- **Interpretação**  
  Nenhum teste foi implementado, impossibilitando validação automatizada.

- **Avaliação:** **Péssimo**

---

### 4.3.7 Security Rating — A

- **Valor obtido:** **A**

- **Conceito**  
  Avalia vulnerabilidades detectáveis por análise estática.

- **Interpretação**  
  Nenhuma vulnerabilidade crítica foi identificada.

- **Avaliação:** **Excelente**

---

### 4.3.8 Security Hotspots Reviewed — E

- **Valor obtido**
  - Hotspots revisados: **0%**
  - Nota: **E**

- **Conceito**  
  Pontos sensíveis do código que exigem revisão humana.

- **Interpretação**  
  Ausência total de revisão aumenta risco potencial.

- **Avaliação:** **Ruim**

---

### 4.3.9 Tamanho do Projeto — ~21.000 linhas

- **Valor obtido:** ~21k LOC

- **Conceito**  
  Volume total de código analisado.

- **Interpretação**  
  Contextualiza os indicadores: para esse tamanho, os valores encontrados são
  considerados altos.

---

## 4.4 Métricas Não Mensuráveis no Contexto Deste Estudo

Conforme definido no planejamento da Fase 3, algumas métricas dependem de ambiente em produção ou de informações técnicas que não estão disponíveis para a equipe de avaliação. Por esse motivo, não foi possível mensurá-las nesta fase.



### Disponibilidade (M1.1 – Availability Rate %)

Para medir a disponibilidade seria necessário monitorar o endpoint principal do sistema. No entanto, a documentação consultada não apresentou o endpoint oficial da aplicação, o que impossibilitou a configuração de ferramentas de monitoramento, como o UptimeRobot. Uma alternativa seria utilizar ferramentas externas de inspeção de tráfego, como o Fiddler, para tentar identificar o endpoint real. Ainda assim, mesmo que esse endpoint fosse descoberto, seria indispensável a confirmação da equipe de desenvolvimento para validar se ele corresponde de fato ao ambiente de produção. Sem essa validação, os dados obtidos não poderiam ser considerados confiáveis.



### Tolerância a Falhas (M2.1/M2.2 – Erros sem queda e com queda)

Para avaliar a tolerância a falhas seria necessário acesso direto ao código em execução ou aos logs de produção, o que não estava disponível para a equipe de avaliação. Uma alternativa seria solicitar à equipe de desenvolvimento que configurasse ferramentas de monitoramento, como o Sentry, para registrar erros e falhas. No entanto, devido ao tempo reduzido para a execução da avaliação, não foi viável abrir essa solicitação e aguardar a implementação. Por esse motivo, a métrica foi declarada como não mensurável nesta fase.

---

## 4.5 Respostas às Questões GQM

### Q1. O sistema está disponível para uso na maior parte do tempo?

- **Resposta:** Não mensurável  
- **Justificativa:** A ausência de informações sobre o endpoint oficial impossibilitou a configuração de monitoramento de disponibilidade. Embora seja tecnicamente possível descobrir o endpoint por meio de ferramentas externas usando o Fiddler, por exemplo, seria necessária a validação da equipe de desenvolvimento para garantir que o monitoramento reflita o ambiente real de produção. Sem essa confirmação, os dados não podem ser considerados confiáveis.

---

### Q2. O sistema continua operando diante de falhas parciais?

- **Resposta:** **Não**

- **Justificativas:**
  - duplicação excessiva (39.1%)  
  - muitos _code smells_ (355)  
  - ausência de testes (0%)  
  - presença de bugs críticos  
  - confiabilidade classificada como D  

---

### Q3. O sistema apresenta baixa incidência de bugs?

- **Resposta:** **Não**

- **Justificativas:**
  - 206 _bugs_  
  - 1 _high issue_  
  - _Reliability Rating_ = D  

---

## 4.6 Conclusão da Fase 4

A execução da análise estática evidenciou que o nível de **Confiabilidade** é
considerado **baixo** no estado atual do código.

### Síntese:

- elevado número de bugs  
- forte duplicação  
- ausência de testes automatizados  
- pontos críticos sem revisão  
- confiabilidade classificada como D  

### Recomendações:

- criar suíte mínima de testes  
- refatorar trechos duplicados  
- corrigir _bugs_ críticos  
- revisar _security hotspots_  
- reduzir complexidade estrutural  

---

## 4.7 Histórico de Versões

| Versão | Data       | Descrição | Autor |
| ------ | ---------- | --------- | ----- |
| `1.0`  | 25/11/2025 | Execução da Avaliação – Confiabilidade | [Uires Carlos de Oliveira](https://github.com/uires2023) |
| `1.1`  | 26/11/2025 | Adiciona a conclusão sobre as métricas não mensuráveis | [Matheus Henrick](https://github.com/MatheusHenrickSantos) |