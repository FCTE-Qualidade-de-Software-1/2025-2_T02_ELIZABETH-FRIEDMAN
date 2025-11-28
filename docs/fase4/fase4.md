# Fase 4 - Executar a avaliação

## 4.x Adequação Funcional

### 1. Métrica M1.1.1 (Taxa de Conformidade de Busca) e M1.1.3 (Tempo de Resposta)

#### 1.1 Metodologia da Coleta

Conforme planejado na Fase 3, foram realizadas **10 execuções de busca** utilizando simultaneamente pelo menos três filtros (ex: Cargo + Localidade + Tipo de Vaga/Experiência).  
O objetivo foi estressar a ferramenta para validar a precisão dos resultados e a performance da API.

### Ferramentas utilizadas:

- **M1.1.1:** Inspeção visual dos resultados retornados (amostra de até 10 itens).
- **M1.1.3:** Chrome DevTools (Network Tab), filtrando pela requisição `voyagerJobsDashJobCards`.

### Tabela de Registros (Dados Brutos)

| Execução (#) | M1.1.3: Tempo (s) | M1.1.3: Tempo (ms) | M1.1.1: Aderência | % Conformidade | Observações |
|--------------|-------------------|---------------------|-------------------|----------------|-------------|
| 01 | 0,68 s | 680 ms | 10/10 | 100% | — |
| 02 | 0,74 s | 740 ms | 10/10 | 100% | — |
| 03 | 0,69 s | 690 ms | 10/10 | 100% | — |
| 04 | 0,78 s | 780 ms | 10/10 | 100% | Pico de tempo registrado. |
| 05 | 0,68 s | 680 ms | 10/10 | 100% | — |
| 06 | 0,55 s | 550 ms | 8/8 | 100% | Retornou apenas 8 resultados totais, todos corretos. |
| 07 | 0,75 s | 750 ms | 10/10 | 100% | — |
| 08 | 0,71 s | 710 ms | 10/10 | 100% | — |
| 09 | 0,61 s | 610 ms | 8/8 | 100% | Retornou apenas 8 resultados totais, todos corretos. |
| 10 | 0,59 s | 590 ms | 2/2 | 100% | Filtro restritivo: apenas 2 resultados, ambos corretos. |

### **RESULTADO**

- **Média (s):** 0,678 s  
- **Média (ms):** 678 ms  
- **Total de Aderência:** 88/88 — **100%**

---

### 1.2 Análise e Julgamento dos Resultados

#### A) Análise da M1.1.1 — Taxa de Conformidade de Busca

**Resultado Obtido:** 100% de conformidade.

**Critério de Julgamento (Tabela 5 da Fase 2):**  
O resultado se enquadra no **Nível 5 - Excelente (Verde)**, que exige 100% de acerto ("Nenhum resultado incorreto encontrado").

#### Validação da Hipótese H1.1

- **Hipótese:** A H1.1 previa que, ao aplicar três filtros, a taxa cairia para um Nível Insuficiente (< 84%), esperando resultados irrelevantes.
- **Conclusão:** A hipótese foi **REFUTADA POSITIVAMENTE**.  
  O sistema demonstrou alta precisão e, em filtros restritivos, preferiu retornar menos resultados do que apresentar itens incorretos.

---

#### B) Análise da M1.1.3 — Tempo Médio de Resposta

**Resultado Obtido:** 678 ms (0,67 s).

**Critério de Julgamento (Tabela 7 da Fase 2):**  
Classificação: **Nível 5 — Excelente (Verde)** (≤ 1 s).

#### Validação da Hipótese H1.2

- **Hipótese:** Esperava-se Nível Aceitável (2–4 s).
- **Conclusão:** A hipótese foi **REFUTADA POSITIVAMENTE**.  
  O tempo médio ficou abaixo de 700 ms e execuções com menos resultados foram mais rápidas, indicando otimização do payload.

---

### 1.3 Veredito Final (Correção Funcional — Busca)

Com base nas métricas **M1.1.1** e **M1.1.3**, a funcionalidade de **Busca do LinkedIn Web foi classificada como _EXCELENTE_.**

O sistema demonstrou ser capaz de lidar com consultas complexas mantendo:

- **Tempo sub-segundo (< 1 s)**
- **100% de precisão**
- **Controle inteligente de resultados** (não preencher com itens incorretos)

Mesmo com filtros restritivos, a ferramenta priorizou a qualidade dos dados e confirmou a robustez da API.

## M1.2.1 — Completude de Campos Críticos (Experiência)

* **Tipo de Medição:** Indireta (Checklist estruturado).  
* **Responsável pela Coleta:** Gabriel Mendes.  
* **Objetivo GQM:** Verificar se todos os campos essenciais da seção *Experiência* no LinkedIn Web estão presentes e funcionais.

#### Metodologia da Coleta

A coleta foi realizada conforme definido na Fase 3, utilizando **4 cenários específicos**:

- Chrome-01 (sessão normal)  
- Chrome-02 (modo anônimo)  
- Safari-01 (sessão normal)  
- Safari-02 (modo privado com restrições de cookies)

Para cada cenário, foi executado um checklist vertical contendo **8 campos críticos** definidos na Fase 2: Cargo, Tipo de vínculo, Nome da empresa, Localidade, Modalidade, Data de início, Data de término e Descrição.

Cada campo foi avaliado como:

- **S** — Presente e funcional  
- **N** — Ausente ou com comportamento inadequado

---

#### Resultados Brutos (Checklist)

| Campo                  | Chrome-01 | Chrome-02 | Safari-01 | Safari-02 |
|----------------------- |-----------|-----------|-----------|-----------|
| Cargo                  | S         | S         | S         | S         |
| Tipo de vínculo        | S         | S         | S         | S         |
| Nome da empresa        | S         | S         | S         | S         |
| Localidade             | S         | S         | S         | S         |
| Modalidade             | S         | S         | S         | S         |
| Data de início         | S         | S         | S         | S         |
| Data de término        | S         | S         | S         | S         |
| Descrição              | S         | S         | S         | S         |
| **Total de Campos**    | **8**     | **8**     | **8**     | **8**     |
| **% Completude**       | **100%**  | **100%**  | **100%**  | **100%**  |
| **Nível**              | **5**     | **5**     | **5**     | **5**     |

---

### Análise Final da Métrica M1.2.1

A métrica obteve **100% de completude** em todos os cenários, mantendo todos os campos essenciais disponíveis e funcionais.  
Isso resulta em:

> **Nível 5 — Excelente (Verde)**

#### Relação com a Hipótese H2.1 (Fase 2)

> *“A completude de campos críticos será de 100%.”*

**Resultado:**  
✔ *Hipótese Confirmada*

O LinkedIn demonstra consistência total no módulo de Experiência, sem falhas, omissões ou comportamentos inesperados.

### Evidências

Todas as evidências de vídeo e prints de execução estão disponíveis no link abaixo:

<div style="text-align: center;">
    <font size="3"><p>Planilha de Evidências — M1.2.2</p></font>
    <a href="https://unbbr-my.sharepoint.com/:x:/g/personal/222006605_aluno_unb_br/IQAeyXZ17yVpQpV9nSw38vuOAYoonlIwHQ9OnTSMqCuFL6M?e=0i6qSe" target="_blank"><b>Acesse aqui os vídeos e registros da execução</b></a>
</div>

---

---

### M1.2.2 — Cobertura de Funcionalidades Relevantes

* **Tipo de Medição:** Indireta (Checklist funcional).  
* **Responsável pela Coleta:** Gabriel Mendes.  
* **Objetivo GQM:** Avaliar se as funcionalidades essenciais da jornada do candidato estão presentes e plenamente funcionais no LinkedIn Web.

#### Metodologia da Coleta

A coleta utilizou 4 cenários distintos:

- Chrome-01 (normal)  
- Chrome-Ext-02 (extensões ativas)  
- Safari-01 (normal)  
- Safari-Priv-02 (privado)

Foram avaliadas 7 funcionalidades críticas:

1. Buscar vaga  
2. Aplicar candidatura  
3. Salvar vaga  
4. Criar alerta  
5. Usar filtros  
6. Ver detalhes da vaga  
7. Ver vagas salvas  

Cada funcionalidade foi marcada como:

- **S** — Funcional e disponível  
- **N** — Ausente ou com erro

---

#### Resultados Brutos (Checklist)

| Funcionalidade         | Chrome-01 | Chrome-Ext-02 | Safari-01 | Safari-Priv-02 |
|------------------------|-----------|----------------|-----------|-----------------|
| Buscar vaga            | S         | S              | S         | S               |
| Aplicar candidatura    | S         | S              | S         | S               |
| Salvar vaga            | S         | S              | S         | S               |
| Criar alerta           | S         | S              | S         | S               |
| Usar filtros           | S         | S              | S         | S               |
| Ver detalhes da vaga   | S         | S              | S         | S               |
| Ver vagas salvas       | S         | S              | S         | S               |
| **Total Funcionalidades** | **7** | **7**          | **7**     | **7**           |
| **% Cobertura**        | **100%**  | **100%**       | **100%**  | **100%**        |
| **Nível**              | **5**     | **5**          | **5**     | **5**           |

---

### Análise Final da Métrica M1.2.2

Todas as funcionalidades críticas da jornada do candidato foram encontradas e funcionando corretamente em **100% dos cenários avaliados**.

Resultado:

> **Nível 5 — Excelente (Verde)**

#### Relação com a Hipótese H2.2 (Fase 2)

> *“A Cobertura de Funcionalidades será ≥ 95% (Nível Excelente).”*

**Resultado:**  
✔ *Hipótese Confirmada*

O LinkedIn apresentou robustez funcional em todos os testes, mantendo toda a jornada do candidato acessível e estável.

### Evidências

Todas as evidências de vídeo e prints de execução estão disponíveis no link abaixo:

<div style="text-align: center;">
    <font size="3"><p>Planilha de Evidências — M1.2.2</p></font>
    <a href="https://unbbr-my.sharepoint.com/:x:/g/personal/222006605_aluno_unb_br/IQAeyXZ17yVpQpV9nSw38vuOAYoonlIwHQ9OnTSMqCuFL6M?e=0i6qSe" target="_blank"><b>Acesse aqui os vídeos e registros da execução</b></a>
</div>

---

---

## x. Compatibilidade

### M2.1.2 - Taxa de Conflito com Extensões de Navegador

* **Tipo de Medição:** Indireta (Calculada a partir de contagens).
* **Responsável pela Coleta:** Bruno Cruz.
* **Objetivo GQM:** Avaliar se o LinkedIn Web consegue coexistir sem impacto negativo com outras aplicações e extensões no ambiente do usuário.

#### Metodologia da Coleta

A coleta para esta métrica consistiu em 20 interações críticas, projetadas para forçar a injeção de scripts na interface do LinkedIn e medir a frequência de erros de script ou falhas de renderização.

**Extensões e Versões Utilizadas**

Foram utilizadas duas extensões dentro do ambiente do Google Chrome (Versão mais recente), que injetam código intensamente, criando o cenário de maior risco de conflito:

| Extensão  | Versão    | Foco do teste                                                      |
| :-------- | :-------- | :----------------------------------------------------------------- |
| Grammarly | 14.1264.0 | Injeção de script em campos de texto (Interações 1-10).            |
| Waalaxy   | 1.3.227   | Injeção de widgets e botões na interface (DOM) (Interações 11-20). |


#### Resultados Brutos por Iteração

| Interação | Resultado (nº de conflitos) | Extensão Testada |
| :-------- | :-------------------------- | :--------------- |
| 1         | 1                           | Grammarly        |
| 2         | 1                           | Grammarly        |
| 3         | 0                           | Grammarly        |
| 4         | 0                           | Grammarly        |
| 5         | 0                           | Grammarly        |
| 6         | 0                           | Grammarly        |
| 7         | 0                           | Grammarly        |
| 8         | 0                           | Grammarly        |
| 9         | 0                           | Grammarly        |
| 10        | 0                           | Grammarly        |
| 11        | 1                           | Waalaxy          |
| 12        | 1                           | Waalaxy          |
| 13        | 1                           | Waalaxy          |
| 14        | 2                           | Waalaxy          |
| 15        | 2                           | Waalaxy          |
| 16        | 2                           | Waalaxy          |
| 17        | 1                           | Waalaxy          |
| 18        | 1                           | Waalaxy          |
| 19        | 1                           | Waalaxy          |
| 20        | 1                           | Waalaxy          |

##### Mapeamento de Falha vs. Conflito

| Causa Raiz                        | Mapeamento no Console                           | Atribuição | Contagem Total                                              |
| :-------------------------------- | :---------------------------------------------- | :--------- | :---------------------------------------------------------- |
| Falha de Extração                 | ERROR INJECTIONS - extractMemberIdFromProfile   | Grammarly  | 2 ocorrências (interações 1 e 2)                            |
| Falha de Carregamento             | GET chrome-extension://invalid/ net::ERR_FAILED | Waalaxy    | 10 ocorrências (em todos os testes)                         |
| Falha Funcional                   | Ocorreu um erro durante a ligação ao servidor   | Waalaxy    | 3 ocorrências (Associadas ao erro de GET, interações 14-16) |
| Total de Ocorrências Registradas: |                                                 |            | 15                                                          |

##### Evidências

<div style="text-align: center;">
    <font size="3"><p>Figura 1: Erro de Falha de Extração</p></font>
    <img src="../coleta/evidencias/M.2.1.2erro1.png" alt="Falha de Extr
