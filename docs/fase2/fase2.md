# Fase 2 - Especificar a Avaliação

## 1. Introdução

<div style="text-align: justify; text-indent: 2cm;">
O objetivo da Fase 2: Especificar a Avaliação é detalhar, de forma objetiva, como as características de qualidade selecionadas <b>(Adequação Funcional e Compatibilidade)</b> serão medidas e julgadas.
</div>

<div style="text-align: justify; text-indent: 2cm;">
Para garantir que a avaliação seja repetível, reprodutível e rastreável, esta fase será estruturada utilizando o <b>Goal-Question-Metric (GQM) Framework</b>. O GQM conecta os objetivos de alto nível (Goal) estabelecidos na Fase 1 às perguntas de avaliação (Question) e, por fim, às medidas concretas (Metric) que serão coletadas na Fase 4.
</div>

<div style="text-align: justify; text-indent: 2cm;">
As métricas definidas a seguir, juntamente com seus níveis de pontuação e critérios de julgamento, servirão de insumo direto para a Fase 3.
</div>

---

## 2. Objetivos Gerais

<font size="3"><p style="text-align: center">Tabela 1: Descrição dos Objetivos gerais da avaliação</p></font>

| Característica de Qualidade | Objetivo (Goal) GQM                                                                                                             |
| :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------ |
| **Adequação Funcional**     | Avaliar se as funções essenciais da jornada do candidato (busca, filtros e candidatura) são corretas e completas na versão Web. |
| **Compatibilidade**         | Avaliar se o LinkedIn Web consegue coexistir sem impacto negativo com outras aplicações e extensões no ambiente do usuário.     |

---

## 3. Perguntas e Hipóteses de Medição

<div style="text-align: justify; text-indent: 2cm;">
Para decompor os objetivos de análise da <b>Adequação Funcional</b> e da <b>Compatibilidade</b>, foram formuladas as seguintes perguntas (extraídas da Fase 2) e suas respectivas hipóteses. As hipóteses tornam explícito o conhecimento atual ou esperado sobre o sistema, que será validado (ou refutado) pelas métricas definidas.
</div>

---

#### Característica: Adequação Funcional

**Questão 1 (Q1):** Qual o grau de precisão e confiabilidade das funções críticas do sistema?  
*(Relacionada às métricas M1.1.1, M1.1.2, M1.1.3)*

- **Hipótese 1.1 (H1.1):** A "Taxa de Conformidade de Busca" (M1.1.1) será alta (**Nível Bom, 95-99%**) para buscas com até dois filtros (ex: cargo e localidade). No entanto, ao aplicar três ou mais filtros (conforme o escopo 6.1), a taxa cairá para um **Nível Insuficiente (< 84%)**, apresentando resultados que não correspondem a todos os critérios.

- **Hipótese 1.2 (H1.2):** O "Tempo Médio de Resposta da Função de Busca" (M1.1.3) permanecerá em **Nível Aceitável (entre 2s e 4s)**. Espera-se que a complexidade da consulta com múltiplos filtros impacte a performance, mas sem torná-la crítica.

- **Hipótese 1.3 (H1.3):** A "Taxa de Erro de Candidatura" (M1.1.2) no fluxo de "candidatura simplificada" será superior a **6% (Nível Aceitável)**, indicando falhas intermitentes e recuperáveis, provavelmente associadas à integração com sistemas ATS externos.

---

**Questão 2 (Q2):** O conjunto de funcionalidades oferecidas é suficiente e completo para o sucesso das tarefas do usuário?  
*(Relacionada às métricas M1.2.1, M1.2.2, M1.2.3)*

- **Hipótese 2.1 (H2.1):** A "Completude de Campos Críticos" (M1.2.1) para a edição da seção "Experiência" (Objeto de Avaliação 6.1) será de **100% (Nível Excelente)**.

- **Hipótese 2.2 (H2.2):** A "Cobertura de Funcionalidades Relevantes" (M1.2.2) para a jornada principal do candidato (buscar, salvar vaga, aplicar) será de **Nível Excelente (≥ 95%)**, indicando que o LinkedIn oferece todas as ações esperadas para essas tarefas.

