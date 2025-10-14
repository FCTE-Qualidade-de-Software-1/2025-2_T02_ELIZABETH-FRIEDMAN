# Fase 2 - Especificar a avaliação

## 1. Introdução

O objetivo da Fase 2: Especificar a Avaliação é detalhar, de forma objetiva, como as características de qualidade selecionadas **(Adequação Funcional e Compatibilidade)** serão medidas e julgadas.

Para garantir que a avaliação seja repetível, reprodutível e rastreável, esta fase será estruturada utilizando o Goal-Question-Metric (GQM) Framework. O GQM conecta os objetivos de alto nível (Goal) estabelecidos na Fase 1 às perguntas de avaliação (Question) e, por fim, às medidas concretas (Metric) que serão coletadas na Fase 4.


As métricas definidas a seguir, juntamente com seus níveis de pontuação e critérios de julgamento, servirão de insumo direto para a Fase 3.

## 2. Adequação Funcional

A Adequação Funcional refere-se à capacidade do LinkedIn de fornecer as funcionalidades necessárias para atender aos objetivos do usuário na sua jornada como candidato. Esta é uma característica de Prioridade Alta, pois é a base da proposta de valor da plataforma. As subcaracterísticas analisadas são: **Correção Funcional, Completude Funcional e Pertinência Funcional**.

### 2.1 GQM

<font size="3"><p style="text-align: center">Tabela 1: GQM - Adequação Funcional</p></font>

| Subcaracterística    | Objetivo (Goal)                                                                                                         | Questão (Question)                                                                                                                        | Métrica (Metric)                                                                                                                                               |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Correção Funcional   | **G1 (Geral):** Assegurar a eficácia das funcionalidades essenciais do LinkedIn para o sucesso profissional do usuário. | **Q1:** Os filtros de busca de vagas operam corretamente, garantindo que os resultados correspondam precisamente aos critérios aplicados? | **M1.1.1 - Taxa de Conformidade de Busca:** Proporção de resultados de vagas (em amostra de N=20) que estritamente obedecem aos filtros utilizados.            |
| Completude Funcional | **G1 (Geral):** Assegurar a eficácia das funcionalidades essenciais do LinkedIn para o sucesso profissional do usuário. | **Q2:** O formulário de candidatura simplificada ("Easy Apply") contém os campos essenciais para a conclusão do processo?                 | **M1.2.2 - Completude de Campos Críticos:** Porcentagem de campos críticos (ex: anexo de CV) presentes e funcionais no formulário de candidatura simplificada. |

### 2.2 Níveis de Pontuação e Critérios para Julgamento

A pontuação é baseada em uma escala de 1 (Crítico) a 5 (Excelente).

#### M1.1.1 - Taxa de Conformidade de Busca (Correção Funcional)

<font size="3"><p style="text-align: center">Tabela 2: Níveis e critérios de Julgamento da Métrica 1.1.1</p></font>

| Nível | Pontuação    | Descrição do Nível | Critério de Julgamento                                                                              |
| ----- | ------------ | ------------------ | --------------------------------------------------------------------------------------------------- |
| 5     | Excelente    | Taxa = 100%        | **Aceitável:** A funcionalidade é totalmente correta e atende plenamente ao objetivo                |
| 4     | Bom          | 95% ≤ Taxa < 100%  | **Aceitável:** Pequenas falhas que não comprometem o resultado                                      |
| 3     | Mediano      | 85% ≤ Taxa < 95%   | **Aceitável com Ressalvas:** Necessita de monitoramento/pequena correção                            |
| 2     | Insuficiente | 70% ≤ Taxa < 85%   | **Não-Conformidade Menor:** Afeta a confiabilidade dos resultados                                   |
| 1     | Crítico      | Taxa < 70%         | **Não-Conformidade Crítica:** A falha no filtro compromete a principal proposta de valor do produto |

#### M1.2.1 - Completude de Campos Críticos (Completude Funcional)

<font size="3"><p style="text-align: center">Tabela 3: Níveis e critérios de Julgamento da Métrica 1.2.1</p></font>

| Nível | Pontuação    | Descrição do Nível                  | Critério de Julgamento                                                                                                |
| ----- | ------------ | ----------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| 5     | Excelente    | 100% dos campos críticos presentes. | **Satisfatória:** O conjunto de funções é completo para a tarefa de candidatura                                       |
| 4     | Bom          | 90% ≤ Campos < 100%                 | **Satisfatória:** Pequena ausência de campos acessórios não-críticos                                                  |
| 3     | Mediano      | 80% ≤ Campos < 90%                  | **Aceitável com Ressalvas:** Ausência de campo importante, mas que não impede a conclusão                             |
| 2     | Insuficiente | 70% ≤ Campos < 80%                  | **Não-Conformidade Menor:** A ausência de um campo crítico gera retrabalho no usuário                                 |
| 1     | Crítico      | Campos < 70%                        | **Não-Conformidade Crítica:** A falta de campos essenciais (ex: Anexo de CV) impede a conclusão eficaz da candidatura |

