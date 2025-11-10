# Fase 3 - Projetar a avaliação

## 1. Introdução

O objetivo da **Fase 3: Projetar a Avaliação** é detalhar, de forma objetiva, como as características de qualidade selecionadas (**Adequação Funcional** e **Compatibilidade**) serão medidas e julgadas.

Este Plano de Avaliação é o documento formal que traduz as especificações da Fase 2 (métricas e critérios) em um roteiro prático para a execução. Ele define o método, os recursos e o cronograma necessários para garantir que a avaliação do aplicativo web LinkedIn seja rastreável, repetível e reprodutível, seguindo o Processo de Avaliação de Produto de Software (ISO/IEC 25040).

---

## 2. Metodologia de Avaliação

O método de avaliação a ser utilizado é a **Execução de Roteiros de Testes (Test Scenarios)**, complementado por **Inspeção e Monitoramento de Recursos de Sistema**. O plano deve conter, explicar e definir esse método para que o avaliador possa executar a avaliação completamente

O processo é fundamentado nos seguintes pilares metodológicos:

* **Modelo de Qualidade:** ISO/IEC 25010 (SQuaRE) para a taxonomia das características (Adequação Funcional e Compatibilidade).
* **Estrutura de Medição:** Framework **Goal-Question-Metric (GQM)**, conectando os objetivos da avaliação às métricas específicas.

### 2.1 Visão Geral do Método

O método consiste em três etapas principais de coleta de dados:

1.  **Testes Funcionais e Comportamentais (Black-Box):** Execução de tarefas críticas (busca, candidatura, edição) para obter dados de taxa de erro e conformidade.
2.  **Medição de Desempenho (Tempo):** Uso de ferramentas de cronometragem para medir a latência do sistema.
3.  **Monitoramento de Coexistência (Sistema):** Uso de ferramentas de monitoramento do Sistema Operacional para medir o impacto do software no ambiente.

### 2.2 Tabela de Métricas (Índice de Medição)

| Característica          | Subcaracterística    | Métrica                                           | Tipo de Medição                |
| :---------------------- | :------------------- | :------------------------------------------------ | :----------------------------- |
| **Adequação Funcional** | Correção Funcional   | M1.1.1 Taxa de Conformidade de Busca              | Porcentagem                    |
|                         | Correção Funcional   | M1.1.2 Taxa de Erro de Candidatura                | Porcentagem                    |
|                         | Correção Funcional   | M1.1.3 Tempo Médio de Resposta da Busca           | Tempo (s)                      |
|                         | Completude Funcional | M1.2.1 Completude de Campos Críticos              | Porcentagem                    |
|                         | Completude Funcional | M1.2.2 Cobertura de Funcionalidades Relevantes    | Porcentagem                    |
|                         | Completude Funcional | M1.2.3 Disponibilidade de Recursos Complementares | Porcentagem                    |
| **Compatibilidade**     | Coexistência         | M2.1.1 Pico de Consumo de Recursos                | Valor Absoluto (CPU %, RAM MB) |
|                         | Coexistência         | M2.1.2 Taxa de Conflito com Extensões             | Porcentagem                    |
|                         | Coexistência         | M2.1.3 Tempo Médio de Recuperação                 | Tempo (s)                      |

---

## 3. Instruções de Execução do Método

O método será executado por meio de instruções padronizadas, que detalham como o avaliador deve obter cada medida.

### 3.1 Execução da Adequação Funcional

A coleta para as métricas de Adequação Funcional exige interações diretas do usuário:

