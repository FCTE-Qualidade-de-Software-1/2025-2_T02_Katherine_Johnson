# 1. Requisitos de Avaliação da Qualidade (GQM)

## 1.1 Objetivo

Esta etapa da análise de qualidade tem como objetivo definir formalmente o **escopo da avaliação** e especificar as **medidas de qualidade** que serão aplicadas ao produto Guardiões da Saúde. 

Para atingirmos esse objetivo, será necessário selecionar métricas apropriadas, estabelecer critérios de julgamento claros e interpretar os resultados de forma que a avaliação possa ser repetida e reproduzível por outros avaliadores em condições semelhantes.

A abordagem adotada será a técnica **GQM (Goal–Question–Metric)**, que permite conectar objetivos estratégicos a perguntas de medição e métricas mensuráveis, assegurando clareza e consistência na avaliação.

---

## 1.2 Metodologia GQM

A metodologia **Goal–Question–Metric (GQM)**, proposta por **Basili, Caldiera e Rombach (1994)**, é uma abordagem estruturada utilizada para planejar, conduzir e interpretar medições de qualidade de software. Ela parte da ideia de que toda medição deve ter um propósito claro, relacionado a um objetivo específico de avaliação.

O modelo GQM organiza o processo de medição em **três níveis hierárquicos**, que conectam os objetivos estratégicos às métricas observáveis, conforme descrito a seguir:

| Nível                  | Descrição                                                                                                                                                                                                  |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Goal (Objetivo)**        | Define o **propósito da medição**, o objeto de estudo (como um produto ou processo), o foco de qualidade e o ponto de vista do avaliador. |
| **Question (Questão)** | Traduz o objetivo em **perguntas específicas**, que permitem compreender se ele está sendo atingido e identificar causas ou fatores que afetam o resultado.                                             |
| **Metric (Métrica)**   | Determina os **valores quantitativos ou qualitativos** que respondem às perguntas formuladas, permitindo medir, comparar e interpretar resultados de maneira objetiva.                                     |

Dessa forma, o GQM adota uma abordagem **top-down**, iniciando com as metas de avaliação e derivando perguntas e métricas a partir delas. Essa estrutura garante **rastreabilidade** e **reprodutibilidade** dos resultados.

Nesta fase do trabalho, o GQM é aplicado para **definir os requisitos de avaliação da qualidade** do sistema **Guardiões da Saúde**, delimitando o escopo de análise nas três características definidas na Fase 1: **manutenibilidade**, **confiabilidade** e **segurança**.

O ponto de partida dessa aplicação é a formulação da [meta global de medição](#121-meta-global), que sintetiza o propósito geral da avaliação.

A seguir, apresenta-se a formulação estruturada da meta global, conforme o modelo GQM:

### 1.2.1 Meta Global

<table>
  <tr><th>Analisar</th><td>o Sistema Guardiões da Saúde</td></tr>
  <tr><th>Com o propósito de</th><td>entender e avaliar a qualidade do software</td></tr>
  <tr><th>Com respeito a</th><td>manutenibilidade, confiabilidade e segurança</td></tr>
  <tr><th>Do ponto de vista da</th><td>equipe de desenvolvimento e qualidade</td></tr>
  <tr><th>No contexto da</th><td>disciplina de Qualidade de Software</td></tr>
</table>

---

## 1.3 Estrutura de Avaliação

A estrutura de avaliação desta fase foi organizada de forma a refletir diretamente a aplicação da metodologia **GQM** sobre as **três características de qualidade** priorizadas na Fase 1.

Cada característica possui um artefato próprio com objetivo, questões, métricas e critérios de julgamento. Essa divisão facilita a leitura, permitindo que cada característica seja analisada de forma independente, mas sob o mesmo referencial metodológico.

| Característica       | Objetivo                                                        | Link                             |
| -------------------- | --------------------------------------------------------------- | -------------------------------- |
| **Manutenibilidade** | Entender (Facilidade de manutenção e evolução do código)         | [Ver seção](manutenabilidade.md) |
| **Confiabilidade**   | Entender (Estabilidade e robustez do sistema)                    | [Ver seção](confiabilidade.md)   |
| **Segurança**        | Enterder e Avaliar (A proteção a vulnerabilidades e controle de acesso) | [Ver seção](seguranca.md)        |

---

## 1.4 Uso de IA no Desenvolvimento do Trabalho

Durante a elaboração desta fase do projeto, foram utilizados recursos de **inteligência artificial generativa**, em especial o modelo *ChatGPT*, como **apoio à estruturação textual, correções ortográficas e padronização da redação e da documentação**.

As contribuições da IA incluíram:

* auxílio na **formatação** e **revisão gramatical** do texto;
* **padronização** da estrutura do documento;
* e **sugestões** de transições entre seções;

Nenhum conteúdo foi gerado sem **validação e revisão humana** e todo o material técnico foi desenvolvido e revisado pela equipe.

---

## 1.6 Referências Bibliográficas

> BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, Hans Dieter. *The Goal Question Metric (GQM) Approach.* In: MARCINIAK, J. J. (ed.). *Encyclopedia of Software Engineering.* New York: John Wiley & Sons, 1994.
> VAN SOLINGEN, R.; BERGHOUT, E. *The Goal/Question/Metric Method: A Practical Guide for Quality Improvement of Software Development.* London: McGraw-Hill, 1999.
> INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. *ISO/IEC 25023:2011 – Systems and Software Quality Requirements and Evaluation (SQuaRE): Measurement of System and Software Product Quality.* Geneva: ISO, 2011.

---

## 1.7 Histórico de Versões

| Versão | Data | Descrição | Autor(es) |
|--------|------|------------|------------|
| `1.0` | 14/10/2025 | Criação do documento | [Uires Carlos de Oliveira](https://github.com/uires2023), [Matheus Henrick](https://github.com/MatheusHenrickSantos) |
| `1.1` | 15/10/2025 | Formatação do texto, remoção de informações redundantes | [Gabriela Tiago](https://github.com/GabrielaTiago) |
| `1.2` | 24/10/2025 | Adição do objetivo, metodologia, estrutura e declaração do uso de IA  | [Arthur Carneiro](https://github.com/trindadea) |
| `1.3` | 25/10/2025 | Ajuste do item 1.3 os objetivos | [Uires Carlos de Oliveira](https://github.com/uires2023) |