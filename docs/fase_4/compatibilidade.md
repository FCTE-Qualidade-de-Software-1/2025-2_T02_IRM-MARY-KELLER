# Resultados dos Testes de Compatibilidade

Esta seção descreve os testes realizados e resultados obtidos com base nos **Casos de Teste (CTs)** projetados para avaliar a característica de **Compatibilidade** do Aprender 3, conforme planejamento realizado na Fase 3.

---
# CT-COMP-01: Sincronia de Status de Conclusão

## Detalhamento do Caso de Teste  
**Questão GQM:** Q1, *Qual é a consistência dos dados do discente entre o Aprender 3 (Web) e o App Moodle?*  
**Métrica Associada:** 1.1, Percentual de Discrepância de Status de Conclusão  
**Hipótese Avaliada:** H1.1, *O status de conclusão de atividades (marcar como "feita") fica inconsistente entre a plataforma Web e o aplicativo móvel.*  
**Perfil:** Discente  

---

## Resultados Obtidos  

| Atividades avaliadas | Discrepâncias | Percentual de Discrepância |
|----------------------|--------------|-----------------------------|
| 10                   | 0            | 0%                          |

**Total de atividades testadas:** 10  
**Total de discrepâncias:** 0  

### Cálculo da Métrica 1.1  
**Percentual de Discrepância** = (Nº de atividades com discrepância / Nº total de atividades avaliadas) x 100  

Aplicando os valores obtidos:  
**Percentual de Discrepância** = (0 / 10) x 100 = **0%**

**Classificação segundo os critérios da Fase 2:** **EXCELENTE**  
(0% de discrepância encontra-se na melhor faixa de avaliação da métrica.)

---

## Análise e Resposta à Questão GQM  

> **Q1, Qual é a consistência dos dados do discente entre o Aprender 3 (Web) e o App Moodle?**

Os resultados indicam que, para o conjunto de 10 atividades analisadas, **não houve qualquer discrepância** entre o status de conclusão exibido na interface Web e o status exibido pelo App Moodle. Sempre que uma atividade foi marcada como concluída na Web, o mesmo estado foi refletido corretamente no aplicativo após a sincronização.

Isso demonstra um **nível máximo de consistência** para o cenário testado, já que o discente pode alternar entre Web e App sem risco de confusão quanto ao que já foi concluído. Do ponto de vista da Questão GQM 1, conclui-se que o Aprender 3 apresentou **consistência total** dos dados de conclusão de atividades entre as duas plataformas, no contexto do teste realizado.

---

## Avaliação da Hipótese H1.1  

> **H1.1, O status de conclusão de atividades (marcar como "feita") fica inconsistente entre a plataforma Web e o aplicativo móvel.**

A hipótese H1.1 pressupõe que existam diferenças perceptíveis entre os estados de conclusão mostrados na Web e no App, sugerindo problemas de sincronização. No entanto, os dados coletados mostram que:

- 10 atividades foram avaliadas;  
- 0 discrepâncias foram encontradas;  
- Percentual de discrepância: 0%.

Não houve qualquer evidência que apoiasse a existência de inconsistências de status de conclusão. Pelo contrário, o comportamento observado foi totalmente coerente entre Web e App.

Diante disso, conclui-se que a hipótese **não é validada** para o cenário testado, pois o comportamento esperado de falha (inconsistência Web × App) **não se manifestou** durante a execução do caso de teste.

---

## Demonstração em Vídeo  

A seguir encontra-se o vídeo que demonstra a execução completa do teste de sincronia de status de conclusão entre o Aprender 3 (Web) e o App Moodle:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/IcZVN-WvuPE"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

# CT-COMP-02: Sincronização Bidirecional de Arquivos

## Detalhamento do Caso de Teste  
**Questão GQM:** Q1, *Qual é a consistência dos dados do discente entre o Aprender 3 (Web) e o App Moodle?*  
**Métrica Associada:** 1.2, Taxa de Sucesso de Sincronização Bidirecional de Arquivos  
**Hipótese Avaliada:** H1.2, *Os arquivos na área "Arquivos privados" não são sincronizados corretamente entre a versão Web e o App.*  
**Perfil:** Discente  

