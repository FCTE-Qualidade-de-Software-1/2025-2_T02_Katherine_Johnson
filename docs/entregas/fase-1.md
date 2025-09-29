# Fase 1 - Requisitos de avaliação

## 1. PROPÓSITO DA AVALIAÇÃO  

### 1.1 Contexto e Motivação  
O enfrentamento de surtos e crises de saúde depende muito da capacidade de **coletar, analisar e entender dados de forma rápida e segura**. Nesse cenário, a vigilância participativa é essencial, pois transforma o cidadão em **agente ativo da saúde pública**.  

O **Guardiões da Saúde**, desenvolvido pela ProEpi e apoiado inicialmente pelo Ministério da Saúde em 2007, é um software de código aberto criado justamente para isso: mobilizar cidadãos e profissionais de saúde na notificação de sintomas, dando aos gestores acesso ágil a informações importantes para a tomada de decisão. A plataforma está disponível gratuitamente para **Android, iOS e navegadores web**, ampliando seu alcance.  

Uma de suas grandes forças é permitir que informações sobre **casos leves**, que normalmente não chegam ao sistema de saúde, sejam registradas. Assim, é possível ter um **panorama mais completo da disseminação de doenças**, complementando a vigilância tradicional. Durante a pandemia de COVID-19, o sistema demonstrou sua importância ao apoiar a **resposta rápida a emergências sanitárias** e fortalecer a cultura de cuidado coletivo.  

Mas a eficiência do Guardiões da Saúde não depende só da parte técnica, e sim também da **participação sincera e constante dos usuários**. Se as pessoas não registrarem seus sintomas com frequência, ou deixarem de usar o app por falta de motivação, os dados podem ficar incompletos e acabar prejudicando a credibilidade do sistema. Por isso, além da parte tecnológica, a ferramenta também precisa **incentivar campanhas de saúde e educação sanitária** que engajem a população.  

Assim, a força do Guardiões da Saúde está em três pilares técnicos — **Segurança, Confiabilidade e Manutenibilidade** — junto de uma boa estratégia de **mobilização social** para garantir o uso correto e contínuo.  


### 1.2 Declaração do Propósito  
> Este trabalho apresenta um plano de avaliação da qualidade do **Guardiões da Saúde**, com foco em **Segurança, Confiabilidade e Manutenibilidade**, conforme a ISO/IEC 25010. O objetivo é analisar de forma prática e sistemática se o software protege bem os dados, se funciona de maneira estável em situações críticas e se sua base de código é fácil de manter e evoluir. Também será considerado o papel do app em **estimular que os usuários participem de forma sincera e constante**, ajudando campanhas de saúde pública e garantindo que os dados coletados sejam realmente úteis. A avaliação vai incluir tanto o aplicativo móvel (Android/iOS) quanto o acesso via web e os serviços de backend disponíveis no repositório oficial.

### 1.3 Objetivos Específicos  
Para alcançar esse propósito, os objetivos específicos da avaliação são:  

### Segurança  
- Rodar **análises de vulnerabilidades** no código e nas dependências, checando riscos de invasão ou vazamento.  
- Avaliar os mecanismos de **autenticação e controle de acesso**, garantindo boas práticas para proteção de dados de saúde.  
- Verificar se existem **auditorias e registros de segurança** que permitam rastrear ações críticas.  

### Confiabilidade  
- Medir a **taxa de falhas** em cenários de alta demanda, como picos de notificações em surtos.  
- Calcular o **MTBF (Mean Time Between Failures)** para entender a robustez do sistema.  
- Avaliar a **disponibilidade e consistência dos dados** coletados.  
- Checar como a **participação sincera e constante dos usuários** impacta na qualidade dos dados.  
- Incluir a análise da **Vigilância Ativa Institucional**, verificando como a integração com universidades e órgãos de saúde influencia na estabilidade e confiabilidade do sistema.  

### Manutenibilidade  
- Medir o **MTTR (Mean Time To Repair)**, ou seja, quanto tempo leva em média para corrigir falhas.  
- Verificar a **facilidade de modificar o sistema**, analisando modularidade, legibilidade e boas práticas no código.  
- Avaliar a **documentação técnica e o pipeline de desenvolvimento**, garantindo suporte à evolução sustentável.  


### 1.4 Alinhamento com Objetivos de Negócio e ODS  
A avaliação proposta está ligada diretamente aos objetivos do Guardiões da Saúde e aos **Objetivos de Desenvolvimento Sustentável (ODS)**:  

