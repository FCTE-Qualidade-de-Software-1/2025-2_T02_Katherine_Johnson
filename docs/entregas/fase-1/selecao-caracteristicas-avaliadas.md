# 5. Seleção das características avaliadas

## 5.1 Critérios de Priorização

Para sistematizar a priorização das subcaracterísticas de qualidade, aplicou-se o método MoSCoW, que classifica os elementos em quatro grupos principais:

- **Must have (Essencial):** requisitos indispensáveis para a viabilidade do sistema.  
- **Should have (Relevante):** requisitos importantes, mas que podem ser adiados sem inviabilizar a solução.  
- **Could have (Oportuno):** requisitos desejáveis, que agregam valor, mas não são críticos.  
- **Won’t have (Fora do escopo atual):** requisitos de baixa prioridade, intencionalmente excluídos nesta fase.  

Cada categoria foi associada a um peso quantitativo, de modo a simplificar o processo de avaliação:  
- Must = 4  
- Should = 3  
- Could = 2  
- Won’t = 0  

---

## 5.2 Priorização das Subcaracterísticas

### 5.2.1 Priorização pelo método MoSCoW

<p align="center"> Tabela 1 - Priorização pelo método MoSCoW </p>

| Subcaracterística        | Característica     | Categoria MoSCoW | Peso | Decisão Final       |
|---------------------------|-------------------|------------------|------|---------------------|
| Confidencialidade         | Segurança         | Must             | 4    | Será analisada      |
| Integridade               | Segurança         | Must             | 4    | Será analisada      |
| Autenticidade             | Segurança         | Should           | 3    | Não será analisada  |
| Não-repúdio               | Segurança         | Could            | 2    | Não será analisada  |
| Responsabilidade          | Segurança         | Could            | 2    | Não será analisada  |
| Maturidade                | Confiabilidade    | Must             | 4    | Será analisada      |
| Disponibilidade           | Confiabilidade    | Should           | 3    | Será analisada      |
| Tolerância a falhas       | Confiabilidade    | Must             | 4    | Será analisada      |
| Capacidade de recuperação | Confiabilidade    | Should           | 3    | Não será analisada  |
| Modularidade              | Manutenibilidade | Could            | 2    | Não será analisada  |
| Reusabilidade             | Manutenibilidade | Should           | 3    | Não será analisada  |
| Analisabilidade           | Manutenibilidade | Must             | 4    | Será analisada      |
| Modificabilidade          | Manutenibilidade | Should           | 3    | Será analisada      |
| Testabilidade             | Manutenibilidade | Must             | 4    | Será analisada      |

<p align="center"><b>Fonte: </b>Autores</p>

---

### 5.2.2 Comparativo de Subcaracterísticas por Risco, Impacto e Esforço

<p align="center"> Tabela 2 - Comparativo de Subcaracterísticas por Risco, Impacto e Esforço </p>

| Subcaracterística        | Característica     | Risco se ausente | Impacto para stakeholders                                  | Esforço de análise                  | Decisão Final   |
|---------------------------|-------------------|------------------|-------------------------------------------------------------|-------------------------------------|-----------------|
| Confidencialidade         | Segurança         | Alto             | Alto (LGPD, cidadãos, confiança institucional)              | Médio (auditoria de acesso, criptografia) | Selecionada |
| Integridade               | Segurança         | Alto             | Alto (consistência dos dados, gestores, pesquisadores)      | Médio (validação de logs, redundância)   | Selecionada |
| Autenticidade             | Segurança         | Médio            | Moderado (usuários autenticados, voluntários)               | Médio (análise de mecanismos de login)  | Não selecionada |
| Não-repúdio               | Segurança         | Médio            | Moderado (auditoria, implicações jurídicas)                 | Alto (implementação de trilhas formais) | Não selecionada |
| Responsabilidade          | Segurança         | Médio            | Médio (accountability, rastreabilidade de ações)            | Alto (auditoria extensa de registros)   | Não selecionada |
| Maturidade                | Confiabilidade    | Alto             | Alto (estabilidade, confiança do usuário final)             | Médio (monitoramento em produção)       | Selecionada |
| Disponibilidade           | Confiabilidade    | Alto             | Alto (serviço contínuo, gestores e cidadãos dependentes)    | Médio (simulação de carga e redundância)| Selecionada |
| Tolerância a falhas       | Confiabilidade    | Alto             | Alto (resiliência, continuidade do serviço)                 | Alto (testes de falhas controladas)     | Selecionada |
| Capacidade de recuperação | Confiabilidade    | Médio            | Moderado (tempo de retomada, impacto em emergências)        | Alto (testes de recuperação e backup)   | Não selecionada |
| Modularidade              | Manutenibilidade | Médio            | Moderado (impacto na escalabilidade futura)                 | Alto (refatoração e análise estrutural) | Não selecionada |
| Reusabilidade             | Manutenibilidade | Médio            | Moderado (reduz custos de manutenção)                       | Médio (avaliação arquitetural)          | Não selecionada |
| Analisabilidade           | Manutenibilidade | Alto             | Alto (detecção rápida de falhas, suporte técnico)           | Médio (ferramentas de análise estática) | Selecionada |
| Modificabilidade          | Manutenibilidade | Alto             | Alto (facilidade de evolução, novas versões)                | Médio (avaliação de código-fonte)       | Selecionada |
| Testabilidade             | Manutenibilidade | Alto             | Alto (garante confiabilidade nos ciclos de teste)           | Médio (construção de testes automatizados) | Selecionada |

<p align="center"><b>Fonte: </b>Autores</p>

---

## Referências Bibliográficas

-   [1] INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. ISO/IEC 25010:2011 — Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models. Geneva: ISO, 2011.  
    Disponível em: <https://cdn.standards.iteh.ai/samples/35733/2ca18b477b7845a5b8cae39d6de0c098/ISO-IEC-25010-2011.pdf>. Acesso em: 01 out. 2025.

---

## Histórico de Versões

| Versão | Data       | Descrição                        | Autor(es)                   |
|--------|------------|----------------------------------|-----------------------------|
| 1.0    | 01/10/2025 | Elaboração inicial do documento | [Uires Carlos de Oliveira](https://github.com/uires2023)    |