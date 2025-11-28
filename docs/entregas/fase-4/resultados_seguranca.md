<!-- # Segurança - Execução, Análise e Interpretação

## 1. Introdução
_Objetivo, escopo e relação com o plano da Fase 3. Liste aqui o que é mensurável/não mensurável._

## 2. Ambiente e Recursos
- SO, versões de ferramentas (ex.: SonarQube/Scanner ou SonarCloud), commit/branch analisado.
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
| (ex.: Vulnerabilidades por severidade, OWASP Top 10, Hotspots revisados, Logs/Auditoria) | | | | |

### 5.1 Métricas não mensuráveis (se houver)
- Descrever e justificar.

## 6. Respostas às Questões GQM
- Q1 …
- Q2 …
- Q3 …
- Q4 …

## 7. Conclusão e Recomendações
- Síntese do nível de Segurança.
- 3–5 ações priorizadas.

## 8. Histórico de Versões
| Versão | Data       | Descrição                      | Autor(es) |
| ------ | ---------- | ------------------------------ | --------- |
| `1.0`  | 27/11/2025 | Criação do documento | [Arthur Carneiro](https://github.com/trindadea)   | -->

# 4. Segurança – Execução da Avaliação
Nesta fase são exibidas as **evidências**, os **dados coletados** e a **interpretação dos resultados** referentes à análise da Segurança.

---
## 4.1 Gravações da coleta e execução dos testes
A análise foi realizada online, utilizando o [SonarQube Cloud](https://sonarcloud.io/)

Etapas executadas:
1. Fork do [repositório](https://github.com/ProEpiDesenvolvimento/guardioes-app). [^Porque?]
2. Acesso ao SonarQube Cloud
3. Criação de um projeto relacionado ao repositório clonado
4. Execução do SonarScanner 
5. Processamento de mais de 21.000 linhas  
6. Geração dos dashboards

[^Porque?]: Necessário, pois o SonarQube Cloud não permite analisar repositórios que você não administra.

### Evidências em Foto

<div align="center">
  <p><strong>Figura 1 – Dashboard geral do Guardiões da Saúde – App no SonarQube.</strong></p>
</div>
<div align="center">
  <img src="../../../assets/evidencias/seguranca/m11_seg_sonar_dashboard.png" width="750" alt="Dashboard geral do Guardiões da Saúde – App no SonarQube">
</div>
<div align="center" style="font-size: 12px; font-style: italic;">
  Fonte: Autores.
</div>

<div align="center">
  <p><strong>Figura 2 – Número de vulnerabilidades de segurança - App no SonarQube.</strong></p>
</div>
<div align="center">
  <img src="../../../assets/evidencias/seguranca/m11_seg_vulnerabilities.png" width="750" alt="Vulnerabilidades de segurança no SonarQube">
</div>
<div align="center" style="font-size: 12px; font-style: italic;">
  Fonte: Autores.
</div>

<div align="center">
  <p><strong>Figura 3 – Security Hotspots – App no SonarQube.</strong></p>
</div>
<div align="center">
  <img src="../../../assets/evidencias/seguranca/m13_seg_hotspots.png" width="750" alt="Security Hotspots no SonarQube">
</div>
<div align="center" style="font-size: 12px; font-style: italic;">
  Fonte: Autores.
</div>

<div align="center">
  <p><strong>Figura 4 – Vulnerabilidades OWASP Top 10 – App no SonarQube.</strong></p>
</div>
<div align="center">
  <img src="../../../assets/evidencias/seguranca/m12_seg_owasp_top10.png" width="750" alt="Vulnerabilidades OWASP Top 10 no SonarQube">
</div>
<div align="center" style="font-size: 12px; font-style: italic;">
  Fonte: Autores.
</div>


---

### Evidências em Vídeo

Para assistir ao vídeo da execução real da análise no SonarQube, clique abaixo:

<div align="center">
  <p><strong>Vídeo 1 – Execução da análise de segurança no SonarQube.</strong></p>
</div>
<div align="center">
  <video width="750" controls>
    <source src="../../../assets/evidencias/seguranca/m1x_seg_sonar_analysis.mp4" type="video/mp4" />
    Seu navegador não suporta a reprodução de vídeo.
  </video>
</div>
<div align="center" style="font-size: 12px; font-style: italic;">
  Fonte: Autores.
</div>


---
## 4.2 Dados coletados
### 4.2.1 Via SonarQube

<div align="center">
  <p><strong>Tabela 1 – Métricas de segurança coletadas via SonarQube.</strong></p>
</div>

| Métrica                                                    | Valor        |
|------------------------------------------------------------|--------------|
| N° de vulnerabilidades **Críticas** encontradas            | **0**        |
| N° de vulnerabilidades **Altas** encontradas               | **0**        |
| Tipos de Vulnerabilidades OWASP Top 10 (`A01,A02,A03,A07`) | `0, 0, 0, 0` |
| Percentual de Security Hotspots Revisados                  | **100%**     |

### 4.2.2 Via Inspeção Manual

<div align="center">
  <p><strong>Tabela 2 – Métrica de segurança coletada via inspeção manual.</strong></p>
</div>

| Métrica                                | Valor   |
|----------------------------------------|---------|
| Implementa mecanismos de Log/Auditoria | **Não** |

<div align="center" style="font-size: 12px; font-style: italic;">
  Fonte: Autores.
</div>

---
## 4.3 Interpretação das métricas
### ✔ Integridade – Alta
A ausência de vulnerabilidades de Injeção (`A03`) e de Quebra de Controle de Acesso (`A01`) indica que o código é robusto contra manipulações indevidas ou alterações não autorizadas de dados via exploração técnica.

### ✔ Confidencialidade – Alta
Com zero falhas criptográficas (`A02`) e zero problemas de identificação/autenticação (`A07`), o sistema demonstra proteger adequadamente o acesso aos dados sensíveis contra vazamentos técnicos detectáveis estaticamente.

### ✔ Rastreabilidade – Inexistente
A falta completa de mecanismos de Log e Auditoria (identificada na inspeção manual) torna impossível o rastreio de ações de usuários, impedindo a imputabilidade (saber "quem fez o quê") e a investigação de incidentes.

---
## 4.4 Respostas das Questões GQM
- **Q1.** O sistema protege adequadamente os dados sensíveis dos usuários?
**Sim** - O sistema não apresenta vulnerabilidades conhecidas relacionadas a Falhas Criptográficas.

- **Q2.** O sistema garante que os dados não sejam alterados indevidamente?
**Sim** - Não foram identificadas vulnerabilidades nas categorias de Quebra de Controle de Acesso ou Injeção.

- **Q3.** As ações dos usuários e do sistema são rastreáveis e auditáveis?
**Não** - A inspeção manual identificou explicitamente que o sistema **não implementa mecanismos de Log/Auditoria** no contexto de segurança.

- **Q4.** O sistema verifica corretamente a identidade dos usuários?
**Sim** - O sistema não apresenta vulnerabilidades conhecidas relacionadas a Falhas de Identificação e Autenticação.

---
## 4.5 Conclusão da Fase 4
Os resultados obtidos mostram:

- **Alta maturidade de código** (Zero vulnerabilidades críticas ou altas detectadas).
- **Integridade e Confidencialidade preservadas** contra ataques técnicos comuns (OWASP Top 10).
- **Rastreabilidade inexistente** devido à falta de mecanismos de log.
- **Monitoramento comprometido**, impossibilitando auditorias de segurança.

> ➡ **Conclusão geral:** O nível de Segurança do aplicativo é **parcial**. Embora a estrutura do código demonstre excelente robustez contra invasões, a ausência de mecanismos de auditoria (Logs) cria um "ponto cego" crítico, exigindo a implementação urgente de registros de atividades para garantir conformidade e detecção de incidentes.

---
# 4.6 Histórico de Versões
| Versão | Data       | Descrição                                           | Autor(es)                                      |
|--------|------------|-----------------------------------------------------|------------------------------------------------|
| `1.0`  | 24/11/2025 | Criação do Documento                                | [Caio Pacheco](https://github.com/CaioPacheco) |
| `1.1`  | 25/11/2025 | Adição das Etapas, Dados, Interpretação e Conclusão | [Caio Pacheco](https://github.com/CaioPacheco) |
| `1.2`  | 26/11/2025 | Adição das Evidências                               | [Caio Pacheco](https://github.com/CaioPacheco) |