- **Hipótese 2.3 (H2.3):** A "Disponibilidade de Recursos Complementares" (M1.2.3), especificamente as funções "salvar vaga" e "criar alerta", apresentará intermitências durante os testes, resultando em uma disponibilidade de **Nível Aceitável (entre 80-89%)**.

---

#### Característica: Compatibilidade (Coexistência)

**Questão 3 (Q3):** O uso da aplicação interfere negativamente no desempenho de outras aplicações no ambiente operacional do usuário?  
*(Relacionada às métricas M2.1.1, M2.1.2, M2.1.3)*

- **Hipótese 3.1 (H3.1):** O "Pico de Consumo de Recursos" (M2.1.1) da aplicação web atingirá o **Nível Crítico (RAM ≥ 1200MB)** nos testes em navegadores com extensões ativas, após 15 minutos de navegação contínua entre vagas e perfis.

- **Hipótese 3.2 (H3.2):** A "Taxa de Conflito com Extensões de Navegador" (M2.1.2) será de **0% (Nível Excelente)** para extensões passivas (ex: bloqueadores de anúncio), mas apresentará um **Nível Insuficiente (> 11%)** de conflitos com extensões ativas que interagem com o DOM (ex: corretores gramaticais), causando falhas na renderização de formulários.

- **Hipótese 3.3 (H3.3):** A ocorrência de travamentos completos (que exijam recuperação) será baixa. No entanto, quando ocorrerem, o "Tempo Médio de Recuperação após Travamento" (M2.1.3) será superior a **20 segundos (Nível Crítico)**, exigindo uma atualização manual da página (F5) pelo usuário.


## 4. Adequação Funcional

<div style="text-align: justify; text-indent: 2cm;">
A Adequação Funcional refere-se à capacidade do LinkedIn de fornecer as funcionalidades necessárias para atender aos objetivos do usuário na sua jornada como candidato. Esta é uma característica de Prioridade Alta, pois é a base da proposta de valor da plataforma. As subcaracterísticas analisadas são: <b>Correção Funcional</b> e <b>Completude Funcional</b>.
</div>

### 4.1 Objetivos

#### 4.1.1 Correção Funcional

<font size="3"><p style="text-align: center">Tabela 2: Descrição do Objetivo de Medição de Correção Funcional</p></font>

| Elemento                  | Descrição                      |
| :------------------------ | :----------------------------- |
| **Analisar:**             | Funções de busca e candidatura |
| **Com o propósito de**    | Avaliar precisão               |
| **Com respeito a**        | Correção Funcional             |
| **Do ponto de vista de:** | Candidato a vagas              |
| **No contexto de:**       | LinkedIn Web                   |

#### 4.1.2 Completude Funcional

<font size="3"><p style="text-align: center">Tabela 3: Descrição do Objetivo de Medição de Completude Funcional</p></font>

| Elemento                  | Descrição                                 |
| :------------------------ | :---------------------------------------- |
| **Analisar:**             | Funcionalidades da jornada de candidatura |
| **Com o propósito de**    | Verificar completude                      |
| **Com respeito a**        | Completude Funcional                      |
| **Do ponto de vista de:** | Usuário candidato                         |
| **No contexto de:**       | Navegador Web (desktop)                   |

### 4.2 Questões e Métricas

<font size="3"><p style="text-align: center">Tabela 4: Questões e Métricas - Adequação Funcional</p></font>

| Subcaracterística        | Questão (Question)                                                                                              | Métricas (Metrics)                                                                                                                                                                       |
| :----------------------- | :-------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Correção Funcional**   | **Q1:** Qual o grau de precisão e confiabilidade das funções críticas do sistema?                               | **M1.1.1 - Taxa de Conformidade de Busca**<br>**M1.1.2 - Taxa de Erro de Candidatura**<br>**M1.1.3 - Tempo Médio de Resposta da Função de Busca**                                        |
| **Completude Funcional** | **Q2:** O conjunto de funcionalidades oferecidas é suficiente e completo para o sucesso das tarefas do usuário? | **M1.2.1 - Completude de Campos Críticos**<br>**M1.2.2 - Cobertura de Funcionalidades Relevantes**<br>**M1.2.3 - Disponibilidade de Recursos Complementares (ex: salvar vaga, alertas)** |

