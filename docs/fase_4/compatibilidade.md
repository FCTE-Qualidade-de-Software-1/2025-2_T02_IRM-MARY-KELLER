# Resultados dos Testes de Compatibilidade

Esta seção descreve os testes realizados e resultados obtidos com base nos **Casos de Teste (CTs)** projetados para avaliar a característica de **Compatibilidade** do Aprender 3, conforme planejamento realizado na Fase 3.

---

# CT-COMP-01: Sincronia de Status de Conclusão

## Informações do Teste
- **Questão GQM:** Q1 – Sincronia de Dados  
- **Métrica:** 1.1 – Percentual de Discrepância  
- **Hipótese:** H1.1 – Possível inconsistência Web × App  
- **Perfil:** Discente  

## Ambiente
- **Web:** Aprender 3 (Linux Ubuntu 24.04)  
- **App:** Moodle 5.0.0 – S24 (Android 16)  
- **Conexão:** Dados móveis (emulado)

## Execução
Foram avaliadas **atividades** com rastreamento de conclusão.  
Passos: marcar na Web → sincronizar App → comparar status.

## Resultados

| Atividades | Discrepâncias | Percentual |
|------------|---------------|------------|
| 10         | 0             | **0%**     |

### Fórmula

Discrepância = (0 / 10) × 100 = 0%


### Classificação (Métrica 1.1)
**EXCELENTE** (0% a 5%)

---

# CT-COMP-02: Sincronização Bidirecional de Arquivos

## Informações do Teste
- **Questão GQM:** Q1 – Sincronia de Dados  
- **Métrica:** 1.2 – Taxa de Sucesso de Sincronização  
- **Hipótese:** H1.2 – Possíveis falhas na sincronização Web ↔ App  
- **Perfil:** Discente  

## Ambiente
- Mesmo do CT-COMP-01  
- Arquivos: PDF, MD

## Execução

### Web → App
- **1 arquivo enviados via Web**
- Resultado: **1/1 sincronizados**

### App → Web
- **1 arquivo enviados via App**
- Resultado: **1/1 sincronizados**

## Resultados Consolidados

| Direção     | Sucesso | Total | Taxa  |
|-------------|---------|-------|-------|
| Web → App   | 1       | 1     | 100%  |
| App → Web   | 1       | 1     | 100%  |

### Fórmula

Taxa de Sucesso = (2/2) × 100 = 100%


### Classificação (Métrica 1.2)
**EXCELENTE** (> 90%)


O video da execução do teste está disponível a seguir:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/IcZVN-WvuPE"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>


## Resumo dos Resultados

### Métricas Avaliadas

| Métrica       | Descrição                                       | Resultado          | Classificação |
| ------------- | ----------------------------------------------- | ------------------ | ------------- |
| **CT-COMP-01**| Sincronia de Status de Conclusão                | 0% discrepâncias   | **Excelente** |
| **CT-COMP-02**| Sincronização Bidirecional de Arquivos          | 100% sincronização | **Excelente** |

---

# CT-COMP-05: Subscrição de Calendário via URL

## Detalhamento do Caso de Teste  
**Questão GQM:** Q4, *Em que medida o Aprender 3 permite a exportação para calendários externos?*  
**Métrica Associada:** 4.1, Taxa de Falha de Subscrição de URL  
**Hipótese Avaliada:** H4.1, *Os principais serviços de calendário (Google, Outlook) falham ao tentar importar o calendário via URL.*  
**Perfil:** Discente, Equipe de Avaliação  

---

## Resultados Obtidos  

| Serviço de Calendário | Resultado |
|----------------------|-----------|
| Google Calendar      | Sucesso   |
| Outlook Calendar     | Sucesso   |
| Yahoo Calendar       | Falha     |
| Zoho Calendar        | Sucesso   |
| Open Web Calendar    | Sucesso   |
| Calendar Web         | Sucesso   |

**Total de serviços testados:** 6  
**Total de falhas:** 1  

### Cálculo da Métrica 4.1  
**Taxa de Falha** = (Nº de tentativas de subscrição que falharam / Nº total de tentativas) x 100

**Classificação segundo os critérios da Fase 2:** **PARCIAL**  
(Existe falha em parte dos serviços testados, mas não em todos.)

---

## Análise e Resposta à Questão GQM  

> **Q4, Em que medida o Aprender 3 permite a exportação para calendários externos?**