- **ODS 3 – Saúde e Bem-Estar**:  
  - Fortalecer a vigilância epidemiológica (Meta 3.d).  
  - **Estimular a participação da população** de forma consciente, apoiando campanhas sanitárias (Meta 3.3).  
  - Contribuir para o **combate à desinformação**, fornecendo dados confiáveis e orientações de saúde seguras.  

- **ODS 9 – Inovação e Infraestrutura**:  
  - Melhorar continuamente a manutenibilidade para sustentar a evolução tecnológica do sistema (Meta 9.c).  
  - Apoiar a **democratização do acesso à saúde digital**, ampliando o impacto social da solução.  

#### Benefícios esperados para o negócio:  
- **Credibilidade e confiança**: mostrar para os usuários que seus dados estão seguros e são tratados de forma responsável.  
- **Engajamento social**: motivar o uso contínuo e sincero do app, com apoio de campanhas de conscientização e integração com políticas públicas.  
- **Agilidade em crises de saúde**: reduzir falhas e garantir que o sistema funcione bem em momentos críticos.  
- **Sustentabilidade técnica**: manter o software fácil de corrigir e evoluir, evitando acúmulo de problemas a longo prazo.  

## 2. IDENTIFICAÇÃO DOS TIPOS DE PRODUTOS A SEREM AVALIADOS

### 2.1 Produto Principal
O **Guardiões da Saúde** é um aplicativo gratuito de vigilância participativa em saúde pública.  
Sua **natureza** é de um sistema digital multiplataforma (aplicativo móvel e web), cujo propósito é **permitir que cidadãos reportem diariamente seu estado de saúde** e recebam orientações, além de apoiar gestores de saúde com dados em tempo real.  

As **funções centrais** incluem:  
- Registro diário de sintomas e estado de saúde.  
- Fornecimento de orientações de saúde e localização de serviços (UPAs, farmácias).  
- Vinculação a instituições (Vigilância Ativa Institucional) para disparo de alertas a equipes de saúde.  
- Disponibilização de informações confiáveis em saúde.  

---

### 2.2 Produto Principal Especificado
- **Nome:** Guardiões da Saúde  
- **Categoria:** Produto **COTS/MOTS** (software de uso público, open-source, com possibilidade de adaptações institucionais)  
- **Plataformas:** Android, iOS e Web  
- **Versão / recorte avaliado:**  
  - iOS: versão 3.4.6 (requer iOS 12.0 ou posterior)  
  - Android: [indicar depois]  
  - Web: [URL/versão observada em DD/MM/AAAA]  
  - Backend/API: repositório público `guardioes-api`  

---

### 2.3 Módulos e Componentes a Avaliar
Considerando que o foco da avaliação são **Segurança, Confiabilidade e Manutenibilidade**, os módulos escolhidos serão aqueles que fornecem evidências para essas dimensões:

- **Segurança**: fluxos de autenticação, consentimento, proteção de dados em trânsito, políticas de privacidade, possibilidade de eliminação de dados.  
- **Confiabilidade**: estabilidade do fluxo de reporte diário de sintomas, comunicação cliente-servidor, recuperação frente a falhas de rede.  
- **Manutenibilidade**: análise do repositório público quanto a modularidade, organização do código, documentação e versionamento.  

---

### 2.4 Características Técnicas Observadas
O projeto é **open source** e está disponível no GitHub: [ProEpiDesenvolvimento](https://github.com/ProEpiDesenvolvimento).  
Com base nas evidências disponíveis:

- **Front-end / Mobile:** repositório `guardioes-app`, voltado a Android e iOS.  
- **Back-end / API:** repositório `guardioes-api`, desenvolvido em Ruby.  
- **Banco de Dados:** [ver depois].  
- **Hospedagem:** [ver depois].  
- **Comunicação:** API RESTful acessada pelos aplicativos móveis e web via HTTPS.  
- **Controle de versão:** GitHub, com issues, branches e histórico de commits públicos.  
- **Recursos adicionais:** módulo de gerenciamento (ePHEM) e dashboard de monitoramento, citados na documentação.  

---

### 2.5 ODS Relacionados
A avaliação se conecta principalmente a:  
- **ODS 3 – Saúde e Bem-Estar**: fortalecimento da vigilância epidemiológica, combate à desinformação e promoção da participação cidadã.  
- **ODS 9 – Indústria, Inovação e Infraestrutura**: desenvolvimento e manutenção de infraestrutura digital de saúde pública.  
- **ODS 16 – Paz, Justiça e Instituições Eficazes**: promoção da transparência no uso de dados e confiança nas instituições de saúde.  
