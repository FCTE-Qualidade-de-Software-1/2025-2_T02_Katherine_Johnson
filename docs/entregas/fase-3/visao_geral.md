# 1. Planejamento da Avaliação

## 1.1 Objetivo

Esta fase tem como objetivo **operacionalizar as métricas definidas na Fase 2** em procedimentos executáveis, estabelecendo critérios claros para coleta e análise de evidências, garantindo a rastreabilidade entre objetivos, questões e métricas. A **reproduzibilidade** é um aspecto fundamental deste planejamento, exigindo que todos os procedimentos estejam documentados em um nível de detalhamento que permita a reprodução exata dos testes realizados, permitindo que qualquer avaliador possa replicar os mesmos resultados seguindo os procedimentos estabelecidos.

Para atingir esse objetivo, será necessário:

-   **Definir procedimentos detalhados** para coleta de cada métrica;
-   **Especificar ferramentas e configurações** necessárias para execução;
-   **Estabelecer critérios de coleta** e validação de dados;
-   **Documentar o fluxo de trabalho** completo, incluindo etapas manuais quando aplicável;
-   **Definir estratégias de armazenamento** e organização dos dados coletados.

---

## 1.2 Metodologia

A metodologia adotada nesta fase segue uma abordagem **sistemática e estruturada**, baseada nos princípios estabelecidos na Fase 2 através do modelo **GQM (Goal-Question-Metric)**.

