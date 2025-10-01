# 3. Identificação do tipo de produto a ser avaliado

## 3.1 Produto Principal
O **Guardiões da Saúde** é um aplicativo gratuito de vigilância participativa em saúde pública.  
Sua **natureza** é de um sistema digital multiplataforma (aplicativo móvel e web), cujo propósito é **permitir que cidadãos reportem diariamente seu estado de saúde** e recebam orientações, além de apoiar gestores de saúde com dados em tempo real.  

As **funções centrais** incluem:  
- Registro diário de sintomas e estado de saúde.  
- Fornecimento de orientações de saúde e localização de serviços (UPAs, farmácias).  
- Vinculação a instituições (Vigilância Ativa Institucional) para disparo de alertas a equipes de saúde.  
- Disponibilização de informações confiáveis em saúde.  

---

## 3.2 Produto Principal Especificado
- **Nome:** Guardiões da Saúde  
- **Categoria:** Produto **COTS/MOTS** (software de uso público, open-source, com possibilidade de adaptações institucionais)  
- **Plataformas:** Android, iOS e Web  
- **Versão / recorte avaliado:**  
  - iOS: versão 3.4.6 (requer iOS 12.0 ou posterior)  
  - Android: [indicar depois]  
  - Web: [URL/versão observada em DD/MM/AAAA]  
  - Backend/API: repositório público `guardioes-api`  

---

## 3.3 Módulos e Componentes a Avaliar
Considerando que o foco da avaliação são **Segurança, Confiabilidade e Manutenibilidade**, os módulos escolhidos serão aqueles que fornecem evidências para essas dimensões:

- **Segurança**: fluxos de autenticação, consentimento, proteção de dados em trânsito, políticas de privacidade, possibilidade de eliminação de dados.  
- **Confiabilidade**: estabilidade do fluxo de reporte diário de sintomas, comunicação cliente-servidor, recuperação frente a falhas de rede.  
- **Manutenibilidade**: análise do repositório público quanto a modularidade, organização do código, documentação e versionamento.  

---

## 3.4 Características Técnicas Observadas
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

## 3.5 ODS Relacionados
A avaliação se conecta principalmente a:  
- **ODS 3 – Saúde e Bem-Estar**: fortalecimento da vigilância epidemiológica, combate à desinformação e promoção da participação cidadã.  
- **ODS 9 – Indústria, Inovação e Infraestrutura**: desenvolvimento e manutenção de infraestrutura digital de saúde pública.  
- **ODS 16 – Paz, Justiça e Instituições Eficazes**: promoção da transparência no uso de dados e confiança nas instituições de saúde.  


