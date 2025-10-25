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

## 2. Objetivos

| Característica de Qualidade | Objetivo (Goal) GQM |
| :--- | :--- |
| **Adequação Funcional** | **G1 (Geral):** Assegurar a eficácia das funcionalidades essenciais do LinkedIn para o sucesso profissional do usuário, na perspectiva de um candidato. |
| **Compatibilidade** | **G2 (Geral):** Garantir que o LinkedIn funcione harmoniosamente no ambiente operacional do usuário, coexistindo de forma eficiente com outros softwares. |

---

## 3. Adequação Funcional

<div style="text-align: justify; text-indent: 2cm;">
A Adequação Funcional refere-se à capacidade do LinkedIn de fornecer as funcionalidades necessárias para atender aos objetivos do usuário na sua jornada como candidato. Esta é uma característica de Prioridade Alta, pois é a base da proposta de valor da plataforma. As subcaracterísticas analisadas são: <b>Correção Funcional</b> e <b>Completude Funcional</b>.
</div>

### 3.1 GQM

<font size="3"><p style="text-align: center">Tabela 1: GQM - Adequação Funcional</p></font>

| Subcaracterística | Objetivo (Goal) | Questão (Question) | Métricas (Metrics) |
| :--- | :--- | :--- | :--- |
| **Correção Funcional** | Assegurar a eficácia das funcionalidades essenciais do LinkedIn. | **Q1:** Qual o grau de precisão e confiabilidade das funções críticas do sistema? | **M1.1.1 - Taxa de Conformidade de Busca**<br>**M1.1.2 - Taxa de Erro de Candidatura**<br>**M1.1.3 - Tempo Médio de Resposta da Função de Busca** |
| **Completude Funcional** | Assegurar a integralidade das funções essenciais ao usuário. | **Q2:** O conjunto de funcionalidades oferecidas é suficiente e completo para o sucesso das tarefas do usuário? | **M1.2.1 - Completude de Campos Críticos**<br>**M1.2.2 - Cobertura de Funcionalidades Relevantes**<br>**M1.2.3 - Disponibilidade de Recursos Complementares (ex: salvar vaga, alertas)** |

---

### 3.2 Níveis de Pontuação e Critérios para Julgamento

A pontuação é baseada em uma escala de 1 (Crítico) a 5 (Excelente), mas os faróis são ajustados conforme a natureza da métrica.

#### M1.1.1 - Taxa de Conformidade de Busca
| Nível | Pontuação | Critério de Julgamento |
| :--- | :--- | :--- |
| 5 | 100% | **Excelente (Verde):** Nenhum resultado incorreto encontrado. |
| 4 | 95–99% | **Bom (Verde):** Resultados precisos, falhas mínimas. |
| 3 | 85–94% | **Aceitável (Amarelo):** Pequenas inconsistências ocasionais. |
| 2 | 70–84% | **Insuficiente (Laranja):** Filtros inconsistentes impactam a confiabilidade. |
| 1 | < 70% | **Crítico (Vermelho):** Resultados incorretos comprometem a função principal. |

#### M1.1.2 - Taxa de Erro de Candidatura
| Nível | Pontuação | Critério de Julgamento |
| :--- | :--- | :--- |
| 5 | 0% | **Excelente (Verde):** Nenhum erro ao enviar candidatura. |
| 4 | 1–5% | **Bom (Verde):** Erros pontuais, não recorrentes. |
| 3 | 6–10% | **Aceitável (Amarelo):** Alguns erros recuperáveis. |
| 2 | 11–20% | **Insuficiente (Laranja):** Falhas frequentes que impactam o uso. |
| 1 | > 20% | **Crítico (Vermelho):** Envio de candidatura frequentemente falha. |

#### M1.1.3 - Tempo Médio de Resposta da Função de Busca
| Nível | Pontuação | Critério de Julgamento |
| :--- | :--- | :--- |
| 5 | ≤ 1s | **Excelente (Verde):** Resposta instantânea e fluida. |
| 4 | 1–2s | **Bom (Verde):** Leve latência, mas aceitável. |
| 3 | 2–4s | **Aceitável (Amarelo):** Perceptível, mas sem prejuízo relevante. |
| 2 | 4–6s | **Insuficiente (Laranja):** Lentidão que afeta a experiência. |
| 1 | > 6s | **Crítico (Vermelho):** Tempo excessivo de resposta. |

#### M1.2.1 - Completude de Campos Críticos
| Nível | Pontuação | Critério de Julgamento |
| :--- | :--- | :--- |
| 5 | 100% | **Excelente (Verde):** Todos os campos críticos presentes e funcionais. |
| 4 | 90–99% | **Bom (Verde):** Poucos campos secundários ausentes. |
| 3 | 80–89% | **Aceitável (Amarelo):** Falta de campo importante, mas não impeditiva. |
| 2 | 70–79% | **Insuficiente (Laranja):** Campos críticos ausentes geram retrabalho. |
| 1 | < 70% | **Crítico (Vermelho):** Falta de campos essenciais impede a conclusão da tarefa. |

#### M1.2.2 - Cobertura de Funcionalidades Relevantes
| Nível | Pontuação | Critério de Julgamento |
| :--- | :--- | :--- |
| 5 | ≥ 95% | **Excelente (Verde):** Todas as funcionalidades relevantes implementadas. |
| 4 | 85–94% | **Bom (Verde):** Funções principais presentes, poucas faltantes. |
| 3 | 75–84% | **Aceitável (Amarelo):** Algumas lacunas relevantes. |
| 2 | 60–74% | **Insuficiente (Laranja):** Várias funções relevantes ausentes. |
| 1 | < 60% | **Crítico (Vermelho):** Grande parte das funcionalidades ausentes. |

