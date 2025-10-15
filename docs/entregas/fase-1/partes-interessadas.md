# 2. Requisitante e Partes Interessadas

## 2.1. Requisitante da Avaliação

A presente avaliação de qualidade de produto de software é requisitada no âmbito acadêmico, pela disciplina **Qualidade de Software**, ministrada na Universidade de Brasília. O requisitante formal é o corpo docente responsável pela disciplina.

O papel do requisitante é avaliar a capacidade da equipe de aplicar os conceitos, métodos e técnicas de avaliação de qualidade de software em um produto real. A expectativa é que os resultados desta análise não apenas demonstrem o domínio técnico da equipe, mas também gerem um relatório coeso e bem fundamentado que possa, ser útil aos desenvolvedores e gestores do projeto "Guardiões da Saúde".

## 2.2. Mapeamento das Partes Interessadas (Stakeholders)

O ecossistema do "Guardiões da Saúde" é composto por uma rede diversificada de organizações e grupos de usuários, cada um com papéis e interesses distintos na qualidade do software. A tabela a seguir detalha os principais stakeholders identificados.

<div align="center">
    <p><strong>Tabela 1 - Partes Interessadas</strong></p>
</div>

| Parte Interessada (Stakeholder)                                               | Categoria                      | Papel e Relação com o Software                                                                                                                                            | Principais Necessidades e Expectativas de Qualidade                                                                                                                                                                                                             |
| :---------------------------------------------------------------------------- | :----------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ProEpi (Associação Brasileira de Profissionais de Epidemiologia de Campo)** | Desenvolvedor / Mantenedor     | Idealizadora e principal desenvolvedora do aplicativo, responsável por suas atualizações e pela coordenação de novos projetos, como o de "Líderes Comunitários".[1, 2, 3] | **Manutenibilidade** para adaptar o app a novas emergências e projetos. **Segurança** para proteger os dados dos usuários e garantir a conformidade com a LGPD. **Confiabilidade** para assegurar que a plataforma funcione sem falhas críticas.                |
| **Ministério da Saúde e Secretarias de Saúde (Estaduais e Municipais)**       | Gestor / Cliente               | Patrocinador inicial e principal consumidor dos dados gerados para a formulação de políticas de saúde pública e resposta a surtos.[2, 4, 5]                               | **Confiabilidade e Precisão dos Dados** para tomar decisões baseadas em evidências. **Oportunidade (Timeliness)** dos alertas para permitir uma resposta rápida a emergências. **Segurança** para garantir a proteção de dados de saúde sensíveis da população. |
| **Universidade de Brasília (UnB) - Sala de Situação (SDS) e Pesquisadores**   | Parceiro Técnico / Analista    | Responsáveis pela análise dos dados brutos, transformação em inteligência epidemiológica (boletins, mapas) e condução de pesquisas.[6, 7]                                 | **Qualidade dos Dados** (integridade, completude). **Eficiência de Desempenho** para processar grandes volumes de informação. **Compatibilidade** para integrar os dados com outras ferramentas de análise.                                                     |
| **Cidadão (Usuário Final da Vigilância Participativa)**                       | Usuário                        | Fonte primária de dados, reportando voluntariamente seu estado de saúde para o monitoramento coletivo.[6, 2]                                                              | **Privacidade e Segurança** dos seus dados pessoais e de saúde. **Simplicidade e Facilidade de Uso** para o reporte diário. **Valor Agregado**, como receber informações confiáveis e orientações de saúde.                                                     |
| **Líderes Comunitários**                                                      | Usuário Especializado          | Atuam como "sensores" qualificados na comunidade, reportando eventos de saúde (humanos, animais e ambientais) através de um módulo específico do app.[8]                  | **Funcionalidade e Confiabilidade** da ferramenta de reporte. **Canais de Comunicação Claros** para receber feedback e orientações das equipes de saúde.                                                                                                        |
| **Gestores de Instituições (Universidades, Escolas, etc.)**                   | Operador / Cliente             | Utilizam a funcionalidade de "Vigilância Ativa Institucional" para monitorar a saúde de suas comunidades (alunos, funcionários) e acionar protocolos de cuidado.[9, 2, 5] | **Confiabilidade do Sistema de Alertas** para uma notificação rápida e precisa. **Facilidade de Implementação** e gerenciamento da plataforma em sua instituição. **Acesso a Dashboards** com dados claros e acionáveis.                                        |
| **Parceiros Internacionais (UK-PHRST, etc.)**                                 | Financiador / Parceiro Técnico | Colaboram em projetos específicos (ex: VBE com Líderes Comunitários), fornecendo financiamento, expertise técnica e validando o modelo em outros contextos.[1]            | **Viabilidade e Sustentabilidade** do modelo proposto. **Eficácia** da ferramenta na detecção de surtos em comparação com métodos tradicionais.                                                                                                                 |
| **Comunidade Acadêmica e Científica**                                         | Pesquisador / Avaliador        | Envolvem-se na validação e avaliação do impacto do aplicativo em estudos de caso e pesquisas acadêmicas.[1]                                                               | **Rigor Científico** na coleta e análise de dados. **Transparência** nos métodos e resultados. **Relevância** das informações para a formulação de políticas públicas.                                                                                          |

