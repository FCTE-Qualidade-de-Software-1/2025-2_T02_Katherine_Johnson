

# FASE 4 — EXECUÇÃO DA AVALIAÇÃO (CONFIABILIDADE)

Esta fase apresenta a execução prática do planejamento definido na Fase 3, incluindo a coleta real das métricas via SonarQube Community Edition, a interpretação dos resultados e as respostas às questões GQM.

Conforme estabelecido nas fases anteriores:

Métricas dependentes de produção → não mensuráveis.

Métricas baseadas em código-fonte → mensuráveis e analisadas aqui.

## 1. Evidências da Execução

A análise foi realizada no Ubuntu através dos comandos:

./sonar.sh start
sonar-scanner


Etapas realizadas:

Inicialização do SonarQube local

Execução do SonarScanner

Processamento de ~21k linhas

Geração dos dashboards

Coleta das métricas e imagens

As figuras utilizadas abaixo foram extraídas do SonarQube durante a análise.

## 2. Métricas Coletadas e Interpretação

A seguir, cada métrica é apresentada com:

Figura correspondente

 Valor obtido

Conceito

Interpretação

## Avaliação

### 2.1 Reliability Rating — D

📸 Figura: “Reliability – D (1 high issue)”

Valor obtido:

Reliability: D

Bugs: 206

High issues: 1

Conceito:
Avalia a probabilidade de falhas com base na quantidade e severidade dos bugs.

Interpretação:
Nota D indica que há bugs relevantes com risco de causar falhas reais.

Avaliação: 🟥 Ruim

### 2.2 Bugs — 206

📸 Figura: Dashboard Geral

Valor obtido: 206 bugs

Conceito:
Erros que comprometem a execução ou lógica do sistema.

Interpretação:
Quantidade muito elevada, indicando fragilidade e baixo nível de robustez.

Avaliação: 🟥 Ruim

### 2.3 Maintainability Rating — A

📸 Figura: “Maintainability – A”

Valor obtido: A

Conceito:
Representa o esforço necessário para manter o código.

Interpretação:
Mesmo com muitos smells, o código é relativamente fácil de corrigir.

Avaliação: 🟩 Excelente

### 2.4 Code Smells — 355

📸 Figura: Dashboard Geral

Valor obtido: 355 code smells

Conceito:
Problemas que não causam falha imediata, mas afetam qualidade interna.

Interpretação:
Indica estrutura frágil e baixa qualidade interna.

Avaliação: 🟧 Regular → Ruim

### 2.5 Duplications — 39.1%

📸 Figura: “Duplications – >20%”

Valor obtido: 39.1%

Conceito:
Percentual de código duplicado no projeto.

Interpretação:
Extremamente alto, causa inconsistência e risco estrutural.

Avaliação: 🟥 Péssimo
(Pior indicador do projeto.)

### 2.6 Coverage — 0%

📸 Figura: “Coverage – 0%”

Valor obtido: 0%

Conceito:
Indica quanto do código é coberto por testes automatizados.

Interpretação:
Nenhum teste foi implementado.

Avaliação: 🟥 Péssimo

### 2.7 Security Rating — A

📸 Figura: “Security – A”

Valor obtido: A

Conceito:
Avalia vulnerabilidades reais no código.

Interpretação:
Nenhuma vulnerabilidade detectada.

Avaliação: 🟩 Excelente

### 2.8 Security Hotspots Reviewed — E

📸 Figura: “Security Hotspots – E (<30%)”

Valor obtido: E (0% revisado)

Conceito:
Hotspots são áreas sensíveis que precisam ser revisadas manualmente.

Interpretação:
Nenhum hotspot revisado, indicando falta de atenção no processo de segurança.

Avaliação: 🟥 Ruim

### 2.9 Project Size — ~21.000 linhas

📸 Figura: “Size”

Conceito:
Representa o volume de código analisado.

Interpretação:
Serve como base para avaliar se os valores estão altos ou baixos — para este tamanho, os números de bugs e smells são considerados elevados.

## 3. Respostas às Questões GQM
Q1 — O sistema está disponível para uso na maior parte do tempo?

Resposta: ❌ Não mensurável
Conforme definido na Fase 3, depende de ambiente de produção (uptime).

Q2 — O sistema tolera falhas e continua operando?

Resposta: ❌ Não

Justificativas estruturais:

39.1% de duplicação

355 code smells

0% de testes

alta complexidade

presença de bugs críticos

Q3 — O sistema apresenta baixa incidência de bugs que impactem a operação?

Resposta: ❌ Não

Motivos:

206 bugs

1 high issue

Reliability Rating = D

## 4. Conclusão da Fase 4

Com base nas métricas coletadas:

🟥 Confiabilidade geral: Baixa
Principais evidências:

Alta quantidade de bugs (206)

Alta duplicação (39.1%)

Zero cobertura de testes (0%)

Número elevado de code smells (355)

Nota D em confiabilidade

Segurança não revisada (Hotspots = E)

O sistema apresenta sinais claros de fragilidade, baixa robustez e alto risco de falhas operacionais.

Recomendações:

Implantar testes automatizados

Refatorar áreas duplicadas

Reduzir complexidade

Revisar hotspots de segurança

Corrigir bugs prioritários



## Histórico de Versões
| Versão | Data | Descrição | Autor(es) |
| 1.0 | 25/11/2025 | Fase 4 Confiabilidade | Uires Carlos |