#### M1.2.3 - Disponibilidade de Recursos Complementares
| Nível | Pontuação | Critério de Julgamento |
| :--- | :--- | :--- |
| 5 | ≥ 95% de disponibilidade | **Excelente (Verde):** Recursos complementares (alertas, salvar vaga) sempre disponíveis. |
| 4 | 90–94% | **Bom (Verde):** Alta disponibilidade, pequenas interrupções. |
| 3 | 80–89% | **Aceitável (Amarelo):** Intermitências ocasionais. |
| 2 | 70–79% | **Insuficiente (Laranja):** Recursos frequentemente indisponíveis. |
| 1 | < 70% | **Crítico (Vermelho):** Recursos quase sempre inoperantes. |

---

## 4. Compatibilidade

<div style="text-align: justify; text-indent: 2cm;">
A Compatibilidade refere-se à capacidade do produto de coexistir e trocar informações com outros sistemas, compartilhando o mesmo ambiente e recursos. Esta característica também é de Prioridade Alta porque conflitos de recursos ou problemas de integração prejudicam a experiência fluida e profissional. A subcaracterística analisada é a <b>Coexistência</b>.
</div>

### 4.1 GQM

<font size="3"><p style="text-align: center">Tabela 2: GQM - Compatibilidade</p></font>

| Subcaracterística | Objetivo (Goal) | Questão (Question) | Métricas (Metrics) |
| :--- | :--- | :--- | :--- |
| **Coexistência** | Garantir funcionamento harmonioso no ambiente do usuário. | **Q3:** O uso da aplicação interfere negativamente no desempenho de outras aplicações no ambiente operacional do usuário? | **M2.1.1 - Pico de Consumo de Recursos (CPU/Memória)**<br>**M2.1.2 - Taxa de Conflito com Extensões de Navegador**<br>**M2.1.3 - Tempo Médio de Recuperação após Travamento** |

---

### 4.2 Níveis de Pontuação e Critérios para Julgamento

#### M2.1.1 - Pico de Consumo de Recursos
| Nível | Pontuação | Critério de Julgamento |
| :--- | :--- | :--- |
| 5 | CPU < 10%, RAM < 500MB | **Excelente (Verde):** Uso mínimo, sem impacto perceptível. |
| 4 | CPU < 20%, RAM < 800MB | **Bom (Verde):** Uso leve, estável. |
| 3 | CPU < 30%, RAM < 1000MB | **Aceitável (Amarelo):** Consumo médio, monitorável. |
| 2 | CPU < 40%, RAM < 1200MB | **Insuficiente (Laranja):** Pode causar lentidão. |
| 1 | CPU ≥ 40% ou RAM ≥ 1200MB | **Crítico (Vermelho):** Compromete a estabilidade do sistema. |

#### M2.1.2 - Taxa de Conflito com Extensões de Navegador
| Nível | Pontuação | Critério de Julgamento |
| :--- | :--- | :--- |
| 5 | 0% de conflito | **Excelente (Verde):** Nenhum problema de compatibilidade. |
| 4 | 1–5% | **Bom (Verde):** Conflitos raros e isolados. |
| 3 | 6–10% | **Aceitável (Amarelo):** Conflitos ocasionais sem perda de funcionalidade. |
| 2 | 11–20% | **Insuficiente (Laranja):** Conflitos frequentes. |
| 1 | > 20% | **Crítico (Vermelho):** Conflitos graves impedem o uso normal. |

#### M2.1.3 - Tempo Médio de Recuperação após Travamento
| Nível | Pontuação | Critério de Julgamento |
| :--- | :--- | :--- |
| 5 | ≤ 2s | **Excelente (Verde):** Recuperação imediata. |
| 4 | 3–5s | **Bom (Verde):** Rápida retomada de operação. |
| 3 | 6–10s | **Aceitável (Amarelo):** Recuperação perceptível. |
| 2 | 11–20s | **Insuficiente (Laranja):** Lentidão na retomada. |
| 1 | > 20s | **Crítico (Vermelho):** Sistema exige reinício manual. |

---

## 5. Histórico de Versões

| Versão | Descrição | Autor | Data | Revisor |
| :---: | :--- | :--- | :---: | :---: |
| 1.0 | Criação do documento | [Bruno Cruz](https://github.com/brunocrzz), [Gabriel Mendes](https://github.com/gbevi), [João Moreira](https://github.com/joaofmoreiraa), [Maria Eduarda Pereira](https://github.com/maaduh), [Mayara Marques](https://github.com/maymarquee), [Pedro Túlio](https://github.com/PedrooCamilo) | 14/10/2025 | Todos |
| 1.1 | Adição da introdução e GQM's | Mesmo autores | 14/10/2025 | Todos |
| 1.2 | Adição dos Níveis de Pontuação e Critérios para Julgamento | Mesmo autores | 14/10/2025 | Todos |
| 1.3 | Ajuste de erro de escrita | [Bruno Cruz](https://github.com/brunocrzz) | 15/10/2025 | - |
| 1.4 | Adiciona objetivos | [Mayara Marques](https://github.com/maymarquee) | 23/10/2025 | [Gabriel Mendes](https://github.com/gbevi) |
| 1.5 | Inclusão de novas métricas e detalhamento dos critérios | [Gabriel Mendes](https://github.com/gbevi) | 24/10/2025 | Todos |
| 1.6 | Refinamento das questões após PC2 | [Maria Eduarda Pereira](https://github.com/maaduh) | 24/10/2025 | [Mayara Marques](https://github.com/maymarquee) |