---

## Resultados Obtidos  

### Web → App  
- Arquivos enviados via Web: **1**  
- Arquivos recebidos no App: **1**  

### App → Web  
- Arquivos enviados via App: **1**  
- Arquivos recebidos na Web: **1**  

### Resultados Consolidados  

| Direção     | Sucessos | Total | Taxa de Sucesso |
|-------------|----------|-------|-----------------|
| Web → App   | 1        | 1     | 100%            |
| App → Web   | 1        | 1     | 100%            |

**Total de sincronizações testadas (ambas as direções):** 2  
**Total de sucessos:** 2  

---

## Cálculo da Métrica 1.2  

A Métrica 1.2 mede a **Taxa de Sucesso de Sincronização Bidirecional de Arquivos** entre Web e App (Web → App e App → Web).

**Taxa de Sucesso** = (Nº de sincronizações bem-sucedidas / Nº total de sincronizações realizadas) x 100  

Aplicando os valores coletados:  

- Nº de sincronizações bem-sucedidas: 2  
- Nº total de sincronizações realizadas: 2  

**Taxa de Sucesso** = (2 / 2) x 100 = **100%**

**Classificação segundo os critérios da Fase 2:** **EXCELENTE**  
(Valor acima de 90%, dentro da melhor faixa de classificação para a métrica.)

---

## Análise e Resposta à Questão GQM  

> **Q1, Qual é a consistência dos dados do discente entre o Aprender 3 (Web) e o App Moodle?**

Os resultados do CT-COMP-02 mostram que as operações de envio de arquivos na área **"Arquivos privados"** foram sincronizadas corretamente em ambas as direções:

- O arquivo enviado pela interface Web foi encontrado no App Moodle após a sincronização;  
- O arquivo enviado pelo App foi exibido corretamente na interface Web.

Com 100% de sucesso nas duas direções, não foram observadas perdas de arquivo, inconsistências na listagem ou falhas aparentes de atualização. Isso indica que, no cenário testado, o Aprender 3 oferece **consistência total** dos dados de arquivos privados entre Web e App, reforçando a percepção de integridade do ambiente para o discente que alterna entre as plataformas.

Assim, em resposta à Questão GQM 1, conclui-se que o Aprender 3 mantém, neste caso de uso, um **altíssimo nível de consistência** dos dados de arquivos entre Web e App.

---

## Avaliação da Hipótese H1.2  

> **H1.2, Os arquivos na área "Arquivos privados" não são sincronizados corretamente entre a versão Web e o App.**

A hipótese H1.2 supõe a existência de falhas no processo de sincronização dos arquivos privados entre Web e App, o que se manifestaria na forma de arquivos ausentes em um dos lados após o envio. No entanto, os resultados mostram que:

- Web → App: 1 de 1 arquivos sincronizado com sucesso;  
- App → Web: 1 de 1 arquivos sincronizado com sucesso;  
- Taxa de sucesso global: 100%.

Não foram registradas falhas ou inconsistências nas operações testadas. Portanto, **não há evidências**, neste contexto, que sustentem a hipótese de falha sistemática na sincronização de arquivos.

Dessa forma, conclui-se que a hipótese **não é validada**, uma vez que o comportamento observado foi exatamente o oposto do que a hipótese previa: a sincronização funcionou corretamente em ambas as direções.

---

# CT-COMP-03: Consumo Médio de RAM por Navegador

## Informações do Teste
- **Questão GQM:** Q2 – Recursos do Navegador
- **Métrica:** 2.1 – Consumo Médio de RAM por Navegador
- **Hipótese:** H2.1 – O consumo de memória RAM do Aprender 3 é visivelmente maior em um navegador (ex: Chrome) comparado a outro (ex: Firefox), atrapalhando o uso de outros programas pelo discente
- **Perfil:** Discente

## Execução
O teste seguiu o **cenário de teste padrão** definido no plano. O consumo de memória (RAM) do processo principal foi monitorado via Gerenciador de Tarefas após a estabilização da página. Foram realizadas **3 repetições** para cada navegador.