---

### 4.3 Níveis de Pontuação e Critérios para Julgamento

A pontuação é baseada em uma escala de 1 (Crítico) a 5 (Excelente), mas os faróis são ajustados conforme a natureza da métrica.

#### M1.1.1 - Taxa de Conformidade de Busca

<font size="3"><p style="text-align: center">Tabela 5: Níveis e critérios da Métrica 1.1.1</p></font>

| Nível | Pontuação | Critério de Julgamento                                                        |
| :---- | :-------- | :---------------------------------------------------------------------------- |
| 5     | 100%      | **Excelente (Verde):** Nenhum resultado incorreto encontrado.                 |
| 4     | 95–99%    | **Bom (Verde):** Resultados precisos, falhas mínimas.                         |
| 3     | 85–94%    | **Aceitável (Amarelo):** Pequenas inconsistências ocasionais.                 |
| 2     | 70–84%    | **Insuficiente (Laranja):** Filtros inconsistentes impactam a confiabilidade. |
| 1     | < 70%     | **Crítico (Vermelho):** Resultados incorretos comprometem a função principal. |

#### M1.1.2 - Taxa de Erro de Candidatura

<font size="3"><p style="text-align: center">Tabela 6: Níveis e critérios da Métrica 1.1.2</p></font>

| Nível | Pontuação | Critério de Julgamento                                             |
| :---- | :-------- | :----------------------------------------------------------------- |
| 5     | 0%        | **Excelente (Verde):** Nenhum erro ao enviar candidatura.          |
| 4     | 1–5%      | **Bom (Verde):** Erros pontuais, não recorrentes.                  |
| 3     | 6–10%     | **Aceitável (Amarelo):** Alguns erros recuperáveis.                |
| 2     | 11–20%    | **Insuficiente (Laranja):** Falhas frequentes que impactam o uso.  |
| 1     | > 20%     | **Crítico (Vermelho):** Envio de candidatura frequentemente falha. |

#### M1.1.3 - Tempo Médio de Resposta da Função de Busca

<font size="3"><p style="text-align: center">Tabela 7: Níveis e critérios da Métrica 1.1.3</p></font>

| Nível | Pontuação | Critério de Julgamento                                            |
| :---- | :-------- | :---------------------------------------------------------------- |
| 5     | ≤ 1s      | **Excelente (Verde):** Resposta instantânea e fluida.             |
| 4     | 1–2s      | **Bom (Verde):** Leve latência, mas aceitável.                    |
| 3     | 2–4s      | **Aceitável (Amarelo):** Perceptível, mas sem prejuízo relevante. |
| 2     | 4–6s      | **Insuficiente (Laranja):** Lentidão que afeta a experiência.     |
| 1     | > 6s      | **Crítico (Vermelho):** Tempo excessivo de resposta.              |

#### M1.2.1 - Completude de Campos Críticos

<font size="3"><p style="text-align: center">Tabela 8: Níveis e critérios da Métrica 1.2.1</p></font>

| Nível | Pontuação | Critério de Julgamento                                                           |
| :---- | :-------- | :------------------------------------------------------------------------------- |
| 5     | 100%      | **Excelente (Verde):** Todos os campos críticos presentes e funcionais.          |
| 4     | 90–99%    | **Bom (Verde):** Poucos campos secundários ausentes.                             |
| 3     | 80–89%    | **Aceitável (Amarelo):** Falta de campo importante, mas não impeditiva.          |
| 2     | 70–79%    | **Insuficiente (Laranja):** Campos críticos ausentes geram retrabalho.           |
| 1     | < 70%     | **Crítico (Vermelho):** Falta de campos essenciais impede a conclusão da tarefa. |

#### M1.2.2 - Cobertura de Funcionalidades Relevantes

<font size="3"><p style="text-align: center">Tabela 9: Níveis e critérios da Métrica 1.2.2</p></font>

