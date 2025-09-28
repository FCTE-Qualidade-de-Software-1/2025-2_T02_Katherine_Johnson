# Planos de Qualidade

## Introdução

Este documento detalha os planos da equipe Katherine Johnson para a aplicação [Guardiões da Saúde](../visao-geral.md). O objetivo é definir as métricas de avaliação para verificar se o sistema atende aos requisitos de qualidade necessários para proporcionar uma experiência segura, confiável e eficiente aos usuários, além de fornecer dados valiosos para gestores de saúde pública.

## Objetivos de Qualidade

Ao analisar a aplicação Guardiões da Saúde, selecionamos três objetivos principais de qualidade que são cruciais para o sucesso e a eficácia do aplicativo:

### Objetivos Gerais

-   Garantir a **segurança** dos dados dos usuários, protegendo informações sensíveis contra acessos não autorizados.
-   Assegurar a **confiabilidade** do sistema, minimizando falhas e garantindo alta disponibilidade.
-   Facilitar a **manutenibilidade** do código, permitindo que futuras modificações sejam realizadas de forma eficiente e segura.

### Métricas de Qualidade Selecionadas

|     Métrica      | Meta  | Medição                                                     |
| :--------------: | :---: | ----------------------------------------------------------- |
|    Segurança     | Alta  | Análise de vulnerabilidades, auditorias de segurança        |
|  Confiabilidade  | Alta  | Taxa de falhas, tempo médio entre falhas (MTBF)             |
| Manutenibilidade | Média | Tempo médio para correção (MTTR), facilidade de modificação |

## Padrões de Qualidade Analisados

### ISO/IEC XXXXX - Qualidade do Produto

#### Segurança

-   **Confidencialidade**: Proteção de dados sensíveis contra acesso não autorizado
-   **Integridade**: Garantia de que os dados não sejam alterados de forma não autorizada
-   **Disponibilidade**: Garantia de que o sistema esteja acessível quando necessário

#### Confiabilidade

-   **Maturidade**: Redução de falhas devido a defeitos no software
-   **Tolerância a Falhas**: Capacidade de continuar operando em caso de falhas
-   **Recuperabilidade**: Capacidade de restaurar o sistema após uma falha

#### Manutenibilidade

-   **Modificabilidade**: Facilidade de realizar modificações no sistema
-   **Estabilidade**: Capacidade de o sistema permanecer inalterado após modificações
-   **Testabilidade**: Facilidade de testar o sistema para garantir sua qualidade
-   **Documentação**: Manutenção de documentação clara e atualizada

## Ferramentas Utilizadas

### Análise de Código

-   **RuboCop**: Análise estática para Ruby
-   **ESLint**: Análise estática para JavaScript
-   **SonarQube**: Análise de qualidade e segurança
-   **CodeClimate**: Métricas de manutenibilidade

### Testes

-   **RSpec**: Testes unitários e integração (Ruby)
-   **Jest**: Testes unitários (JavaScript)
-   **Cypress**: Testes E2E
-   **Artillery**: Testes de performance

### Monitoramento

-   **Sentry**: Monitoramento de erros
-   **New Relic**: Monitoramento de performance
-   **Prometheus**: Métricas de sistema
-   **Grafana**: Dashboards de monitoramento
