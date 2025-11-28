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



# Confiabilidade – Execução, Análise e Interpretação

## 1. Introdução

Este documento apresenta a execução da avaliação da característica **Confiabilidade**
do projeto **Guardiões da Saúde – App**, conforme o planejamento definido na **Fase 3**.
A avaliação foi conduzida por meio de **análise estática do código-fonte**, visando
coletar métricas objetivas, interpretar resultados e responder às questões do modelo **GQM**.

### Escopo da avaliação

- **Métricas mensuráveis (análise estática):**  
  _Bugs_, _Reliability Rating_, _Code Smells_, _Duplicação_, _Coverage_, _Maintainability_,
  _Security_, _Security Hotspots Reviewed_ e _Tamanho do código (LOC)_.

- **Métricas não mensuráveis (execução em produção / telemetria):**  
  **M1.1 – Availability Rate (%)**, **M2.1 – Erros sem queda**, **M2.2 – Crashes**.

Essas métricas foram classificadas como não mensuráveis pela ausência de ambiente em
produção, telemetria e logs de execução.

---

## 2. Ambiente e Recursos

- **Sistema Operacional:** Ubuntu Linux  
- **Ferramenta de análise:** SonarQube Community Build **v25.11.0.114957**  
- **Modo:** MQR  
- **Scanner:** SonarScanner  
- **Projeto:** `guardioes-app`  
- **URL do painel:** `http://localhost:9000/dashboard?id=guardioes-app&codeScope=overall`  
- **Branch/commit analisado:** *(informar, se aplicável)*

### Evidências
- Diretório de armazenamento: `/docs/assets/images/fase-4/`

---

## 3. Procedimentos Executados (reprodutibilidade)

1. Inicialização do SonarQube (`./sonar.sh start`).  
2. Acesso ao painel web (`http://localhost:9000`).  
3. Criação do projeto e configuração do token.  
4. Execução do **SonarScanner** no repositório clonado.  
5. Processamento de aproximadamente **21.000 linhas de código**.  
6. Registro dos dashboards e métricas.

### Desvios do plano
- Não houve coleta de métricas em produção, conforme previsto na Fase 3.

---

## 4. Evidências e Dados Brutos

- Prints dos dashboards:
  - Geral / Overview
  - Reliability
  - Maintainability
  - Security
  - Security Hotspots
  - Coverage
  - Duplications
  - Size / Languages
- Local: `/docs/assets/images/fase-4/`
- Planilhas/relatórios adicionais: *(não aplicável, se não houver)*

---

## 5. Métricas Coletadas

| Métrica | Valor | Evidência | Interpretação | Julgamento |
| --- | --- | --- | --- | --- |
| Bugs | 206 | Dashboard / Reliability | Volume alto de defeitos | Ruim |
| Reliability Rating | D | Aba Reliability | Alta probabilidade de falhas | Ruim |
| Code Smells | 355 | Dashboard | Qualidade interna baixa | Regular → Ruim |
| Duplicação | 39,1% | Aba Duplications | Código excessivamente repetido | Péssimo |
| Cobertura | 0% | Aba Coverage | Ausência de testes | Péssimo |
| Maintainability Rating | A | Aba Maintainability | Esforço baixo de correção | Excelente |
| Security Rating | A | Aba Security | Sem vulnerabilidades críticas | Excelente |
| Hotspots revisados | 0% (E) | Aba Security Hotspots | Risco não revisado | Ruim |
| Tamanho (LOC) | ~21k | Aba Size | Alta densidade de problemas | Contextual |

---

### 5.1 Métricas não mensuráveis

- **M1.1 – Availability Rate (%)**  
  Requer endpoint validado em produção e monitoramento contínuo (ex.: UptimeRobot).

- **M2.1 – Erros sem queda (runtime)**  
  Depende de telemetria e logs em produção (ex.: Sentry).

- **M2.2 – Crashes**  
  Exige ferramentas de monitoramento de falhas (ex.: Crashlytics/Sentry).

*Justificativa comum:* inexistência de ambiente de produção e instrumentação.

---

## 6. Respostas às Questões GQM

### Q1 — O sistema está disponível para uso na maior parte do tempo?
- **Resposta:** Não mensurável.  
- **Justificativa:** ausência de endpoint oficial e dados de produção.

### Q2 — O sistema continua operando diante de falhas parciais?
- **Resposta:** Não.  
- **Evidências:** duplicação (39,1%), 355 _smells_, 0% de cobertura, _high issue_ e _rating_ D.

### Q3 — O sistema apresenta baixa incidência de _bugs_?
- **Resposta:** Não.  
- **Evidências:** 206 _bugs_ e _Reliability Rating_ = D.

---

## 7. Conclusão e Recomendações

### Síntese
A **Confiabilidade** é considerada **baixa**, devido ao alto volume de defeitos,
duplicação elevada e ausência de testes automatizados.

### Ações priorizadas
1. Implementar testes automatizados (unitários e integração).  
2. Reduzir duplicação por refatoração.  
3. Priorizar correção de _bugs_ críticos e *high*.  
4. Tratar _code smells_ de maior impacto.  
5. Revisar manualmente _security hotspots_.

---

## 8. Histórico de Versões

| Versão | Data       | Descrição | Autor |
| ------ | ---------- | --------- | ----- |
| `1.0`  | 25/11/2025 | Execução da Avaliação – Confiabilidade | [Uires Carlos de Oliveira](https://github.com/uires2023) |
| `1.1`  | 26/11/2025 | Adiciona a conclusão sobre as métricas não mensuráveis | [Matheus Henrick](https://github.com/MatheusHenrickSantos) |
| `1.2` | 27/11/2025 | Execução e análise (SonarQube v25.11.0.114957) | Uires Carlos de Oliveira |
