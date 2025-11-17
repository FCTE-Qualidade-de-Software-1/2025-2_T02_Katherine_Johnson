## Histórico de Versões


Nesta fase são exibidas as evidências, os dados coletados e a interpretação dos resultados referentes à análise da Confiabilidade.

🔹 1. Gravações das coletas e execução dos testes

A análise foi realizada no Ubuntu.
O SonarQube foi iniciado com sucesso:

./sonar.sh start
SonarQube is running


Etapas executadas:

Acesso ao painel web

Execução do SonarScanner

Processamento de 21.000+ linhas

Geração de métricas completas

🔸 Prints que devem ser incluídos no GitPages:

Dashboard geral do SonarQube

Aba "Bugs"

Aba "Reliability"

Aba "Code Smells"

Aba "Duplications"

(Os prints você cola no seu GitPages.)

🔹 2. Dados coletados (métricas reais do SonarQube)
🟩 Maturidade
Métrica	Valor
Bugs detectados	206
Severidade	Critical / Major
Reliability Rating	D
🟩 Disponibilidade (estrutura do código)
Métrica	Valor
Build Blockers	0
Erros Críticos	Presentes
Cobertura de Testes	0%
Uptime (%)	Não mensurável
🟩 Tolerância a Falhas
Métrica	Valor
Code Smells	355
Duplicação de Código	39.1%
Complexidade	Elevada
🔹 3. Análise das métricas (interpretação)
✔ Maturidade – Baixa

Alto volume de bugs

Presença de falhas críticas

Reliability Rating = D

➡ Indica baixa robustez e necessidade de correções.

✔ Disponibilidade – Comprometida

Ausência total de testes

Erros críticos

Estrutura frágil

Uptime e telemetria não disponíveis

➡ Em ambiente real, a disponibilidade seria prejudicada.

✔ Tolerância a Falhas – Insuficiente

Muitos code smells

Duplicação elevada

Complexidade alta

Ausência de mecanismos robustos de tratamento de exceções

➡ O sistema não tolera falhas de forma eficiente.

🔹 4. Resposta das Questões GQM
● Q1 – O sistema apresenta erros que comprometem a operação?

Sim. Foram encontrados 206 bugs.

● Q2 – O código possui fragilidades que afetam a disponibilidade?

Sim. A ausência de testes e erros críticos prejudicam a estabilidade.

● Q3 – O sistema é tolerante a falhas?

Não. Há muitos smells, duplicação e complexidade elevada.

🔹 5. Conclusão da Fase 4

Os resultados mostraram:

Baixa maturidade

Baixa tolerância a falhas

Estrutura insuficiente para garantir disponibilidade

Código com alto risco de falhas

Solução exige refatoração e testes urgentes

➡ Conclusão geral: O nível de Confiabilidade do Guardiões da Saúde – App é insatisfatório.

| Versão | Data | Descrição | Autor(es) |
| ------ | ---- | --------- | --------- |