## 2.3. Influência das Partes Interessadas na Avaliação

O mapeamento das partes interessadas influencia diretamente a seleção e priorização das características de qualidade que serão avaliadas. As necessidades de múltiplos stakeholders convergem para alguns pontos críticos:

-   A forte dependência de **gestores de saúde** e **pesquisadores** na precisão dos dados para tomadas de decisão críticas eleva a importância da **Confiabilidade** do software.
-   A natureza sensível dos dados coletados, conforme a preocupação de **cidadãos**, **ProEpi** e **Ministério da Saúde**, torna a avaliação da **Segurança** um requisito indispensável, especialmente no que tange à conformidade com a LGPD.
-   A necessidade da **ProEpi** de adaptar o aplicativo para novas crises e projetos, como a expansão para a Vigilância Baseada em Eventos, destaca a relevância de avaliar a **Manutenibilidade** e a **Flexibilidade** da arquitetura do software.

<!-- Portanto, a definição do escopo e da profundidade da nossa avaliação será guiada por essas necessidades, buscando analisar as características que geram maior valor e mitigam os maiores riscos para as principais partes interessadas. -->

---

## Referências Bibliográficas

-   [1] PROEPI. Guardiões da Saúde. ProEpi - Associação Brasileira de Profissionais de Epidemiologia de Campo, 2025. Disponível em: <https://proepi.org.br/guardioes-da-saude>. Acesso em: 29 set. 2025.
-   [2] UFSCar. Estratégia Guardiões da Saúde. Universidade Federal de São Carlos, 2021. Disponível em: <https://www.vencendoacovid19.ufscar.br/arquivos/gtve-estrategia-guardioes-da-saude/estrategia-guardioes-da-saude-ufscar.pdf>. Acesso em: 29 set. 2025.
-   [3] UNB. Nova atualização do Guardiões da Saúde será testada por colaboradores da SDS/UNB. Universidade de Brasília, 2021. Disponível em: <https://sds.unb.br/nova-atualizacao-do-guardioes-da-saude-sera-testada-por-colaboradores-da-sds-unb/>. Acesso em: 29 set. 2025.
-   [4] Folha. Governo quer usar app para monitorar surtos de doenças como dengue e zika. Folha de S.Paulo, 2017. Disponível em: <https://m.folha.uol.com.br/seminariosfolha/2017/03/1870826-governo-quer-usar-app-para-monitorar-surtos-de-doencas-como-dengue-e-zika.shtml>. Acesso em: 29 set. 2025.
-   [5] CONASEMS. Vigilância em Saúde de Belém (PA) se une à Educação no desafio de enfrentar o coronavírus. Conselho Nacional de Secretários de Saúde, 2022. Disponível em: <https://portal.conasems.org.br/brasil-aqui-tem-sus/reportagens-especiais/33_vigilancia-em-saude-de-belem-pa-se-une-a-educacao-no-desafio-de-enfrentar-o-coronavirus>. Acesso em: 29 set. 2025.
-   [6] UNB. Retorno Seguro. Universidade de Brasília, 2022. Disponível em: <https://sds.unb.br/retornoseguro/>. Acesso em: 29 set. 2025.
-   [7] UNB. Vigilância Epidemiológica e Análise de Informações no Guardiões da Saúde. Universidade de Brasília, 2021. Disponível em: <https://noticias.unb.br/artigos-main/5097-vigilancia-epidemiologica-e-analise-de-informacoes-no-guardioes-da-saude>. Acesso em: 29 set. 2025.
-   [8] ProEpi. Você sabe o que é o Vigilância Baseada em Eventos (VBE) de Base Comunitária? ProEpi, 2024. Disponível em: <https://proepi.org.br/2024/04/15/voce-sabe-o-que-e-o-vigilancia-baseada-em-eventos-vbe-de-base-comunitaria/11251/>. Acesso em: 29 set. 2025.
-   [9] UNB. Nova funcionalidade do app Guardiões da Saúde facilita o monitoramento de casos de COVID-19 na UNB. Universidade de Brasília, 2024. Disponível em: <https://noticias.unb.br/76-institucional/4899-nova-funcionalidade-do-app-guardioes-da-saude-facilita-o-monitoramento-de-casos-de-covid-19-na-unb>. Acesso em: 29 set. 2025.

---

## Histórico de Versões

| Versão | Descrição                     | Autor(es)                                          | Data de Produção |
| :----: | ----------------------------- | -------------------------------------------------- | :--------------: |
| `1.0`  | Criação do documento          | [Gabriela Tiago](https://github.com/GabrielaTiago) |    01/10/2025    |
| `1.1`  | Atualização do nome da tabela | [Gabriela Tiago](https://github.com/GabrielaTiago) |    01/10/2025    |
