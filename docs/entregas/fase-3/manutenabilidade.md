# 2. Manutenabilidade - Planejamento da Coleta

A Fase 3 define como serão coletados, organizados e registrados os dados referentes à característica Confiabilidade, aplicada ao projeto Guardiões da Saúde – App.
As subcaracterísticas avaliadas são:

Maturidade

Disponibilidade

Tolerância a Falhas
## 2.1 Introdução

## 2.2 Operacionalização das Métricas

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

## 2.3 Ferramentas de Coleta

## 2.4 Procedimentos de Coleta

## 2.5 Armazenamento de Dados

## 2.6 Procedimentos Manuais

## 2.7 Histórico de Versões

| Versão | Data       | Descrição            | Autor(es)                                          |
| ------ | ---------- | -------------------- | -------------------------------------------------- |
| `1.0`  | 15/11/2025 | Criação do documento | [Arthur Carneiro](https://github.com/trindadea)   |