A Questão 4 tem como objetivo avaliar a capacidade de interoperabilidade do Aprender 3 com plataformas externas de calendário, utilizando o mecanismo de subscrição via URL. A análise dos resultados demonstra que o sistema apresenta um nível elevado de compatibilidade, já que cinco dos seis serviços avaliados conseguiram importar corretamente os eventos disponibilizados pela plataforma.  

Os dois serviços de maior relevância institucional, Google Calendar e Outlook Calendar, processaram o link com sucesso, o que evidencia que o Aprender 3 atende adequadamente às necessidades da comunidade acadêmica que depende desses sistemas para organização pessoal e acompanhamento de atividades. A falha isolada observada no Yahoo Calendar não compromete essa avaliação, pois se trata de um serviço menos utilizado e que não representa impacto significativo para o público da universidade.  

Dessa forma, conclui-se que o Aprender 3 permite de maneira consistente a exportação de seu calendário para serviços externos, apresentando interoperabilidade satisfatória e desempenho alinhado ao esperado pela métrica associada à Questão GQM 4.

---

## Avaliação da Hipótese H4.1  

> **H4.1, Os principais serviços de calendário, Google e Outlook, falham ao tentar importar o calendário via URL.**

Os resultados obtidos demonstram que os serviços considerados principais, Google Calendar e Outlook Calendar, foram capazes de importar o calendário do Aprender 3 sem qualquer impedimento. Ambos interpretaram a URL corretamente e exibiram os eventos conforme configurados na plataforma, contrariando diretamente o que previa a hipótese.  

A falha registrada ocorreu apenas no Yahoo Calendar e não se estendeu aos serviços centrais citados na hipótese. Assim, não existem evidências que corroborem a afirmação de que haveria incompatibilidade nos sistemas mais utilizados pelos estudantes.  

Com base nesses resultados, conclui-se que a hipótese **não é validada**, uma vez que o comportamento esperado de falha nos serviços principais não foi observado durante o teste.

---

## Demonstração em Vídeo  
A seguir encontra-se o vídeo que demonstra a execução completa do teste de subscrição do calendário via URL:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/3xOpbAHUyNA"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

# CT-COMP-06: Importação Estática (.ics) vs Subscrição Dinâmica (URL)

## Detalhamento do Caso de Teste  
**Questão GQM:** Q4, *Em que medida o Aprender 3 permite a exportação para calendários externos?*  
**Métrica Associada:** 4.2, Diferencial de Sucesso entre Importação Manual (.ics) e Subscrição Automática (URL)  
**Hipótese Avaliada:** H4.2, *A importação manual do arquivo .ics funciona, mas a subscrição automática via URL falha, indicando problema específico no mecanismo dinâmico.*  
**Perfil:** Discente, Equipe de Avaliação  

---

## Resultados Obtidos  

| Nome do Calendário | Resultado URL | Resultado ICS |
|--------------------|--------------|----------------|
| Atlanta Hawks | Falha | Sucesso |
| Boston Celtics | Falha | Sucesso |
| Chicago Bulls | Falha | Sucesso |
| Dallas Mavericks | Falha | Sucesso |
| Golden State Warriors | Falha | Sucesso |
| Los Angeles Lakers | Falha | Sucesso |
| Miami Heat | Falha | Sucesso |
| New York Knicks | Falha | Sucesso |
| Orlando Magic | Falha | Sucesso |
| San Antonio Spurs | Falha | Sucesso |
| NBA (Todos os jogos 2025) | Sucesso | Sucesso |
| UFC | Sucesso | Sucesso |
| Campeonato Brasiliense | Sucesso | Sucesso |
| Fases da Lua | Sucesso | Sucesso |
| Chuvas de Meteoros | Sucesso | Sucesso |
| Eventos Relacionados a Planetas | Sucesso | Sucesso |
| Lançamento de Foguetes | Sucesso | Sucesso |
| Eventos Históricos | Sucesso | Sucesso |
| Curiosidades Históricas | Sucesso | Sucesso |
| Estreias de Filmes | Sucesso | Sucesso |
| Previsões de Fim do Mundo | Sucesso | Sucesso |
| Feriados Brasil | Sucesso | Sucesso |
| Feriados Angola | Sucesso | Sucesso |
| Feriados Benin | Sucesso | Sucesso |
| Feriados Cabo Verde | Sucesso | Sucesso |
| Feriados Honduras | Sucesso | Sucesso |
| Feriados Macau | Sucesso | Sucesso |
| Feriados Moçambique | Sucesso | Sucesso |
| Feriados Portugal | Sucesso | Sucesso |
| Feriados Colômbia | Sucesso | Sucesso |
| Feriados Cristãos | Sucesso | Sucesso |
| Feriados Hinduístas | Sucesso | Sucesso |
| Feriados Judaicos | Sucesso | Sucesso |
| Feriados Muçulmanos | Sucesso | Sucesso |
| Feriados Cristãos Ortodoxos | Sucesso | Sucesso |

