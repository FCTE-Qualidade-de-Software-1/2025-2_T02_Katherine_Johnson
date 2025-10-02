# Visão Geral do Projeto

## O Aplicativo Guardiões da Saúde

O **Guardiões da Saúde** é um aplicativo gratuito para dispositivos móveis (Android e iOS) e navegadores de internet, projetado para fortalecer a vigilância em saúde no Brasil. Idealizado pela Associação Brasileira de Profissionais de Epidemiologia de Campo (ProEpi) e com desenvolvimento inicial apoiado pelo Ministério da Saúde em 2007, a plataforma permite que a população contribua voluntariamente para o monitoramento da saúde coletiva, atuando como uma ferramenta inovadora de vigilância participativa.

## Contexto e Importância

A vigilância participativa é uma estratégia que transforma o cidadão em um agente ativo na saúde pública. Neste modelo:

-   **Cidadãos** contribuem voluntariamente com informações sobre seu estado de saúde, reportando sintomas diariamente.
-   **Dados** são coletados em tempo real, permitindo que os serviços de saúde se antecipem a surtos e elaborem planos de contingência.
-   **Ações** de colaboração e engajamento são estimuladas, fortalecendo a relação entre a comunidade e o sistema de saúde.
-   **Informações** sobre casos leves, que normalmente não chegariam ao sistema de saúde, são capturadas, fornecendo um panorama mais preciso da disseminação de doenças.

## Funcionalidades Principais

A funcionalidade central do aplicativo é o **reporte diário do estado de saúde**, no qual o usuário informa se está se sentindo _"bem"_ ou _"mal"_.

Caso reporte mal-estar, pode selecionar sintomas específicos em uma lista detalhada. Em troca, a plataforma oferece **orientações de saúde**, a **localização de farmácias** e **Unidades de Pronto Atendimento (UPAs)** próximas via GPS e atua como um canal de informações confiáveis, como notícias e boletins.

Outra função chave é a **Vigilância Ativa Institucional**, que permite ao usuário, mediante consentimento, vincular seu perfil a uma instituição (como uma universidade) para notificar automaticamente a equipe de saúde local em caso de sintomas, agilizando o cuidado e o monitoramento.

## Tecnologias e Plataforma

### Plataforma

-   **Aplicativo Móvel**: Disponível gratuitamente para as plataformas Android e iOS.
-   **Acesso Web**: Funcionalidades também acessíveis via navegadores de internet.
-   **Parcerias de Desenvolvimento**: O projeto evoluiu através de parcerias entre a ProEpi, o Ministério da Saúde, a Sala de Situação em Saúde da Universidade de Brasília (UnB) e outras instituições acadêmicas.

### Segurança e Privacidade

-   **Criptografia**: Os dados dos usuários são criptografados durante o trânsito para garantir a segurança.
-   **Conformidade Legal**: A plataforma opera em conformidade com a Lei Geral de Proteção de Dados (LGPD) do Brasil.
-   **Controle do Usuário**: O compartilhamento de dados sensíveis exige consentimento explícito, e os usuários podem solicitar a exclusão de suas informações a qualquer momento.

### Arquitetura do Sistema

O sistema é composto por diferentes módulos que trabalham em conjunto para viabilizar a vigilância participativa e ativa.

-   **Aplicativo _Mobile_/_Web_**: Interface principal para o usuário reportar seu estado de saúde, acessar informações e localizar serviços próximos, como UPAs e farmácias.
-   **Banco de Dados Centralizado**: Armazena os registros de saúde enviados pelos usuários para análise posterior.
-   **Módulo de Análise (Sala de Situação da UnB)**: Equipes de especialistas processam os dados brutos, gerando inteligência epidemiológica, mapas de calor e análises de padrões.
-   **Dashboard e Sistema de Boletins**: Painéis públicos e boletins epidemiológicos são gerados para gestores de saúde e para a sociedade, garantindo transparência e subsidiando a tomada de decisão.
-   **Sistema de Alertas (Vigilância Ativa Institucional)**: Funcionalidade que notifica equipes de saúde designadas quando um usuário vinculado a uma instituição (como uma universidade) reporta sintomas, disparando ações de orientação e cuidado.

## Benefícios para a Saúde Pública

### Para Usuários

-   Contribuição direta para a saúde coletiva e o fortalecimento do SUS.
-   Acesso a informações de saúde confiáveis, combatendo a desinformação.
-   Recebimento de orientações sobre como proceder em caso de sintomas.
-   Ferramentas úteis, como a localização de farmácias e unidades de saúde próximas.

### Para Gestores de Saúde

-   Acesso a dados em tempo real sobre a situação de saúde na comunidade.
-   Mapeamento geográfico de síndromes e detecção precoce de surtos.
-   Complemento ao sistema de vigilância tradicional, capturando dados de casos leves que não seriam notificados.
-   Tomada de decisão mais ágil e baseada em evidências para alocação de recursos e planejamento de ações.

## Impacto Social

O projeto contribui para:

-   Democratização da vigilância em saúde, com a participação ativa dos cidadãos.
-   Fortalecimento do Sistema Único de Saúde (SUS) com dados complementares e oportunos.
-   Melhoria na capacidade de resposta a emergências sanitárias, como demonstrado na pandemia de COVID-19.
-   Promoção de uma cultura de cuidado coletivo na saúde pública.

---

## Histórico de Versões

| Versão | Descrição                      | Autor(es)                                                  | Data de Produção |
| :----: | ------------------------------ | ---------------------------------------------------------- | :--------------: |
| `1.0`  | Criação do documento           | [Gabriela Tiago](https://github.com/GabrielaTiago)         |    28/09/2025    |
| `1.1`  | Adição do Histórico de Versões | [Matheus Henrick](https://github.com/MatheusHenrickSantos) |    30/09/2025    |
| `1.2`  | Linter e formatação            | [Gabriela Tiago](https://github.com/GabrielaTiago)         |    01/10/2025    |
