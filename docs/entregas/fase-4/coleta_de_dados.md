

# FASE 4 – CONFIABILIDADE - Executar o Planejamento (Execução + Análise + Interpretação)

Nesta fase são exibidas as **evidências**, os **dados coletados** e a **interpretação dos resultados** referentes à análise da Confiabilidade.

---

## 1. Gravações das coletas e execução dos testes

A análise foi realizada no Ubuntu, com o SonarQube iniciado via: ./sonar.sh start

Etapas executadas:

1. Acesso ao painel web  
2. Execução do SonarScanner  
3. Processamento de mais de 21.000 linhas  
4. Geração dos dashboards

### Prints que devem ser adicionados ao GitPages:

- Dashboard geral  
- Aba "Bugs"  
- Aba "Reliability"  
- Aba "Code Smells"  
- Aba "Duplications"

## **📸 Evidência – Dashboard Geral do Projeto**

<p align="center">
  <img src="..docs/assets/images/sonar_resultado.jpeg" width="85%">
  <br>
  <strong>Figura 1 – Dashboard geral do Guardiões da Saúde – App no SonarQube</strong>
</p>

> *(Substitua o caminho pelo local onde você salvar o arquivo no repositório)*  
Exemplo usado: `docs/assets/images/sonar_resultado.jpeg`

---

## 🎥 **Evidência em Vídeo – Execução da Análise**

Para assistir ao vídeo da execução real da análise no SonarQube, clique abaixo:

👉 **[▶️ Assistir vídeo da análise](../evidencias/confiabilidade/sonar-analise.mp4)**

> *(Depois que você subir o arquivo para o GitHub, renomeie para `sonar-analise.mp4` ou ajuste o caminho.)*

---

---

## 2. Dados coletados (métricas reais do SonarQube)

### ✔ Maturidade

| Métrica | Valor |
|--------|--------|
| Bugs detectados | **206** |
| Severidade | Critical / Major |
| Reliability Rating | **D** |

---

### ✔ Disponibilidade (estrutura do código)

| Métrica | Valor |
|--------|--------|
| Build Blockers | **0** |
| Erros Críticos | Presentes |
| Cobertura de Testes | **0%** |
| Uptime (%) | **Não mensurável** |

---

### ✔ Tolerância a Falhas

| Métrica | Valor |
|--------|--------|
| Code Smells | **355** |
| Duplicação de Código | **39.1%** |
| Complexidade | Elevada |

---

## 3. Interpretação das métricas

### ✔ Maturidade – Baixa  
Alto volume de bugs e erros críticos compromete a robustez.

### ✔ Disponibilidade – Comprometida  
Sem testes, com erros críticos e duplicação elevada, a estabilidade real do app é afetada.

### ✔ Tolerância a Falhas – Insuficiente  
Code smells, duplicação e alta complexidade indicam fragilidade no tratamento de erros.

---

## 4. Respostas das Questões GQM

- **Q1:** O sistema apresenta erros que comprometem a operação?  
  **Sim** – 206 bugs, incluindo críticos.

- **Q2:** O código possui fragilidades que afetam a disponibilidade?  
  **Sim** – ausência de testes e erros críticos.

- **Q3:** O sistema é tolerante a falhas?  
  **Não** – muitos smells e duplicação elevada.

---

## 5. Conclusão da Fase 4

Os resultados obtidos mostram:

- Baixa maturidade  
- Disponibilidade estrutural comprometida  
- Baixa tolerância a falhas  
- Alta complexidade e duplicação  
- Ausência de testes

➡ **Conclusão geral:** O nível de Confiabilidade do Guardiões da Saúde – App é **insatisfatório**, exigindo refatorações e implantação de testes.



## Histórico de Versões
| Versão | Data | Descrição | Autor(es) |
| ------ | ---- | --------- | --------- |