**Taxa de Sucesso via URL:** 71,43%  
**Taxa de Sucesso via ICS:** 100,00%  

---

## Cálculo da Métrica 4.2  
A Métrica 4.2 compara diretamente o sucesso da importação manual (.ics) com o sucesso da subscrição automática (URL).

Diferencial de Sucesso = % Sucesso ICS - % Sucesso URL

**Aplicando os valores coletados:**

100% - 71,43% = 28,57%

**Diferencial obtido: 28,57%**

Segundo os critérios definidos na Fase 2:

- **Diferencial = 0%** → Hipótese refutada  
- **Diferencial > 0%** → Hipótese validada  

**Classificação final:** O resultado **valida a hipótese H4.2**, pois a importação via .ics supera a subscrição via URL.

---

## Análise e Resposta à Questão GQM  

> **Q4, Em que medida o Aprender 3 permite a exportação para calendários externos?**

A Questão 4 procura avaliar de forma abrangente a capacidade do Aprender 3 de interoperar com serviços externos de calendário, considerando tanto a exportação manual quanto a automática. Os resultados mostram que a plataforma é plenamente capaz de gerar arquivos .ics válidos, que foram importados com sucesso em todos os calendários testados. Isso indica que o formato exportado pelo Aprender 3 é compatível e segue corretamente o padrão iCalendar.

Por outro lado, os resultados da subscrição dinâmica via URL apresentam limitações importantes. Embora diversos calendários tenham sido capazes de interpretar e atualizar o conteúdo da URL de forma satisfatória, houve falhas concentradas em calendários específicos, especialmente aqueles que dependem de validações rígidas ou mecanismos próprios de atualização. A diferença de desempenho entre os dois métodos revela que, apesar de o Aprender 3 suportar exportação automática, este mecanismo ainda não apresenta a mesma confiabilidade assegurada pela exportação estática.

Assim, ao responder à Questão GQM, conclui-se que o Aprender 3 **permite a exportação de calendários para sistemas externos de forma consistente pelo método estático (.ics)**, mas apresenta **restrições claras no método dinâmico (URL)**, que afetam a garantia de interoperabilidade completa entre os serviços testados.

---

## Avaliação da Hipótese H4.2  

> **H4.2, A importação manual do arquivo .ics funciona, mas a importação automática via link falha, indicando problema específico no mecanismo de atualização automática.**

Os resultados obtidos oferecem evidências diretas que confirmam a hipótese H4.2. O fato de que **100%** das importações manuais via arquivo .ics foram bem-sucedidas demonstra que o Aprender 3 produz corretamente os dados do calendário. Em contraste, o mecanismo de subscrição automática via URL apresentou um conjunto de falhas que afetaram aproximadamente **28%** dos calendários testados, incluindo diversos sistemas que não conseguiram interpretar ou atualizar os eventos adequadamente.

Essa diferença significativa entre os métodos revela que não há um problema na geração do conteúdo do calendário, e sim no mecanismo de disponibilização dinâmica via URL. A validação da hipótese reforça a necessidade de ajustes no serviço responsável por fornecer atualizações contínuas ao calendário externo, enquanto confirma a robustez do arquivo estático gerado pela plataforma.

Assim, a hipótese **é validada**, pois a importação manual demonstrou confiabilidade total, ao passo que a subscrição automática evidenciou inconsistências que limitam sua eficácia.

---

## Demonstração em Vídeo  
O vídeo a seguir apresenta a **execução completa do teste**, mostrando a comparação entre a importação via URL e a importação manual via arquivo .ics:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://youtu.be/Nz8FJW_gg-w?si=T5MFM9ilrOiQgmVp"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>


## Histórico de Versões

| Versão | Data       | Descrição                               | Autor                                  |
| :----: | ---------- | --------------------------------------- | -------------------------------------- |
| `1.0`  | 24/11/2025 | Criação da página | [Felipe Hansen](https://github.com/FHansen98) |
| `1.1`  | 23/11/2025 | Adição do CT-COM-01 e CT-COM-02 | [Thales Germano](https://github.com/thalesgvl) |
| `1.2`  | 24/11/2025 | Adição do CT-COM-05 e CT-COM-06 | [Pedro Sampaio](https://github.com/PedroSampaioDias) |

