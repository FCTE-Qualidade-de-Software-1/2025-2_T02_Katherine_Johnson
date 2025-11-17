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
- code smells  
- complexidade  
- riscos de falha  
- confiabilidade estrutural do sistema

Como não há ambiente de produção, métricas de runtime (como uptime e erros Sentry) serão classificadas como **não mensuráveis no contexto da análise estática**.

### Operacionalização por subcaracterística

#### ➤ Maturidade  
Identificar bugs, severidades e impacto no funcionamento.

#### ➤ Disponibilidade  
Avaliada como “resiliência estrutural”, considerando:

- blockers  
- erros críticos  
- ausência de testes  
- fragilidade na inicialização

**Uptime real (Availability %)** → *Não mensurável*.

#### ➤ Tolerância a Falhas  
Avaliar:

- code smells  
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

### ✔ Maturidade
- M1.1: Quantidade total de bugs  
- M1.2: Severidade dos bugs (Critical / Major / Minor)

### ✔ Disponibilidade (estrutura do código)
- M2.1: Quantidade de erros críticos  
- M2.2: Erros bloqueadores de execução  
- M2.3: Ausência de testes / riscos de instabilidade

### ✔ Disponibilidade (não mensurável via UptimeRobot)
- **Availability (%)** – Não mensurável  
  Motivo: app não possui endpoint monitorável.

### ✔ Erros de runtime (não mensuráveis)
- **Erros sem queda (Sentry)**  
- **Crashes (Sentry)**  

### ✔ Tolerância a Falhas
- M3.1: Code Smells relacionados a exceções  
- M3.2: Duplicação de código  
- M3.3: Complexidade ciclomática

---


## 3.7 Histórico de Versões

| Versão | Data       | Descrição            | Autor(es)                                          |
| ------ | ---------- | -------------------- | -------------------------------------------------- |
| `1.0`  | 15/11/2025 | Criação do documento | [Arthur Carneiro](https://github.com/trindadea)   |
| `1.2`  | 17/11/2025 | Confiabilidade pontos| [Uires Carlos de oliveira](https://github.com/uires2023)   |