As métricas que serão operacionalizadas nesta fase foram previamente definidas na Fase 2, onde cada característica de qualidade possui suas métricas específicas detalhadas: [Manutenibilidade](../fase-2/manutenabilidade.md#25-métricas), [Confiabilidade](../fase-2/confiabilidade.md#35-métricas) e [Segurança](../fase-2/seguranca.md#45-métricas). Cada uma dessas métricas será transformada em procedimentos executáveis neste planejamento.

Cada característica de qualidade (Manutenibilidade, Confiabilidade e Segurança) será planejada de forma independente, mas seguindo um padrão consistente que garante:

-   **Rastreabilidade**: Cada procedimento está vinculado às métricas, questões e objetivos definidos na Fase 2;
-   **Reprodutibilidade**: Procedimentos detalhados permitem que outros avaliadores repliquem a avaliação;
-   **Consistência**: Uso padronizado de ferramentas e critérios de coleta;
-   **Validação**: Critérios claros para verificar a qualidade dos dados coletados.

---

## 1.3 Estrutura do Planejamento

Para tornar o plano de avaliação mais claro e navegável, a Fase 3 foi organizada em artefatos específicos para cada característica de qualidade priorizada. Em cada um desses documentos são descritos, de forma detalhada, os procedimentos de coleta, as ferramentas utilizadas, os outputs esperados e a forma de armazenamento dos dados. Assim, as métricas definidas na Fase 2 são operacionalizadas de maneira sistemática e rastreável, conforme sintetizado na tabela a seguir.

| Característica       | Objetivo                                                                 | Link                             |
| -------------------- | ------------------------------------------------------------------------ | -------------------------------- |
| **Manutenibilidade** | Operacionalizar a coleta de [métricas](../fase-2/manutenabilidade.md#25-metricas) de manutenibilidade do código     | [Ver seção](manutenabilidade.md) |
| **Confiabilidade**   | Operacionalizar a coleta de [métricas](../fase-2/confiabilidade.md#35-metricas) de confiabilidade do sistema       | [Ver seção](confiabilidade.md)  |
| **Segurança**        | Operacionalizar a coleta de [métricas](../fase-2/seguranca.md#45-metricas) de segurança e vulnerabilidades    | [Ver seção](seguranca.md)        |

---

## 1.4 Preparação do Ambiente

Antes de iniciar a coleta de métricas, é necessário preparar o ambiente de avaliação. Esta seção descreve os requisitos e configurações necessárias para garantir que todas as ferramentas estejam adequadamente configuradas e que o ambiente esteja pronto para a execução dos procedimentos de coleta.

### 1.4.1 Requisitos de Ambiente

-   **Acesso ao código-fonte**: Permissão de leitura ao [repositório do Guardiões da Saúde](https://github.com/ProEpiDesenvolvimento);
-   **Ferramentas de análise estática**: SonarQube (Community 9.x+) para coleta de métricas de manutenibilidade, confiabilidade e segurança.
-   **Ferramentas de monitoramento**: Para coleta de métricas de Confiabilidade relacionadas à disponibilidade do sistema e análise de erros;
-   **Ferramentas de documentação**: Editores de texto, planilhas e captura de tela para registrar dados e procedimentos.
-   **Ferramentas de gravação**: Software para captura de tela e gravação de vídeo para documentar a execução dos testes.

---

## 1.5 Procedimento Geral de Coleta e Documentação

O procedimento geral de coleta segue uma sequência padronizada para garantir consistência e reproduzibilidade. Além da coleta de dados, é fundamental documentar todo o processo de forma completa, incluindo evidências visuais e cálculos realizados.

### 1.5.1 Sequência de Execução

1.  **Preparação**: Configuração do ambiente e ferramentas;
2.  **Execução**: Coleta das métricas conforme procedimentos específicos de cada característica;
3.  **Validação**: Verificação da qualidade e completude dos dados coletados;
4.  **Armazenamento**: Organização e registro dos dados coletados em estrutura padronizada;
5.  **Documentação**: Registro completo de observações, cálculos e conclusões.

### 1.5.2 Documentação

Para garantir a **reproduzibilidade** e fornecer evidências da execução, cada procedimento de coleta deve ser documentado com os seguintes elementos:

#### 1.5.2.1 Gravações de Vídeo

-   **Gravação da execução dos testes**: Todas as coletas de métricas devem ser gravadas em vídeo, capturando a tela durante a execução dos procedimentos;
-   **Conteúdo das gravações**: Deve incluir a configuração inicial das ferramentas, a execução dos comandos, a visualização dos resultados no SonarQube e outras ferramentas, e a exportação dos dados;
-   **Duração**: As gravações devem capturar todo o processo, desde a preparação até a obtenção dos resultados finais.

#### 1.5.2.2 Cálculos e Processamento de Dados

-   **Registro de cálculos**: Todos os cálculos realizados para obter métricas derivadas devem ser documentados, incluindo fórmulas utilizadas e valores intermediários;
-   **Planilhas de cálculo**: Manter planilhas eletrônicas com as fórmulas e dados brutos utilizados, permitindo verificação e reprodução dos cálculos;

#### 1.5.2.3 Conclusão Final

-   **Síntese dos resultados**: Para cada característica, elaborar uma conclusão que sintetize os resultados obtidos;
-   **Interpretação**: Relacionar os resultados com os critérios de julgamento estabelecidos na Fase 2;
-   **Classificação**: Classificar cada métrica conforme os níveis de pontuação definidos (Excelente, Bom, Satisfatório, Insuficiente);

### 1.5.3 Armazenamento dos dados

Todos os dados, evidências e documentação coletados durante a execução dos procedimentos serão armazenados neste repositório, organizados por **característica de qualidade**, em pastas específicas (por exemplo, `docs/evidencias/manutenabilidade/`, `docs/evidencias/confiabilidade/`, `docs/evidencias/seguranca/`).  
Os resultados completos da coleta, incluindo vídeos, cálculos, status dos testes e conclusões, serão apresentados e analisados nas páginas de resultados da [Fase 4 - Execução da Avaliação](../fase-4/visao_geral.md) para cada característica, bem como na conclusão geral da Fase 4.

---

## 1.6 Referências Bibliográficas

> BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, Hans Dieter. _The Goal Question Metric (GQM) Approach._ In: MARCINIAK, J. J. (ed.). _Encyclopedia of Software Engineering._ New York: John Wiley & Sons, 1994.
> INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. _ISO/IEC 25023:2011 – Systems and Software Quality Requirements and Evaluation (SQuaRE): Measurement of System and Software Product Quality._ Geneva: ISO, 2011.
> SONARQUBE. _SonarQube Documentation._ Disponível em: <https://docs.sonarqube.org/>. Acesso em: 25 out. 2025.

---

## 1.8 Histórico de Versões

| Versão | Data       | Descrição                      | Autor(es) |
| ------ | ---------- | ------------------------------ | --------- |
| `1.0`  | 15/11/2025 | Criação do documento | [Arthur Carneiro](https://github.com/trindadea)   |
| `1.1`  | 16/11/2025 | Revisão e formatação            | [Matheus Henrick](https://github.com/MatheusHenrickSantos)   |

