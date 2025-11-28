# 5. Conclusão Geral e Recomendações

## 5.1 Síntese por Característica

### 5.1.1 Manutenibilidade
Com base nas métricas coletadas e nas respostas GQM, o nível geral de **Manutenibilidade** do Guardiões da Saúde foi avaliado como **crítico**.  

Os principais fatores que levaram a essa classificação foram:

- complexidade ciclomática total de 1.419, concentrada quase integralmente em `src/`, indicando módulos extensos e difíceis de compreender;  
- cobertura de testes automatizados igual a 0%, mesmo com a suíte de Jest configurada, o que aumenta significativamente o risco de regressões;  
- documentação técnica praticamente inexistente (apenas README, CONTRIBUTING e templates de issues/PR), dificultando onboarding e manutenção. 

> Conclusão: o sistema apresenta **alta dificuldade de manutenção**, exigindo esforço estruturado de refatoração, testes e documentação.

### 5.1.2 Confiabilidade 
Com base nas métricas coletadas e nas respostas GQM, o nível geral de **Confiabilidade** do Guardiões da Saúde foi avaliado como **baixo**.  

Os principais fatores que levaram a essa classificação foram:

- SonarQube ter reportado 206 bugs e `Reliability Rating = D`, evidenciando baixa maturidade do código;  
- forte presença de code smells e 39,1% de duplicação de código, o que aumenta a probabilidade de falhas e o custo de correção;  
- ausência de testes e de métricas de disponibilidade/tolerância a falhas em produção, impedindo validar o comportamento em cenários reais. 

> Conclusão: a probabilidade de falhas em execução é **elevada**, e a confiabilidade atual não é adequada para um sistema crítico de saúde.

### 5.1.3 Segurança
Com base nas métricas coletadas e nas respostas GQM, o nível geral de **Segurança** do Guardiões da Saúde foi avaliado como **regular**.  

Os principais fatores que levaram a essa classificação foram:

- a análise SAST no SonarCloud não ter identificado vulnerabilidades críticas ou altas, nem problemas nas categorias OWASP avaliadas, indicando boa robustez técnica do código;  
- todos os Security Hotspots terem sido revisados na coleta, reduzindo o risco de pontos cegos em trechos sensíveis;  
- por outro lado, o sistema não implementar mecanismos de log/auditoria, comprometendo rastreabilidade, imputabilidade e investigação de incidentes.  

> Conclusão: a proteção técnica contra ataques é **boa**, mas a ausência de monitoramento e trilhas de auditoria mantém a segurança em um nível **apenas regular** para o contexto de saúde.

## 5.2 Coerência com o Propósito

O propósito definido na Fase 1 foi avaliar sistematicamente a qualidade do Guardiões da Saúde para apoiar decisões de evolução do produto e fortalecer a confiança dos stakeholders (ProEpi, gestores de saúde, usuários e comunidade acadêmica).  

Os resultados da Fase 4 atendem a esse propósito ao:

- explicitar riscos concretos de manutenção e confiabilidade que impactam diretamente a operação contínua do aplicativo;  
- evidenciar pontos fortes em segurança técnica, importantes para a confiança de usuários e gestores;  
- fornecer evidências auditáveis (prints, vídeos, métricas) que podem ser revisitadas por equipes de desenvolvimento e avaliação em ciclos futuros.

## 5.3 Julgamento Final e Recomendações Prioritárias

**Julgamento geral:** à luz das métricas e da análise realizada, a qualidade do Guardiões da Saúde é considerada **parcialmente adequada** ao propósito e às necessidades dos stakeholders. A segurança técnica é boa, mas manutenibilidade e confiabilidade apresentam fragilidades relevantes.

**Recomendações prioritárias:**

1. **Reduzir a complexidade estrutural** dos módulos mais críticos, por meio de refatorações incrementais em componentes/telas com maior concentração de lógica.  
2. **Implantar uma suíte mínima de testes automatizados**, priorizando fluxos centrais do app (registro, reporte diário, sincronização de dados), com meta inicial de cobertura entre 30–40%.  
3. **Introduzir logging e auditoria de segurança**, registrando eventos relevantes (login, alterações de dados sensíveis, falhas) com identificador de usuário, timestamp e contexto.  
4. **Criar documentação técnica essencial**, incluindo visão de arquitetura, descrição dos principais módulos e passos de build/deploy, para reduzir dependência do conhecimento tácito.  
5. **Planejar um ciclo de correção de bugs e redução de duplicações**, priorizando as issues mais críticas apontadas pelo SonarQube e estabelecendo critérios de “pronto” que incluam qualidade de código.

## 5.7 Histórico de Versões
| Versão | Data | Descrição | Autor(es) |
| --- | --- | --- | --- |
| `1.0`  | 27/11/2025 | Criação do documento | [Arthur Carneiro](https://github.com/trindadea) |
| `1.1`  | 27/11/2025 | Preenchimento da conclusão | [Arthur Carneiro](https://github.com/trindadea) |