## 3. Compatibilidade

A Compatibilidade refere-se à capacidade do produto de coexistir e trocar informações com outros sistemas, compartilhando o mesmo ambiente e recursos. Esta característica também é de Prioridade Alta porque conflitos de recursos ou problemas de integração prejudicam a experiência fluida e profissional. As subcaracterísticas analisadas são: **Coexistência e Interoperabilidade**.

### 3.1 GQM

<font size="3"><p style="text-align: center">Tabela 4: GQM - Compatibilidade</p></font>

| Subcaracterística | Objetivo (Goal)                                                                                      | Questão (Question)                                                                                                                               | Métrica (Metric)                                                                                                                                                                     |
| ----------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Coexistência      | **G2 (Geral):** Garantir que o LinkedIn funcione harmoniosamente no ambiente operacional do usuário. | **Q3:** O uso do LinkedIn em navegadores com extensões causa um consumo de CPU/Memória que gere impacto negativo no desempenho geral do sistema? | **M2.1.1 - Pico de Consumo de Recursos:** O pico máximo de consumo de CPU (%) e Memória (MB) do processo do navegador (Chrome/Firefox) durante a execução de um objeto de avaliação. |

### 3.2 Níveis de Pontuação e Critérios para Julgamento

A pontuação é baseada em uma escala de 1 (Crítico) a 5 (Excelente).

#### M2.1.1 - Pico de Consumo de Recursos 

<font size="3"><p style="text-align: center">Tabela 5: Níveis e critérios de Julgamento da Métrica 2.1.1</p></font>

| Nível | Pontuação    | Descrição do Nível            | Critério de Julgamento                                                                                   |
| ----- | ------------ | ----------------------------- | -------------------------------------------------------------------------------------------------------- |
| 5     | Excelente    | CPU < 10% e Memória < 500MB   | **Satisfatória:** O aplicativo coexiste de forma eficiente e sem conflitos                               |
| 4     | Bom          | CPU < 20% e Memória < 800MB   | **Satisfatória:** Consumo aceitável, sem impacto negativo percebido                                      |
| 3     | Mediano      | CPU < 30% e Memória < 1000MB  | **Aceitável com Ressalvas:** Alto, mas dentro da margem de tolerância                                    |
| 2     | Insuficiente | CPU < 40% ou Memória < 1200MB | **Não-Conformidade Menor:** O consumo pode afetar o desempenho de outras aplicações                      |
| 1     | Crítico      | CPU ≥ 40% ou Memória ≥ 1200MB | **Não-Conformidade Crítica:** Consumo excessivo que compromete a estabilidade do ambiente (Coexistência) |

## 8. Histórico de Versões 

<font size="3"><p style="text-align: center">Tabela 6: Histórico de versões</p></font>

| Versão |                         Descrição                          |                                                                                                                                             Autor                                                                                                                                             |    Data    | Revisor |
| :----: | :--------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------: | :-----: |
|  1.0   |                    Criação do documento                    | [Bruno Cruz](https://github.com/brunocrzz), [Gabriel Mendes](https://github.com/gbevi), [João Moreira](https://github.com/joaofmoreiraa), [Maria Eduarda Pereira](https://github.com/maaduh), [Mayara Marques](https://github.com/maymarquee), [Pedro Túlio](https://github.com/PedrooCamilo) | 14/10/2025 |  Todos  |
|  1.1   |                Adição da introdução e GQM's                | [Bruno Cruz](https://github.com/brunocrzz), [Gabriel Mendes](https://github.com/gbevi), [João Moreira](https://github.com/joaofmoreiraa), [Maria Eduarda Pereira](https://github.com/maaduh), [Mayara Marques](https://github.com/maymarquee), [Pedro Túlio](https://github.com/PedrooCamilo) | 14/10/2025 |  Todos  |
|  1.2   | Adição dos Níveis de Pontuação e Critérios para Julgamento | [Bruno Cruz](https://github.com/brunocrzz), [Gabriel Mendes](https://github.com/gbevi), [João Moreira](https://github.com/joaofmoreiraa), [Maria Eduarda Pereira](https://github.com/maaduh), [Mayara Marques](https://github.com/maymarquee), [Pedro Túlio](https://github.com/PedrooCamilo) | 14/10/2025 |  Todos  |