## Resultados

| Navegador | Tentativa 1 (MB) | Tentativa 2 (MB) | Tentativa 3 (MB) | Média (MB) |
| :--- | :--- | :--- | :--- | :--- |
| Chrome | 443 | 414 | 396 | **417.67** |
| Firefox | 651 | 707 | 641 | **666.33** |
| Edge | 810 | 702 | 702 | **738.00** |

### Comparativo de Consumo

| Navegador | Média de RAM | Diferença vs Mais Leve (Chrome) |
| :--- | :--- | :--- |
| Chrome | 417.67 MB | - |
| Firefox | 666.33 MB | + 59.53% |
| Edge | 738.00 MB | + 76.69% |

## Classificação da Métrica 2.1

Critérios (Definidos na Fase 2):
- Variação < 10%: Excelente
- Variação 10% - 30%: Bom
- Variação 30% - 50%: Regular
- Variação > 50%: Insatisfatório

**Resultado Final:**
A maior variação registrada foi de **76.69%** (Edge em relação ao Chrome).

**Classificação:** **INSATISFATÓRIO**

## Validação da Hipótese

**H2.1: VALIDADA**

A hipótese foi confirmada. O navegador Microsoft Edge apresentou um consumo de memória significativamente superior (+76%) ao navegador de referência (Chrome) no mesmo cenário de uso. Essa discrepância elevada valida a preocupação de que a escolha do navegador pode impactar o desempenho do dispositivo do discente, especialmente em hardwares com recursos limitados.

O video da execução do teste está disponível a seguir:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/watch?v=9jLINYBFCZw"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

# CT-COMP-04: Entrega de Notificações de Fórum por E-mail

## Informações do Teste
- **Questão GQM:** Q3 – Notificações de Fórum
- **Métrica:** 3.1 – Taxa de Falha de Entrega de Notificação
- **Hipótese:** H3.1 – Discente não recebe e-mails de novas mensagens em fóruns subscritos
- **Perfil:** Discente (Visão do Usuário)

## Execução
Foram realizadas 4 respostas distintas no fórum para conta A e 3 respostas distintas para conta B. A caixa de entrada e a pasta de Spam da Conta A e B foram monitoradas.

## Resultados

| ID Postagem | Recebeu Notificação A? | Recebeu Notificação B? |Local de Recebimento |
| :--- | :--- | :--- | :--- | 
| Post 1 | Sim | Não enviado | Caixa de Entrada | 
| Post 2 | Sim | Sim | Caixa de Entrada | 
| Post 3 | Sim | Sim | Caixa de Entrada | 
| Post 4 | Sim | Sim | Caixa de Entrada | 



### Estatísticas de Entrega
- **Total de Envios:** 4
- **Recebidos na Entrada:** 4
- **Recebidos no Spam:** 0
- **Não Recebidos:** 0

## Cálculo da Métrica 3.1 e Classificação

**Fórmula:**
Taxa de Falha = (Nº de Não Recebidos / Total de Postagens) x 100
Taxa de Falha = (0 / 4) x 100 = **0%**

Critérios:
- 0% Falha: Excelente
- < 10% Falha: Bom

**Classificação:** **EXCELENTE**

## Validação da Hipótese

**H3.1: REFUTADA**

O sistema entregou 100% das notificações geradas. O usuário recebeu os e-mails correspondentes a todas as mensagens.

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://youtu.be/KFnzUSq2q5I"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>---

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


---

# CT-COMP-07: Sucesso da Funcionalidade Drag-and-Drop (D&D) por Navegador

## Informações do Teste
- **Métrica:** 5.1 - Compatibilidade de Drag-and-Drop
- **Objetivo:** Avaliar a taxa de sucesso da funcionalidade drag-and-drop em diferentes navegadores.
- **Hipótese:** H5.1: A funcionalidade de drag-and-drop apresenta taxa de sucesso superior a 85% em navegadores modernos.

