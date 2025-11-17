# 3. Confiabilidade - Planejamento da Coleta

## 3.1 Introdução

A Fase 3 define como serão coletados, organizados e registrados os dados referentes à característica Confiabilidade, aplicada ao projeto Guardiões da Saúde – App.
As subcaracterísticas avaliadas são:

Maturidade
Disponibilidade
Tolerância a Falhas

## 3.2 Operacionalização das Métricas

A coleta será realizada através de análise estática do código, utilizando o SonarQube para medir:

quantidade e severidade de bugs

duplicação de código

code smells

complexidade

riscos de falha

confiabilidade estrutural do sistema

Como não há ambiente de produção, algumas métricas de runtime (ex.: uptime e erros Sentry) serão classificadas como não mensuráveis no contexto da análise estática.

Operacionalização por subcaracterística:

➤ Maturidade
Identificar bugs, severidades e impacto no funcionamento.

➤ Disponibilidade
Avaliada como “resiliência estrutural”, considerando:
blockers
erros críticos
ausência de testes
fragilidade na inicialização
Uptime real (Availability %) → Não mensurável.

➤ Tolerância a Falhas
Avaliar:
code smells
duplicação
complexidade
tratamento de erros

## 3.3 Ferramentas de Coleta

- SonarQube Community Edition
- Principal ferramenta de análise estática.

- SonarScanner
- Responsável por enviar o código ao SonarQube.

- GitHub
- Para obtenção do código-fonte.

- GitHub Pages / Docs
- Para armazenamento das evidências.

## 3.4 Procedimentos de Coleta

Clonar o repositório do app.
Iniciar o SonarQube no Ubuntu (./sonar.sh start).
Acessar http://localhost:9000.
Criar o projeto no Sonar.
Executar a análise com SonarScanner.
Aguardar o processamento.
Coletar prints e métricas.
Registrar tudo no GitPages.

## 3.5 Armazenamento de Dados

GitHub Pages (aba Fase 4)
Pasta /docs/evidencias no GitHub
Prints arquivados em PNG
PDF final (opcional)
Planilha Excel (opcional)

## 3.6 Procedimentos Manuais
Fluxo manual complementa o processo automático:
Rodar SonarScanner
Abrir painel do SonarQube
Acessar: Bugs / Reliability / Smells / Duplications
Capturar prints das telas
Registrar métricas nas tabelas
Publicar no GitPages

🟩 Métricas Planejadas (GQM)
✔ Maturidade
M1.1: Quantidade total de bugs
M1.2: Severidade dos bugs (Critical / Major / Minor)

✔ Disponibilidade (estrutura do código)
M2.1: Quantidade de erros críticos
M2.2: Erros bloqueadores de execução
M2.3: Ausência de testes / riscos de instabilidade

✔ Disponibilidade (não mensurável via UptimeRobot)
M1.1 – Availability (%) → Não mensurável
Motivo: app não possui endpoint monitorável.
✔ Erros de runtime (não mensuráveis)
M2.1 – Erros sem queda (Sentry)
M2.2 – Crashes (Sentry)
Motivo: exigem telemetria em produção, não disponível.

✔ Tolerância a Falhas
M3.1: Code Smells relacionados a exceções
M3.2: Duplicação de código
M3.3: Complexidade ciclomática


## 3.7 Histórico de Versões

| Versão | Data       | Descrição            | Autor(es)                                          |
| ------ | ---------- | -------------------- | -------------------------------------------------- |
| `1.0`  | 15/11/2025 | Criação do documento | [Arthur Carneiro](https://github.com/trindadea)   |
