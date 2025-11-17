# 4. Segurança - Planejamento da Coleta

## 4.1 Introdução

Esta fase descreve como será realizada a coleta dos dados necessários para avaliar a característica Segurança do sistema Guardiões da Saúde, conforme o objetivo GQM definido na Fase 2. O planejamento considera as métricas selecionadas (M1.1, M1.2, M1.3 e M3.1), bem como as restrições das ferramentas disponíveis e a necessidade de garantir que a coleta seja reprodutível, objetiva e sustentada por evidências.  
A coleta envolve tanto métodos automatizados (via análise SAST) quanto inspeções manuais em trechos críticos do código, assegurando cobertura adequada das subcaracterísticas de confidencialidade, integridade, autenticação e rastreabilidade.

---

## 4.2 Operacionalização das Métricas

As métricas serão operacionalizadas conforme sua natureza:

As métricas **M1.1, M1.2 e M1.3** serão obtidas automaticamente por meio de análise estática do código, utilizando os relatórios gerados pelo SonarQube. Esses relatórios já fornecem diretamente a contagem de vulnerabilidades por severidade, sua classificação conforme o OWASP Top 10, e o percentual de hotspots revisados, permitindo extração objetiva dos valores.

A métrica **M3.1**, por sua vez, exige inspeção manual, pois visa verificar a existência de mecanismos de log/auditoria em módulos sensíveis. Isso envolve leitura direcionada do código, especialmente em rotinas de autenticação e manipulação de dados.

Cada métrica será registrada na planilha de coleta, sempre associada à questão GQM correspondente e à hipótese avaliada.

---

## 4.3 Ferramentas de Coleta

- **SonarQube (SAST + Hotspots)**  
  Responsável pela coleta automática de vulnerabilidades, classificação OWASP e análise de hotspots.

- **Navegador do GitHub / Editor de código**  
  Utilizado para inspeção manual de trechos relevantes ao logging (M3.1).

- **Google Docs / Excel**  
  Para o registro e consolidação dos resultados das métricas.

- **Repositório GitHub (pasta `/docs/evidencias/seguranca/`)**  
  Armazenamento oficial das evidências, relatórios e capturas de tela da análise.

O uso combinado dessas ferramentas garante precisão, rastreabilidade e transparência na coleta dos dados.

---


## 4.4 Procedimentos de Coleta

O processo de coleta será executado na seguinte ordem:

1. Importação do código no SonarQube e execução completa da análise SAST.  
2. Extração dos resultados referentes às métricas M1.1, M1.2 e M1.3 diretamente do dashboard da ferramenta.  
3. Captura das evidências (prints, relatórios, telas do SonarQube) e armazenamento padronizado.  
4. Inspeção manual de módulos críticos para a métrica M3.1, verificando presença ou ausência de mecanismos de log.  
5. Registro dos dados na planilha de coleta, incluindo resultados, data, responsável e evidência associada.  
6. Validação interna para garantir que todas as métricas estejam respaldadas por prova documental.

Esse fluxo garante consistência e minimiza subjetividade na avaliação.

---

## 4.5 Armazenamento de Dados

Todos os dados coletados serão organizados em dois repositórios principais:

### **Planilha de Coleta (Google Docs / Excel)**
Conterá:  
- ID da métrica  
- questão associada  
- valor obtido  
- interpretação preliminar  
- responsável  
- link da evidência  

### **Pasta de Evidências no GitHub**
Local: `docs/evidencias/seguranca/`  
Armazenará:

- capturas de tela do SonarQube  
- exportações de relatórios  
- trechos de código relevantes (para M3.1)  
- registros das inspeções manuais  

A estrutura é projetada para garantir rastreabilidade, facilidade de consulta e padronização para auditorias.

---


## 4.6 Procedimentos Manuais

Para métricas que exigem inspeção manual (especialmente M3.1), será seguido o seguinte fluxo:

1. Identificar os módulos críticos relacionados à autenticação, envio de dados sensíveis e operações de backend.  
2. Realizar leitura direcionada do código, buscando chamadas a mecanismos de log, auditoria ou registro de eventos.  
3. Verificar se os logs incluem informações essenciais como timestamp, identificação do ator e ação realizada.  
4. Capturar evidências (prints ou trechos de código) e armazená-las no repositório oficial.  
5. Registrar na planilha o resultado qualitativo (“Sim” ou “Não”), bem como a evidência correspondente.

Esse processo assegura que mesmo métricas subjetivas sejam tratadas com rigor e documentação apropriada.

## 4.7 Histórico de Versões

| Versão | Data       | Descrição            | Autor(es)                                          |
| ------ | ---------- | -------------------- | -------------------------------------------------- |
| `1.0`  | 15/11/2025 | Criação do documento | [Arthur Carneiro](https://github.com/trindadea)   |
| `1.1`  | 17/11/2025 | Segurança | [Guilherme Coelho Mendonça](https://github.com/Guilermanoo)   |