* **Para M1.1.1 (Conformidade de Busca) e M1.1.3 (Tempo de Resposta):** O avaliador deve realizar **10 execuções de busca**, sempre aplicando **três filtros** simultaneamente (ex: cargo, localidade, experiência). Para M1.1.1, será feita a inspeção dos 10 primeiros resultados para verificar a aderência aos filtros. Para M1.1.3, o tempo de carregamento será medido com ferramentas de DevTools.
* **Para M1.1.2 (Taxa de Erro de Candidatura):** O avaliador tentará concluir o fluxo "candidatura simplificada" em **20 vagas** diferentes, registrando quantas falhas irrecuperáveis ocorrem.
* **Para M1.2.1 (Completude de Campos) e M1.2.2 (Cobertura de Funcionalidades):** Estas são métricas de inspeção; o avaliador fará uma lista de verificação (checklist) dos campos essenciais no módulo "Experiência" e das funcionalidades esperadas (buscar, candidatar, salvar), calculando a porcentagem de itens presentes.
* **Para M1.2.3 (Disponibilidade):** A funcionalidade "Salvar Vaga" será monitorada passivamente durante um período prolongado de uso, registrando-se qualquer intermitência ou erro de indisponibilidade.

### 3.2 Execução da Compatibilidade

A coleta para as métricas de Compatibilidade envolve o uso de ferramentas de monitoramento do ambiente:

* **Para M2.1.1 (Consumo de Recursos):** O avaliador abrirá o LinkedIn em dois navegadores (Chrome e Firefox) com extensões ativas. O Gerenciador de Tarefas do Sistema Operacional será usado para registrar o pico de consumo de CPU e RAM alocados ao processo do navegador durante **15 minutos** de navegação intensa (entre vagas e perfis).
* **Para M2.1.2 (Conflito com Extensões):** O avaliador executará 10 interações críticas (onde o código da extensão e do LinkedIn interagem, como preenchimento de formulários) com as extensões ativas para contar a ocorrência de erros de script ou falhas de renderização.
* **Para M2.1.3 (Tempo de Recuperação):** O avaliador induzirá um travamento (por sobrecarga ou falha simulada) e cronometrará o tempo até que a página seja restaurada, ou o tempo necessário para o usuário realizar a recuperação manual (F5). A média de **5 repetições** será utilizada.

---

## 4. Especificação dos Recursos

Os seguintes recursos são necessários para a execução completa e controlada do Plano de Avaliação:

### 4.1 Recursos Humanos

| Membro                   | Responsabilidades                                            |
| :----------------------- | :----------------------------------------------------------- |
| **Avaliadores (Equipe)** | Execução dos roteiros de testes, coleta e registro de dados. |

### 4.2 Materiais de Apoio e Ferramentas Técnicas

| Recurso                          | Função na Avaliação                                               |
| :------------------------------- | :---------------------------------------------------------------- |
| **Software Objeto de Avaliação** | Aplicação web do LinkedIn (versão desktop).                       |
| **Navegadores**                  | Google Chrome e Mozilla Firefox (ambientes de teste).             |
| **Ferramentas de Sistema**       | Gerenciador de Tarefas do S.O. (Medição de CPU/RAM).              |
| **Ferramentas de Software**      | Ferramentas do Desenvolvedor (DevTools).                          |
| **Recurso de Teste**             | Extensões ativas e passivas (Criação de cenário de coexistência). |
| **Registro**                     | Planilha Eletrônica (Excel) para coleta de dados.                 |
| **Documentação**                 | Cretérios de Avaliação Fase 2.                                    |

---

## 5. Histórico de Versões

| Versão | Descrição            | Autor                                                                                                                                                                                                                                                                                         |    Data    | Revisor |
| :----: | :------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------: | :-----: |
|  1.0   | Criação do documento | [Bruno Cruz](https://github.com/brunocrzz), [Gabriel Mendes](https://github.com/gbevi), [João Moreira](https://github.com/joaofmoreiraa), [Maria Eduarda Pereira](https://github.com/maaduh), [Mayara Marques](https://github.com/maymarquee), [Pedro Túlio](https://github.com/PedrooCamilo) | 08/11/2025 |  Todos  |
|  1.1   | Documentação         | [Bruno Cruz](https://github.com/brunocrzz), [Gabriel Mendes](https://github.com/gbevi), [João Moreira](https://github.com/joaofmoreiraa), [Maria Eduarda Pereira](https://github.com/maaduh), [Mayara Marques](https://github.com/maymarquee), [Pedro Túlio](https://github.com/PedrooCamilo) | 10/11/2025 |  Todos  |
