# 3. Confiabilidade - Planejamento da Coleta

## 3.1 Introdução

A Fase 3 define como serão coletados, organizados e registrados os dados referentes à característica **Confiabilidade**, aplicada ao projeto **Guardiões da Saúde – App**.  
As subcaracterísticas avaliadas são:

- **Maturidade**
- **Disponibilidade**
- **Tolerância a Falhas**

## 3.2 Operacionalização das Métricas

A coleta será realizada através de **análise estática do código**, utilizando o **SonarQube** para medir:

- quantidade e severidade de bugs  
- duplicação de código  
- _code smells_  
- complexidade  
- riscos de falha  
- confiabilidade estrutural do sistema

Como não há ambiente de produção, métricas de _runtime_ (como _uptime_ e erros Sentry) serão classificadas como **não mensuráveis no contexto da análise estática**.

### Operacionalização por subcaracterística

#### Maturidade  
Identificar bugs, severidades e impacto no funcionamento.

#### Disponibilidade  
Avaliada como “resiliência estrutural”, considerando:

- _blockers_  
- erros críticos  
- ausência de testes  
- fragilidade na inicialização

**_Uptime real_ (_Availability_ %)** → *Não mensurável*.

#### Tolerância a Falhas  
Avaliar:

- _code smells_  
- duplicação  
- complexidade  
- tratamento de erros

---


## 3.3 Ferramentas de Coleta

- **SonarQube Community Edition** – ferramenta principal  
- **SonarScanner**  
- **GitHub** – fonte do código  
- **GitHub Pages** – armazenamento das evidências

## 3.4 Procedimentos de Coleta

1. Clonar o repositório do app.  
2. Iniciar o SonarQube no Ubuntu (`./sonar.sh start`).  
3. Acessar `http://localhost:9000`.  
4. Criar o projeto no SonarQube.  
5. Executar o SonarScanner.  
6. Coletar métricas e prints.  
7. Publicar no GitPages.

---
## 3.5 Armazenamento de Dados

- Arquivos e prints no **GitHub Pages**  
- Evidências no diretório `/docs/evidencias`  
- Planilha Excel/PDF (opcional)

---

## 3.6 Procedimentos Manuais
1. Rodar SonarScanner  
2. Abrir painel do Sonar  
3. Acessar Bugs, Reliability, Smells e Duplications  
4. Capturar prints  
5. Montar tabelas  
6. Publicar no GitPages

---

## Métricas Planejadas (GQM)

### Disponibilidade (não mensurável via UptimeRobot)
- [M1.1: _Availability Rate_ (%)](../fase-2/confiabilidade.md#m11conf) – Não mensurável  

> Observação: a medição de _Availability_ (_uptime_) requer um _endpoint_ em execução contínua e monitoramento externo, (por exemplo, UptimeRobot). Como o repositório disponibiliza apenas o código‑fonte, não há ambiente de produção nem informação sobre qual endpoint principal deve ser monitorado; por isso, a [métrica M1.1](../fase-2/confiabilidade.md#m11conf) foi classificada como “não mensurável no contexto deste estudo (análise estática do código)”.

### Tolerância a Falhas (Erros de _runtime_) (não mensuráveis)
- [M2.1: Erros sem queda](../fase-2/confiabilidade.md#m21conf) (Sentry) – Não mensurável: requer integração com Sentry/telemetria e acesso aos logs de produção.
- [M2.2: Crashes](../fase-2/confiabilidade.md#m22conf) (Sentry) – Não mensurável: requer integração com Sentry/telemetria e acesso aos logs de produção.

> Observação: O repositório GitHub também não registra automaticamente erros de execução. As métricas de erros sem queda ([M2.1](../fase-2/confiabilidade.md#m21conf)) e com queda ([M2.2](../fase-2/confiabilidade.md#m22conf)) exigem a integração prévia do app com um serviço de monitoramento (por exemplo, Sentry) e coleta de dados de uso real pelos usuários.
Como o trabalho está focado na análise estática via SonarQube, sem acesso ao ambiente de produção e, consequentemente, aos logs do Sentry, essas métricas não puderam ser coletadas e foram marcadas como “não mensuráveis com os dados disponíveis”.

### Tolerância a Falhas

- M3.1: Code Smells relacionados a exceções
- M3.2: Duplicação de código
- M3.3: Complexidade ciclomática

### Maturidade (SonarQube)
- [M3.1: Quantidade total de _bugs_](../fase-2/confiabilidade.md#m31conf)  
- [M3.2: Severidade dos _bugs_](../fase-2/confiabilidade.md#m32conf) (Critical / Major / Minor)

---


## 3.7 Histórico de Versões

| Versão | Data       | Descrição            | Autor(es)                                          |
| ------ | ---------- | -------------------- | -------------------------------------------------- |
| `1.0`  | 15/11/2025 | Criação do documento | [Arthur Carneiro](https://github.com/trindadea)   |
| `1.2`  | 17/11/2025 | Confiabilidade pontos | [Uires Carlos de oliveira](https://github.com/uires2023)   |
| `1.3`  | 17/11/2025 | Adiciona justificativas e links | [Matheus Henrick](https://github.com/MatheusHenrickSantos) |