| Nível | Pontuação | Critério de Julgamento                                                    |
| :---- | :-------- | :------------------------------------------------------------------------ |
| 5     | ≥ 95%     | **Excelente (Verde):** Todas as funcionalidades relevantes implementadas. |
| 4     | 85–94%    | **Bom (Verde):** Funções principais presentes, poucas faltantes.          |
| 3     | 75–84%    | **Aceitável (Amarelo):** Algumas lacunas relevantes.                      |
| 2     | 60–74%    | **Insuficiente (Laranja):** Várias funções relevantes ausentes.           |
| 1     | < 60%     | **Crítico (Vermelho):** Grande parte das funcionalidades ausentes.        |

#### M1.2.3 - Disponibilidade de Recursos Complementares

<font size="3"><p style="text-align: center">Tabela 10: Níveis e critérios da Métrica 1.2.3</p></font>

| Nível | Pontuação                | Critério de Julgamento                                                                    |
| :---- | :----------------------- | :---------------------------------------------------------------------------------------- |
| 5     | ≥ 95% de disponibilidade | **Excelente (Verde):** Recursos complementares (alertas, salvar vaga) sempre disponíveis. |
| 4     | 90–94%                   | **Bom (Verde):** Alta disponibilidade, pequenas interrupções.                             |
| 3     | 80–89%                   | **Aceitável (Amarelo):** Intermitências ocasionais.                                       |
| 2     | 70–79%                   | **Insuficiente (Laranja):** Recursos frequentemente indisponíveis.                        |
| 1     | < 70%                    | **Crítico (Vermelho):** Recursos quase sempre inoperantes.                                |

---

## 5. Compatibilidade

<div style="text-align: justify; text-indent: 2cm;">
A Compatibilidade refere-se à capacidade do produto de coexistir e trocar informações com outros sistemas, compartilhando o mesmo ambiente e recursos. Esta característica também é de Prioridade Alta porque conflitos de recursos ou problemas de integração prejudicam a experiência fluida e profissional. A subcaracterística analisada é a <b>Coexistência</b>.
</div>

### 5.1 Objetivo

<font size="3"><p style="text-align: center">Tabela 11: Descrição do Objetivo de Medição de Compatibilidade</p></font>

| Elemento                  | Descrição                                       |
| :------------------------ | :---------------------------------------------- |
| **Analisar:**             | Comportamento do LinkedIn com outras aplicações |
| **Com o propósito de**    | Avaliar coexistência                            |
| **Com respeito a**        | Coexistência                                    |
| **Do ponto de vista de:** | Usuário multitarefa                             |
| **No contexto de:**       | Navegador Web com extensões                     |


### 5.2 Questões e Métricas

<font size="3"><p style="text-align: center">Tabela 12: Questões e Métricas - Compatibilidade</p></font>

| Subcaracterística | Questão (Question)                                                                                                        | Métricas (Metrics)                                                                                                                                                                    |
| :---------------- | :------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Coexistência**  | **Q3:** O uso da aplicação interfere negativamente no desempenho de outras aplicações no ambiente operacional do usuário? | **M2.1.1 - Pico de Consumo de Recursos (CPU/Memória)**<br><br>**M2.1.2 - Taxa de Conflito com Extensões de Navegador**<br><br>**M2.1.3 - Tempo Médio de Recuperação após Travamento** |

---

### 5.3 Níveis de Pontuação e Critérios para Julgamento

#### M2.1.1 - Pico de Consumo de Recursos

<font size="3"><p style="text-align: center">Tabela 13: Níveis e critérios da Métrica 2.1.1</p></font>

| Nível | Pontuação                 | Critério de Julgamento                                        |
| :---- | :------------------------ | :------------------------------------------------------------ |
| 5     | CPU < 10%, RAM < 500MB    | **Excelente (Verde):** Uso mínimo, sem impacto perceptível.   |
| 4     | CPU < 20%, RAM < 800MB    | **Bom (Verde):** Uso leve, estável.                           |
| 3     | CPU < 30%, RAM < 1000MB   | **Aceitável (Amarelo):** Consumo médio, monitorável.          |
| 2     | CPU < 40%, RAM < 1200MB   | **Insuficiente (Laranja):** Pode causar lentidão.             |
| 1     | CPU ≥ 40% ou RAM ≥ 1200MB | **Crítico (Vermelho):** Compromete a estabilidade do sistema. |

