# 2. Manutenabilidade - Planejamento da Coleta

## 2.1 Introdução

Esta seção detalha o planejamento para coleta das métricas de **Manutenibilidade** definidas na [Fase 2](../fase-2/manutenabilidade.md). O objetivo é operacionalizar cada métrica em procedimentos executáveis, garantindo que a coleta seja consistente, rastreável e reproduzível.

As métricas a serem coletadas são:

-   **M1.1**: Complexidade Ciclomática
-   **M2.1**: Nível de Acoplamento entre Módulos
-   **M2.2**: Detecção de Ciclos de Dependência
-   **M3.1**: Cobertura de Testes Automatizados (%)
-   **M4.1**: Disponibilidade da Documentação
-   **M4.2**: Qualidade da Documentação

---

## 2.2 Ferramentas de Coleta

### Ferramentas Principais

| Ferramenta      | Uso                                    | Métricas Suportadas                    |
| --------------- | -------------------------------------- | -------------------------------------- |
| **SonarQube**   | Análise estática do código             | M1.1, M2.1, M2.2                       |
| **SimpleCov**   | Cobertura de testes (Ruby/Rails)       | M3.1                                   |
| **Jest**        | Cobertura de testes (JavaScript/React) | M3.1                                   |
| **Inspeção Manual** | Verificação de documentação        | M4.1, M4.2                             |

### Configuração do SonarQube

-   **Versão**: Community Edition 9.x ou superior;
-   **Regras habilitadas**: Complexidade Ciclomática, Acoplamento, Dependências;
-   **Linguagens**: Ruby, JavaScript, TypeScript;
-   **Configuração de qualidade**: Perfil padrão com ajustes específicos para o projeto.

### Ferramentas Auxiliares

-   **Git**: Para clonar e navegar no repositório;
-   **Editor de texto**: Para inspeção manual de código e documentação;
-   **Planilha eletrônica**: Para registro e organização dos dados coletados;
-   **Ferramenta de gravação**: Para capturar vídeo da execução dos procedimentos.

---

## 2.3 Operacionalização das Métricas

### M1.1 - Complexidade Ciclomática

**Questão relacionada**: Q1 - Qual o nível de complexidade estrutural do código-fonte do sistema?

**Objetivo da coleta**: Medir a complexidade estrutural do código através da contagem de caminhos linearmente independentes.

**Procedimento**:

1.  Executar análise estática do código-fonte utilizando o SonarQube;
2.  A ferramenta calcula automaticamente a complexidade ciclomática para cada método/função;
3.  Extrair do dashboard do SonarQube:
    -   Complexidade ciclomática média do projeto;
    -   Complexidade ciclomática máxima encontrada;
    -   Número de métodos com complexidade > 10, > 20 e > 30;
4.  Identificar métodos com complexidade crítica (> 20) para análise detalhada;
5.  Registrar os valores coletados e classificar conforme critérios da Fase 2:
    -   **< 10**: Baixa complexidade (Aceitável)
    -   **11-20**: Complexidade moderada (Atenção)
    -   **> 20**: Alta complexidade (Crítico)

---

### M2.1 - Nível de Acoplamento entre Módulos

**Questão relacionada**: Q2 - As responsabilidades dos módulos estão bem separadas?

**Objetivo da coleta**: Medir o grau de interdependência entre os módulos do software.

**Procedimento**:

1.  Executar análise estática do código-fonte utilizando o SonarQube;
2.  Acessar a seção de dependências no dashboard do SonarQube;
3.  Analisar os relatórios de dependência gerados:
    -   Identificar o número de classes/módulos dos quais cada módulo depende;
    -   Extrair métricas de acoplamento por módulo;
4.  Identificar módulos com alto acoplamento (> 5 dependências diretas);
5.  Registrar o nível geral de acoplamento do sistema e módulos problemáticos.

---

### M2.2 - Detecção de Ciclos de Dependência

**Questão relacionada**: Q2 - As responsabilidades dos módulos estão bem separadas?

**Objetivo da coleta**: Verificar a existência de dependências circulares entre módulos ou pacotes.

**Procedimento**:

1.  Executar análise estática do código-fonte utilizando o SonarQube;
2.  A ferramenta detecta automaticamente ciclos de dependência;
3.  Verificar no dashboard do SonarQube a presença de ciclos de dependência;
4.  Se detectados, documentar os ciclos encontrados (quais módulos estão envolvidos);
5.  Registrar resultado binário:
    -   **Não**: Aceitável
    -   **Sim**: Crítico

---

### M3.1 - Cobertura de Testes Automatizados (%)

**Questão relacionada**: Q3 - O código está suficientemente coberto por testes automatizados?

**Objetivo da coleta**: Medir a porcentagem do código-fonte executada por testes automatizados.

**Procedimento**:

1.  Preparar ambiente de testes do projeto (instalar dependências);
2.  Executar a suíte de testes automatizados:
    -   **Backend (Ruby/Rails)**: `bundle exec rspec --format documentation`
    -   **Frontend (React Native)**: `npm test -- --coverage`
