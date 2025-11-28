# Fase 4 - Executar a avaliação

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

A tabela a seguir registra o número de conflitos observados a cada uma das 20 interações críticas:

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
    <img src="../coleta/evidencias/M.2.1.2erro1.png" alt="Falha de Extração">
    <font size="3"><p>Figura 2: Erro de Falha de Carregamento</p></font>
    <img src="../coleta/evidencias/M.2.1.2erro2.png" alt="Falha de Carregamento">
    <font size="3"><p>Figura 3: Erro de Falha Funcional</p></font>
    <img src="../coleta/evidencias/M.2.1.2erro3.png" alt="Falha Funcional">
    <font size="3"><p>Vídeo</p></font>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/Jh_vf3EznfI?si=iMG6O19ahkt1iKCf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

### Análise Final

O número total de ocorrências de falha registradas foi de 15. Aplicando a Tabela de Julgamento da Métrica realizada na Fase 2:

| Contagem Registrada | Nível de Julgamento (Fase 2) | Conclusão              |
| :------------------ | :--------------------------- | :--------------------- |
| 15 Conflitos        | 11–20 conflitos              | Insuficiente (Laranja) |

* A coexistência do LinkedIn com extensões é classificada como Insuficiente (Laranja). Embora o site seja possível de ser usado (o navegador não travou completamente), a frequência de 15 ocorrências de falha em 20 interações é muito alta, confirmando a instabilidade crítica do ambiente diante dessas extensões.
* A Aplicação interfere negativamente, pois as falhas de script das extensões (Grammarly) e os erros de carregamento (Waalaxy) consumiram recursos e resultaram em falha funcional visível ao usuário final.
* A **Hipótese 3.2 (H3.2)** previa que a métrica M2.1.2 apresentaria um Nível Insuficiente (> 11%) de conflitos com extensões ativas que interagem com o DOM.
    * **Resultado:** O teste confirmou a H3.2. As extensões ativas (Grammarly e Waalaxy), que injetam scripts e widgets no DOM do LinkedIn, geraram 15 ocorrências de falha, classificando o resultado no Nível Insuficiente (Laranja).
    * **Implicação:** O resultado valida a premissa de que a arquitetura do LinkedIn apresenta fragilidade de coexistência com scripts injetados, causando erros de parsing e falhas de requisição de recursos.
* Apesar de o site ainda ser utilizável, a interferência é frequente e negativa. Em **75%** das interações de teste, nos deparamos com falhas visíveis ou erros no console, exigindo que ele ignore ou reinicie a tarefa. Isso se deve aos 3 Defeitos (Causas Raízes) Únicos que se manifestaram 15 vezes. 