## Ambiente de Teste
- **Funcionalidades Testadas:** Fóruns (anexo de arquivos), Blocos laterais (reorganização), Calendário (arrastar eventos).
- **Método:** 10 tentativas totais por navegador (distribuídas entre as funcionalidades).
- **Arquivos teste:** PDF (2.5MB), DOCX (1.8MB), PNG (3.2MB).

## Resultados dos Testes

| Navegador | Tentativas | Sucessos | Falhas | Taxa de Sucesso |
| :--- | :--- | :--- | :--- | :--- |
| Chrome | 10 | 9 | 1 | 90% |
| Firefox | 10 | 10 | 0 | 100% |
| Edge | 10 | 9 | 1 | 90% |

### Detalhamento por Funcionalidade

| Funcionalidade | Chrome | Firefox | Edge |
| :--- | :--- | :--- | :--- |
| Fóruns (4 tentativas) | 4/4 | 4/4 | 3/4 |
| Blocos Laterais (3 tentativas) | 2/3 | 3/3 | 3/3 |
| Calendário (3 tentativas) | 3/3 | 3/3 | 3/3 |

### Falhas Identificadas
- **Chrome (1 falha):** Blocos Laterais: Elemento não posicionou corretamente, retornou à posição original sem mensagem de erro.
- **Firefox (0 falhas):** Nenhuma falha registrada.
- **Edge (1 falha):** Fóruns: Arquivo não foi reconhecido imediatamente na área de drop, necessitou segunda tentativa.

## Classificação da Métrica 5.1

Critérios (ISO/IEC 25010):
- ≥ 95%: Excelente
- 85-94%: Bom
- 70-84%: Regular
- < 70%: Insatisfatório

**Resultados:**
- Chrome: 90% - **BOM**
- Firefox: 100% - **EXCELENTE**
- Edge: 90% - **BOM**

## Validação da Hipótese

**H5.1: CONFIRMADA**

Todos os navegadores apresentaram taxa de sucesso igual ou superior a 85%, com desempenho satisfatório. As falhas identificadas foram pontuais e não caracterizam problemas sistemáticos de compatibilidade.

---

## Resumo dos Resultados

### Métricas Avaliadas

| Métrica       | Descrição                                       | Resultado          | Classificação |
| ------------- | ----------------------------------------------- | ------------------ | ------------- |
| **CT-COMP-01**| Sincronia de Status de Conclusão                | 0% discrepâncias   | **Excelente** |
| **CT-COMP-02**| Sincronização Bidirecional de Arquivos          | 100% sincronização | **Excelente** |
| **CT-COMP-03**| Consumo Médio de RAM por Navegador              | Variação > 50%     | **Insatisfatório** |
| **CT-COMP-04**| Entrega de Notificações de Fórum por E-mail     | 0 falhas           | **Excelente** |
| **CT-COMP-05**| Taxa de Falha de Subscrição de URL              | 1 falha (Yahoo)    | **Parcial**   |
| **CT-COMP-06**| Diferencial de Sucesso (ICS vs URL)             | 28,57% dif.        | **Validada (H4.2)** |
| **CT-COMP-07**| Sucesso de Drag-and-Drop                        | > 90% sucesso      | **Bom/Excelente** |

---

## Histórico de Versões

| Versão | Data       | Descrição                               | Autor                                  |
| :----: | ---------- | --------------------------------------- | -------------------------------------- |
| `1.0`  | 24/11/2025 | Criação da página | [Felipe Hansen](https://github.com/FHansen98) |
| `1.1`  | 23/11/2025 | Adição do CT-COM-01 e CT-COM-02 | [Thales Germano](https://github.com/thalesgvl) |
| `1.2`  | 24/11/2025 | Adição do CT-COM-05 e CT-COM-06 | [Pedro Sampaio](https://github.com/PedroSampaioDias) |
| `1.3`  | 25/11/2025 | Adição do CT-COMP-07 e Reorganização | [Patrick Anderson Carvalho dos Santos](http://github.com/patrickacs) |
| `1.4`  | 25/11/2025 | Adição do CT-COM-03 e CT-COM-04 | [Taynara Vitorino](http://github.com/taybalau) |