3.  Coletar relatórios de cobertura gerados pelas ferramentas:
    -   SimpleCov para Ruby (geralmente em `coverage/index.html`);
    -   Jest Coverage para JavaScript/React (geralmente em `coverage/coverage-summary.json`);
4.  Extrair percentual de cobertura geral e por módulo;
5.  Identificar módulos com cobertura < 70%;
6.  Registrar o valor de cobertura geral e classificar conforme critérios:
    -   **> 70%**: Adequada
    -   **50-70%**: A melhorar
    -   **< 50%**: Insuficiente

---

### M4.1 - Disponibilidade da Documentação

**Questão relacionada**: Q4 - A documentação técnica existente é suficiente para apoiar futuras manutenções?

**Objetivo da coleta**: Verificar a existência de artefatos de documentação considerados essenciais.

**Procedimento**:

1.  Navegar pelo repositório do projeto no GitHub;
2.  Inspecionar manualmente a presença dos seguintes artefatos:
    -   README.md principal (na raiz do repositório);
    -   Documentação de arquitetura (se existir);
    -   Documentação de API (se existir);
    -   Guias de contribuição (CONTRIBUTING.md, se existir);
    -   Documentação técnica de módulos principais;
3.  Para cada artefato, registrar: **Sim** (presente) ou **Não** (ausente);
4.  Documentar localização dos arquivos encontrados.

---

### M4.2 - Qualidade da Documentação

**Questão relacionada**: Q4 - A documentação técnica existente é suficiente para apoiar futuras manutenções?

**Objetivo da coleta**: Avaliar a qualidade da documentação existente com base em critérios predefinidos.

**Procedimento**:

1.  Para cada documento identificado na métrica M4.1, aplicar checklist de qualidade;
2.  Avaliar cada documento em três dimensões (escala de 1 a 5):
    -   **Clareza**: A documentação é clara e compreensível? (1=Confusa, 5=Muito Clara)
    -   **Completude**: Informações essenciais estão presentes? (1=Incompleta, 5=Completa)
    -   **Atualização**: Documentação está atualizada com o código? (1=Desatualizada, 5=Atualizada)
3.  Calcular média das três notas para cada documento;
4.  Classificar conforme critérios:
    -   **4-5**: Boa
    -   **3**: Regular
    -   **1-2**: Ruim
5.  Registrar observações sobre principais pontos de melhoria identificados.

---

## 2.4 Armazenamento de Dados

## 2.5 Procedimentos Manuais

### Inspeção de Documentação (M4.1 e M4.2)

**Fluxo**:

1.  **Identificação de Documentos**:
    -   Navegar pelo repositório;
    -   Listar todos os arquivos `.md` e `README`;
    -   Classificar por tipo (arquitetura, API, guia, etc.).

2.  **Aplicação do Checklist**:
    -   Para cada documento:
        -   Ler completamente;
        -   Verificar clareza (1-5);
        -   Verificar completude (1-5);
        -   Verificar atualização (comparar com código) (1-5);
        -   Registrar observações.

3.  **Consolidação**:
    -   Calcular média das notas;
    -   Classificar conforme critérios;
    -   Documentar principais pontos de melhoria.

---

## 2.6 Rastreabilidade com Fase 2

| Métrica | Questão (Fase 2) | Objetivo (Fase 2)                          | Link para Fase 2                                    |
| ------- | ---------------- | ------------------------------------------ | --------------------------------------------------- |
| M1.1    | Q1               | Entender a complexidade estrutural         | [Ver métrica](../fase-2/manutenabilidade.md#m11)   |
| M2.1    | Q2               | Verificar separação de responsabilidades   | [Ver métrica](../fase-2/manutenabilidade.md#m21)   |
| M2.2    | Q2               | Verificar separação de responsabilidades   | [Ver métrica](../fase-2/manutenabilidade.md#m22)   |
| M3.1    | Q3               | Verificar cobertura de testes              | [Ver métrica](../fase-2/manutenabilidade.md#m31)   |
| M4.1    | Q4               | Verificar disponibilidade de documentação | [Ver métrica](../fase-2/manutenabilidade.md#m41)   |
| M4.2    | Q4               | Verificar qualidade de documentação        | [Ver métrica](../fase-2/manutenabilidade.md#m42)   |

---

## 2.7 Referências Bibliográficas

> SONARQUBE. _SonarQube Documentation._ Disponível em: <https://docs.sonarqube.org/>. Acesso em: 25 out. 2025.
> SIMPLECOV. _SimpleCov Documentation._ Disponível em: <https://github.com/simplecov-ruby/simplecov>. Acesso em: 25 out. 2025.
> JEST. _Jest Documentation._ Disponível em: <https://jestjs.io/>. Acesso em: 25 out. 2025.

---

## 2.8 Histórico de Versões

| Versão | Data       | Descrição            | Autor(es)                                          |
| ------ | ---------- | -------------------- | -------------------------------------------------- |
| `1.0`  | 16/11/2025 | Criação do documento | [Arthur Carneiro](https://github.com/trindadea)   |
