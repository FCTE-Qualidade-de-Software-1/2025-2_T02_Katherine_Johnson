# Fase 1

# 1. PROPÓSITO DA AVALIAÇÃO  

## 1.1 Contexto e Motivação  
O enfrentamento de surtos e crises de saúde depende muito da capacidade de coletar, analisar e entender dados de forma rápida e segura. Nesse cenário, a vigilância participativa é essencial, pois permite que a própria população ajude no monitoramento de sintomas e possíveis focos de epidemias.  

O **Guardiões da Saúde**, desenvolvido pela ProEpi, é um software de código aberto criado justamente para isso: mobilizar cidadãos e profissionais de saúde na notificação de sintomas, dando aos gestores acesso ágil a informações importantes para a tomada de decisão e precavendo deles de decisões baseadas em Fake News.  

Mas a eficiência do sistema não depende só da parte técnica, e sim também da participação sincera e constante dos usuários. Se as pessoas não registrarem seus sintomas com frequência, ou deixarem de usar o app por falta de motivação, os dados podem ficar incompletos e acabar prejudicando a credibilidade do sistema. Por isso, além da parte tecnológica, a ferramenta também precisa **incentivar campanhas de saúde e educação sanitária** que engajem a população.  

Assim, a força do Guardiões da Saúde está em três pilares técnicos — **Segurança, Confiabilidade e Manutenibilidade** — junto de uma boa estratégia de **mobilização social** para garantir o uso correto e contínuo.  


## 1.2 Declaração do Propósito  
"Este trabalho apresenta um plano de avaliação da qualidade do **Guardiões da Saúde**, com foco em **Segurança, Confiabilidade e Manutenibilidade**, conforme a ISO/IEC 25010. O objetivo é analisar de forma prática e sistemática se o software protege bem os dados, se funciona de maneira estável em situações críticas e se sua base de código é fácil de manter e evoluir. Também será considerado o papel do app em **estimular que os usuários participem de forma sincera e constante**, ajudando campanhas de saúde pública e garantindo que os dados coletados sejam realmente úteis. A avaliação vai incluir tanto o aplicativo móvel quanto os serviços de backend disponíveis no repositório oficial."  


## 1.3 Objetivos Específicos  
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

### Manutenibilidade  
- Medir o **MTTR (Mean Time To Repair)**, ou seja, quanto tempo leva em média para corrigir falhas.  
- Verificar a **facilidade de modificar o sistema**, analisando modularidade, legibilidade e boas práticas no código.  
- Avaliar a **documentação técnica e o pipeline de desenvolvimento**, garantindo suporte à evolução sustentável.  


## 1.4 Alinhamento com Objetivos de Negócio e ODS  
A avaliação proposta está ligada diretamente aos objetivos do Guardiões da Saúde e aos **Objetivos de Desenvolvimento Sustentável (ODS)**:  

- **ODS 3 – Saúde e Bem-Estar**: fortalecer a vigilância epidemiológica (Meta 3.d) e **estimular a participação da população** de forma consciente, apoiando campanhas sanitárias (Meta 3.3).  
- **ODS 9 – Inovação e Infraestrutura**: melhorar continuamente a manutenibilidade para sustentar a evolução tecnológica do sistema (Meta 9.c).  

### Benefícios esperados para o negócio:  
- **Credibilidade e confiança**: mostrar para os usuários que seus dados estão seguros e são tratados de forma responsável.  
- **Engajamento social**: motivar o uso contínuo e sincero do app, com apoio de campanhas de conscientização e integração com políticas públicas.  
- **Agilidade em crises de saúde**: reduzir falhas e garantir que o sistema funcione bem em momentos críticos.  
- **Sustentabilidade técnica**: manter o software fácil de corrigir e evoluir, evitando acúmulo de problemas a longo prazo.  

