# 3. Características do Produto

## 3.1 Visão Geral do Produto

O **Guardiões da Saúde** é um serviço digital de vigilância participativa voltado principalmente a cidadãos que registram voluntariamente seu estado de saúde, com benefícios diretos também para perfis vinculados a instituições (como estudantes) e para gestores que utilizam os dados agregados no monitoramento e na resposta em saúde pública. Além de coletar relatos, o app atua como canal de informação e engajamento, trazendo **dicas gerais de saúde**, **notícias confiáveis** e **quizzes** educativos que incentivam o uso contínuo e a educação sanitária. O acesso é **mobile** (Android e iOS) e há uma **plataforma web** para informações gerais.

Em linhas gerais, o usuário indica diariamente se está bem ou mal e, quando necessário, seleciona sintomas; a partir disso, recebe **orientações** personalizadas e pode localizar **serviços de saúde próximos** por meio de um **mapa**. Quando existe vínculo institucional, entra em ação a **Vigilância Ativa Institucional**, que **notifica** equipes responsáveis para acompanhamento mais ágil. O aplicativo também oferece uma **visão agregada no mapa**, apresentando a distribuição de relatos, ampliando a percepção situacional da comunidade e apoiando decisões de gestores.

## 3.2 Identificação das características do produto
Abaixo estão, de forma sintética, as principais características do **Guardiões da Saúde** consideradas nesta identificação do produto. As informações foram coletadas no repositório público [ProEpiDesenvolvimento](https://github.com/ProEpiDesenvolvimento) e nas lojas [Google Play](https://play.google.com/store) e [App Store](https://apps.apple.com/).

<p align="center"> Tabela 1 - Características do Produto </a> </p>

| Característica                                   | Descrição |
|---|---|
| **Nome**                                         | Guardiões da Saúde |
| **Versão**                                       | 3.4.6 |
| **Categoria (IEEE)**                             | COTS com particularizações possíveis (MOTS) |
| **Público-alvo**                                 | Cidadãos; perfis vinculados a instituições; gestores e equipes de saúde |
| **Plataformas**                                  | Android, iOS e acesso Web informativo |
| **Banco de dados**                               | PostgreSQL |
| **Tecnologias Frontend (mobile)**                | React Native / JavaScript |
| **Tecnologias Backend (API)**                    | Ruby on Rails e Docker |
| **Hardware (referência para avaliação)**         | Smartphones Android 5.0+ / iOS 12.0+ com GPS e rede móvel / Wi-Fi|
| **Conhecimento exigido em informática**          | Baixo (fluxos curtos, poucos toques, interface intuitiva) |
| **Conhecimento exigido no domínio da aplicação** | Baixo (informar estado de saúde, visualizar mapas, ranking e quizzes) |

<p align="center"><b>Fonte: </b>Autores; repositório público ProEpiDesenvolvimento e lojas Google Play e App Store</p>

## 3.3 Módulos e Componentes do Produto

A seguir apresentamos, em alto nível, os principais módulos e funcionalidades do **Guardiões da Saúde**. Cada subseção apresenta o objetivo do módulo, seu funcionamento básico e observações úteis para a avaliação.

### 3.3.1 Reporte diário de saúde
Permite que o usuário informe, de forma voluntária e rápida, seu estado de saúde (ex.: **bem** ou **mal**) e selecione sintomas quando aplicável. O envio gera um registro diário associado ao perfil e à localização aproximada (quando permitido), servindo como insumo para orientações ao usuário e análises agregadas.

### 3.3.2 Orientações pós-reporte
Após o envio do reporte, o app apresenta **orientações**. O conteúdo é educativo e busca orientar condutas básicas, reduzindo incertezas e reforçando boas práticas de saúde.

### 3.3.3 Mapa e localização de serviços
Oferece um **mapa** para localizar unidades de saúde próximas, utilizando GPS (com consentimento do usuário) e serviços de mapas. Ajuda o usuário a identificar pontos de cuidado disponíveis na região.

### 3.3.4 Vigilância Ativa Institucional
Funcionalidade opcional que permite **vincular** o perfil do usuário a uma **instituição acadêmica**. Quando o usuário reporta sintomas, o sistema pode **notificar equipes de saúde** da instituição, agilizando triagem, orientação e acompanhamento.

### 3.3.5 Conteúdos informativos
Canal interno com **dicas gerais de saúde**, **notícias confiáveis** e **quizzes** educativos. Visa combater desinformação, engajar o usuário no uso contínuo do app e promover educação sanitária de forma simples e contextualizada.

### 3.3.6 Visão agregada no mapa
Apresenta a **distribuição de relatos e sintomas por área** no mapa, ampliando a percepção situacional da comunidade. O objetivo é oferecer transparência e apoio a decisões, sem expor dados pessoais ou informações que identifiquem indivíduos.

### 3.3.7 Notificações e lembretes
Envia **lembretes** para estimular o reporte diário e **avisos** relevantes (por exemplo, mudanças importantes ou campanhas). Podem ser usadas notificações push no Android/iOS, respeitando permissões e preferências do usuário.


### 3.3.8 Autenticação e perfis de usuário
Inclui **criação de conta**, login, recuperação de acesso e gestão de **perfis**. Garante acesso controlado às funcionalidades e associa eventos (reportes, consentimentos) à identidade do usuário.

### 3.3.9 Acessibilidade e usabilidade básica
Conjunto de princípios e recursos que suportam **uso simples e inclusivo**. Focado em reduzir barreiras para diferentes níveis de letramento digital e de saúde.

### 3.3.10 Integração cliente-servidor (API)
Camada de comunicação entre aplicativos (Android/iOS/web) e os **serviços de backend** (API). É responsável por **transmitir dados com segurança**, sincronizar reportes e conteúdos, e manter a coerência entre o que o usuário vê e o que é armazenado/analizado no servidor.

---

## Histórico de Versões

| Versão | Descrição            | Autor(es)                                          | Data de Produção | 
| :----: | -------------------- | -------------------------------------------------- | :--------------: |
| `1.0`  | Criação do documento | [Arthur Trindade](https://github.com/trindadea)    |    28/09/2025    |
| `1.1`  | Revisão e ajustes pós feedback | [Arthur Trindade](https://github.com/trindadea)    |    01/10/2025    |