#### M2.1.2 - Taxa de Conflito com Extensões de Navegador

<font size="3"><p style="text-align: center">Tabela 14: Níveis e critérios da Métrica 2.1.2</p></font>

| Nível | Pontuação      | Critério de Julgamento                                                     |
| :---- | :------------- | :------------------------------------------------------------------------- |
| 5     | 0% de conflito | **Excelente (Verde):** Nenhum problema de compatibilidade.                 |
| 4     | 1–5%           | **Bom (Verde):** Conflitos raros e isolados.                               |
| 3     | 6–10%          | **Aceitável (Amarelo):** Conflitos ocasionais sem perda de funcionalidade. |
| 2     | 11–20%         | **Insuficiente (Laranja):** Conflitos frequentes.                          |
| 1     | > 20%          | **Crítico (Vermelho):** Conflitos graves impedem o uso normal.             |

#### M2.1.3 - Tempo Médio de Recuperação após Travamento

<font size="3"><p style="text-align: center">Tabela 15: Níveis e critérios da Métrica 1.2.3</p></font>

| Nível | Pontuação | Critério de Julgamento                                 |
| :---- | :-------- | :----------------------------------------------------- |
| 5     | ≤ 2s      | **Excelente (Verde):** Recuperação imediata.           |
| 4     | 3–5s      | **Bom (Verde):** Rápida retomada de operação.          |
| 3     | 6–10s     | **Aceitável (Amarelo):** Recuperação perceptível.      |
| 2     | 11–20s    | **Insuficiente (Laranja):** Lentidão na retomada.      |
| 1     | > 20s     | **Crítico (Vermelho):** Sistema exige reinício manual. |

---

## 6. Histórico de Versões

<font size="3"><p style="text-align: center">Tabela 16: Histórico de Versões</p></font>

| Versão | Descrição                                                  | Autor                                                                                                                                                                                                                                                                                         |    Data    |                      Revisor                       |
| :----: | :--------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------: | :------------------------------------------------: |
|  1.0   | Criação do documento                                       | [Bruno Cruz](https://github.com/brunocrzz), [Gabriel Mendes](https://github.com/gbevi), [João Moreira](https://github.com/joaofmoreiraa), [Maria Eduarda Pereira](https://github.com/maaduh), [Mayara Marques](https://github.com/maymarquee), [Pedro Túlio](https://github.com/PedrooCamilo) | 14/10/2025 |                       Todos                        |
|  1.1   | Adição da introdução e GQM's                               | Mesmo autores                                                                                                                                                                                                                                                                                 | 14/10/2025 |                       Todos                        |
|  1.2   | Adição dos Níveis de Pontuação e Critérios para Julgamento | Mesmo autores                                                                                                                                                                                                                                                                                 | 14/10/2025 |                       Todos                        |
|  1.3   | Ajuste de erro de escrita                                  | [Bruno Cruz](https://github.com/brunocrzz)                                                                                                                                                                                                                                                    | 15/10/2025 |                         -                          |
|  1.4   | Adiciona objetivos                                         | [Mayara Marques](https://github.com/maymarquee)                                                                                                                                                                                                                                               | 23/10/2025 |     [Gabriel Mendes](https://github.com/gbevi)     |
|  1.5   | Inclusão de novas métricas e detalhamento dos critérios    | [Gabriel Mendes](https://github.com/gbevi)                                                                                                                                                                                                                                                    | 24/10/2025 |                       Todos                        |
|  1.6   | Refinamento das questões após PC2                          | [Maria Eduarda Pereira](https://github.com/maaduh)                                                                                                                                                                                                                                            | 24/10/2025 |  [Mayara Marques](https://github.com/maymarquee)   |
|  1.7   | Adição das hipóteses                                       | [João Moreira](https://github.com/joaofmoreiraa)                                                                                                                                                                                                                                              | 24/10/2025 | [Maria Eduarda Pereira](https://github.com/maaduh) |
|  1.8   | Reajuste de objetivos, formatação e erros gerais           | [Bruno Cruz](https://github.com/brunocrzz)                                                                                                                                                                                                                                                    | 26/11/2025 |                         -                          |
