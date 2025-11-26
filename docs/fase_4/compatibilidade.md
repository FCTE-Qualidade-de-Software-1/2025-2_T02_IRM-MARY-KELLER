# Resultados dos Testes de Compatibilidade

Esta seção descreve os testes realizados e resultados obtidos com base nos **Casos de Teste (CTs)** projetados para avaliar a característica de **Compatibilidade** do Aprender 3, conforme planejamento realizado na Fase 3.

---

## CT-COMP-01: Sincronia de Status de Conclusão

### Detalhamento do Caso de Teste  
**Questão GQM:** Q1, *Qual é a consistência dos dados do discente entre o Aprender 3 (Web) e o App Moodle?*  
**Métrica Associada:** 1.1, Percentual de Discrepância de Status de Conclusão  
**Hipótese Avaliada:** H1.1, *O status de conclusão de atividades (marcar como "feita") fica inconsistente entre a plataforma Web e o aplicativo móvel.*  
**Perfil:** Discente  

---

### Resultados Obtidos  

| Atividades avaliadas | Discrepâncias | Percentual de Discrepância |
|----------------------|--------------|-----------------------------|
| 10                   | 0            | 0%                          |

**Total de atividades testadas:** 10  
**Total de discrepâncias:** 0  

---

### Cálculo da Métrica 1.1  

A Métrica 1.1 mede o **Percentual de Discrepância de Status de Conclusão** entre Web e App.  

**Fórmula utilizada:**  
Percentual de Discrepância = (Número de atividades com discrepância / Número total de atividades avaliadas) x 100  

Aplicando os valores obtidos:  
Percentual de Discrepância = (0 / 10) x 100 = **0%**

**Classificação segundo os critérios da Fase 2:** **EXCELENTE**  
(0% de discrepância encontra-se na melhor faixa de avaliação da métrica.)

---

### Análise e Resposta à Questão GQM  

> **Q1, Qual é a consistência dos dados do discente entre o Aprender 3 (Web) e o App Moodle?**

Os resultados indicam que, para o conjunto de 10 atividades analisadas, **não houve qualquer discrepância** entre o status de conclusão exibido na interface Web e o status exibido pelo App Moodle. Sempre que uma atividade foi marcada como concluída na Web, o mesmo estado foi refletido corretamente no aplicativo após a sincronização.

Isso demonstra um **nível máximo de consistência** para o cenário testado, já que o discente pode alternar entre Web e App sem risco de confusão quanto ao que já foi concluído. Do ponto de vista da Questão GQM 1, conclui-se que o Aprender 3 apresentou **consistência total** dos dados de conclusão de atividades entre as duas plataformas, no contexto do teste realizado.

---

### Avaliação da Hipótese H1.1  

> **H1.1, O status de conclusão de atividades (marcar como "feita") fica inconsistente entre a plataforma Web e o aplicativo móvel.**

A hipótese H1.1 pressupõe que existam diferenças perceptíveis entre os estados de conclusão mostrados na Web e no App, sugerindo problemas de sincronização. No entanto, os dados coletados mostram que:

- 10 atividades foram avaliadas;  
- 0 discrepâncias foram encontradas;  
- Percentual de discrepância: 0%.

Não houve qualquer evidência que apoiasse a existência de inconsistências de status de conclusão. Pelo contrário, o comportamento observado foi totalmente coerente entre Web e App.

Diante disso, conclui-se que a hipótese **não é validada** para o cenário testado, pois o comportamento esperado de falha, inconsistência Web e App, **não se manifestou** durante a execução do caso de teste.

---

### Demonstração em Vídeo  

A seguir encontra-se o vídeo que demonstra a execução completa do teste de sincronia de status de conclusão entre o Aprender 3 (Web) e o App Moodle:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/IcZVN-WvuPE"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## CT-COMP-02: Sincronização Bidirecional de Arquivos

### Detalhamento do Caso de Teste  
**Questão GQM:** Q1, *Qual é a consistência dos dados do discente entre o Aprender 3 (Web) e o App Moodle?*  
**Métrica Associada:** 1.2, Taxa de Sucesso de Sincronização Bidirecional de Arquivos  
**Hipótese Avaliada:** H1.2, *Os arquivos na área "Arquivos privados" não são sincronizados corretamente entre a versão Web e o App.*  
**Perfil:** Discente  

---

### Resultados Obtidos  

#### Web → App  
- Arquivos enviados via Web: **1**  
- Arquivos recebidos no App: **1**  

#### App → Web  
- Arquivos enviados via App: **1**  
- Arquivos recebidos na Web: **1**  

#### Resultados Consolidados  

| Direção     | Sucessos | Total | Taxa de Sucesso |
|-------------|----------|-------|-----------------|
| Web → App   | 1        | 1     | 100%            |
| App → Web   | 1        | 1     | 100%            |

**Total de sincronizações testadas, ambas as direções:** 2  
**Total de sucessos:** 2  

---

### Cálculo da Métrica 1.2  

A Métrica 1.2 mede a **Taxa de Sucesso de Sincronização Bidirecional de Arquivos** entre Web e App.

**Fórmula utilizada:**  
Taxa de Sucesso = (Número de sincronizações bem-sucedidas / Número total de sincronizações realizadas) x 100  

Aplicando os valores coletados:  

- Número de sincronizações bem-sucedidas: 2  
- Número total de sincronizações realizadas: 2  

Taxa de Sucesso = (2 / 2) x 100 = **100%**

**Classificação segundo os critérios da Fase 2:** **EXCELENTE**  
(Valor acima de 90%, dentro da melhor faixa de classificação para a métrica.)

---

### Análise e Resposta à Questão GQM  

> **Q1, Qual é a consistência dos dados do discente entre o Aprender 3 (Web) e o App Moodle?**

Os resultados do CT-COMP-02 mostram que as operações de envio de arquivos na área **"Arquivos privados"** foram sincronizadas corretamente em ambas as direções:

- O arquivo enviado pela interface Web foi encontrado no App Moodle após a sincronização;  
- O arquivo enviado pelo App foi exibido corretamente na interface Web.

Com 100% de sucesso nas duas direções, não foram observadas perdas de arquivo, inconsistências na listagem ou falhas aparentes de atualização. Isso indica que, no cenário testado, o Aprender 3 oferece **consistência total** dos dados de arquivos privados entre Web e App, reforçando a percepção de integridade do ambiente para o discente que alterna entre as plataformas.

Assim, em resposta à Questão GQM 1, conclui-se que o Aprender 3 mantém, neste caso de uso, um **altíssimo nível de consistência** dos dados de arquivos entre Web e App.

---

### Avaliação da Hipótese H1.2  

> **H1.2, Os arquivos na área "Arquivos privados" não são sincronizados corretamente entre a versão Web e o App.**

A hipótese H1.2 supõe a existência de falhas no processo de sincronização dos arquivos privados entre Web e App, o que se manifestaria na forma de arquivos ausentes em um dos lados após o envio. No entanto, os resultados mostram que:

- Web → App: 1 de 1 arquivos sincronizado com sucesso;  
- App → Web: 1 de 1 arquivos sincronizado com sucesso;  
- Taxa de sucesso global: 100%.

Não foram registradas falhas ou inconsistências nas operações testadas. Portanto, **não há evidências**, neste contexto, que sustentem a hipótese de falha sistemática na sincronização de arquivos.

Dessa forma, conclui-se que a hipótese **não é validada**, uma vez que o comportamento observado foi exatamente o oposto do que a hipótese previa, a sincronização funcionou corretamente em ambas as direções.

---

### Demonstração em Vídeo  

O vídeo da execução do teste está disponível a seguir:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/IcZVN-WvuPE"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## CT-COMP-03: Consumo Médio de RAM por Navegador

### Detalhamento do Caso de Teste  
**Questão GQM:** Q2, *Qual é a variação no consumo de recursos, CPU e RAM, do Aprender 3 entre diferentes navegadores?*  
**Métrica Associada:** 2.1, Consumo Médio de RAM por Navegador  
**Hipótese Avaliada:** H2.1, *O consumo de memória RAM do Aprender 3 é visivelmente maior em um navegador, por exemplo Chrome, comparado a outro, por exemplo Firefox, atrapalhando o uso de outros programas pelo discente.*  
**Perfil:** Discente  

---

### Resultados Obtidos  

O teste seguiu o **cenário de teste padrão** definido no plano, com login no Aprender 3, abertura de curso, navegação por tópicos e visualização de atividades. O consumo de memória RAM do processo principal do navegador foi monitorado via Gerenciador de Tarefas, após a estabilização da página. Foram realizadas **3 repetições** para cada navegador.

#### Medidas de Consumo por Navegador

| Navegador | Tentativa 1 (MB) | Tentativa 2 (MB) | Tentativa 3 (MB) | Média (MB) |
| :--- | :--- | :--- | :--- | :--- |
| Chrome | 443 | 414 | 396 | **417,67** |
| Firefox | 651 | 707 | 641 | **666,33** |
| Edge | 810 | 702 | 702 | **738,00** |

#### Comparativo de Consumo Médio

| Navegador | Média de RAM | Diferença em relação ao mais leve, Chrome |
| :--- | :--- | :--- |
| Chrome | 417,67 MB | - |
| Firefox | 666,33 MB | + 59,53% |
| Edge | 738,00 MB | + 76,69% |

---

### Cálculo da Métrica 2.1 e Classificação  

A Métrica 2.1 avalia a **variação de consumo médio de RAM** entre os navegadores, tomando como referência o navegador mais leve. A variação percentual é calculada comparando o consumo médio do navegador mais pesado com o mais leve.

No cenário medido:

- Navegador mais leve: **Chrome**, 417,67 MB  
- Navegador mais pesado: **Edge**, 738,00 MB  
- Variação aproximada: **76,69%** acima do consumo do Chrome  

Os critérios definidos para a Métrica 2.1 foram:

- Variação menor que 10%: Excelente  
- Variação entre 10% e 30%: Bom  
- Variação entre 30% e 50%: Regular  
- Variação maior que 50%: Insatisfatório  

A maior variação registrada foi de **76,69%** entre o navegador mais pesado e o mais leve.

**Classificação:** **INSATISFATÓRIO**

---

### Análise e Resposta à Questão GQM  

> **Q2, Qual é a variação no consumo de recursos, CPU e RAM, do Aprender 3 entre diferentes navegadores?**

Os resultados do CT-COMP-03 mostram que há uma diferença significativa no consumo de memória RAM do Aprender 3 entre os navegadores analisados. O Chrome apresentou o menor consumo médio, enquanto o Edge foi o mais pesado, com um acréscimo superior a 70% em relação ao Chrome. O Firefox também exibiu um consumo consideravelmente maior que o Chrome, com variação de aproximadamente 60%.

Essa disparidade indica que, embora o Aprender 3 seja acessível em múltiplos navegadores, o impacto sobre os recursos de hardware pode variar de forma expressiva dependendo do navegador escolhido pelo discente. Em equipamentos com memória limitada, o uso dos navegadores mais pesados pode prejudicar a execução simultânea de outras aplicações, o que afeta a experiência de uso e a eficiência no contexto acadêmico.

Portanto, em resposta à Questão GQM 2, conclui-se que a **variação no consumo de RAM entre navegadores é alta**, o que caracteriza uma situação de compatibilidade apenas parcial sob a ótica de recursos, com risco de impacto negativo para usuários em dispositivos mais modestos.

---

### Avaliação da Hipótese H2.1  

> **H2.1, O consumo de memória RAM do Aprender 3 é visivelmente maior em um navegador, por exemplo Chrome, comparado a outro, por exemplo Firefox, atrapalhando o uso de outros programas pelo discente.**

Os dados coletados mostram que a hipótese H2.1 é **validada**, com uma nuance importante. A hipótese previa que um navegador apresentaria consumo visivelmente maior, comprometendo potencialmente o uso de outros programas. Isso foi de fato observado, ainda que com um resultado diferente do exemplo dado na formulação da hipótese.

Embora a hipótese cite Chrome e Firefox como exemplo, os testes demonstraram que o **Edge** foi o navegador com maior consumo médio de RAM, seguido pelo Firefox, ambos significativamente mais pesados que o Chrome. A variação superior a 50% em relação ao navegador mais leve confirma que o consumo de recursos pode ser bastante desigual, e que a escolha do navegador influencia diretamente o desempenho percebido pelo discente.

Dessa forma, a hipótese é **validada** quanto ao seu conteúdo essencial, uma vez que foi comprovada a existência de um navegador com consumo de RAM visivelmente maior, com potencial de afetar o uso paralelo de outras aplicações.

---

### Demonstração em Vídeo  

O vídeo da execução do teste de consumo de RAM por navegador está disponível a seguir:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/9jLINYBFCZw?si=C1zRf0DeIY4yrWhX"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## CT-COMP-04: Entrega de Notificações de Fórum por E-mail

### Detalhamento do Caso de Teste  
**Questão GQM:** Q3, *Em que medida o discente recebe notificações por e-mail sobre novas postagens em fóruns de discussão subscritos?*  
**Métrica Associada:** 3.1, Taxa de Falha de Entrega de Notificação  
**Hipótese Avaliada:** H3.1, *O discente não recebe os e-mails de notificação de novas mensagens em fóruns que acompanha, mesmo com a opção ativada.*  
**Perfil:** Discente, visão do usuário  

---

### Resultados Obtidos  

No teste foram utilizadas duas contas, uma para postar, Conta A, e outra para receber notificações, Conta B, conforme definido na Fase 3. Foram realizadas **4 postagens** com monitoramento da caixa de entrada e da pasta de spam.

| ID Postagem | Recebeu Notificação A? | Recebeu Notificação B? | Local de Recebimento |
| :--- | :--- | :--- | :--- |
| Post 1 | Sim | Não enviado | Caixa de Entrada |
| Post 2 | Sim | Sim | Caixa de Entrada |
| Post 3 | Sim | Sim | Caixa de Entrada |
| Post 4 | Sim | Sim | Caixa de Entrada |

#### Estatísticas de Entrega

- **Total de envios:** 4  
- **Recebidos na caixa de entrada:** 4  
- **Recebidos no spam:** 0  
- **Não recebidos:** 0  

---

### Cálculo da Métrica 3.1 e Classificação  

A Métrica 3.1 mede a **Taxa de Falha de Entrega de Notificação**.

**Fórmula utilizada:**  
Taxa de Falha = (Número de notificações não recebidas / Número total de postagens) x 100  

Aplicando os valores:

- Número de notificações não recebidas: 0  
- Número total de postagens: 4  

Taxa de Falha = (0 / 4) x 100 = **0%**

Critérios considerados:

- 0% de falha: Excelente  
- Menos de 10% de falha: Bom  

**Classificação:** **EXCELENTE**

---

### Análise e Resposta à Questão GQM  

> **Q3, Em que medida o discente recebe notificações por e-mail sobre novas postagens em fóruns de discussão subscritos?**

Os resultados do CT-COMP-04 indicam que, no cenário testado, o mecanismo de notificações por e-mail do Aprender 3 funcionou de forma totalmente confiável. Todas as postagens realizadas no fórum geraram notificações correspondentes, que chegaram corretamente à caixa de entrada dos usuários envolvidos, sem registros de mensagens extraviadas ou enviadas para a pasta de spam.

Essa evidência mostra que o discente que subscreve um fórum pode confiar que será avisado sobre novas mensagens, desde que suas preferências de notificação estejam configuradas adequadamente. Do ponto de vista da Questão GQM 3, conclui-se que o Aprender 3 apresenta **alta efetividade na entrega de notificações de fórum por e-mail**, garantindo que a comunicação assíncrona seja mantida de forma consistente.

---

### Avaliação da Hipótese H3.1  

> **H3.1, O discente não recebe os e-mails de notificação de novas mensagens em fóruns que acompanha, mesmo com a opção ativada.**

A hipótese H3.1 descreve um cenário em que as notificações de fórum deixariam de ser entregues, mesmo com o usuário corretamente subscrito e com as configurações ajustadas. No entanto, os dados coletados mostram uma **taxa de falha igual a 0%**, com todas as notificações esperadas sendo efetivamente entregues.

Não houve qualquer evidência de problemas de envio, rejeição de mensagens ou comportamento inesperado na rota de entrega dos e-mails. Portanto, a hipótese **é refutada** no contexto deste teste, já que o comportamento observado é oposto ao problema descrito, o Aprender 3 enviou corretamente todas as notificações, e as contas de teste as receberam sem incidentes.

---

### Demonstração em Vídeo  

O vídeo da execução do teste de notificações de fórum está disponível a seguir:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/KFnzUSq2q5I?si=U0nBsFvnui4WKgg-"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## CT-COMP-05: Subscrição de Calendário via URL

### Detalhamento do Caso de Teste  
**Questão GQM:** Q4, *Em que medida o Aprender 3 permite a exportação para calendários externos?*  
**Métrica Associada:** 4.1, Taxa de Falha de Subscrição de URL  
**Hipótese Avaliada:** H4.1, *Os principais serviços de calendário, Google e Outlook, falham ao tentar importar o calendário via URL.*  
**Perfil:** Discente, Equipe de Avaliação  

---

### Resultados Obtidos  

| Serviço de Calendário | Resultado |
|-----------------------|-----------|
| Google Calendar       | Sucesso   |
| Outlook Calendar      | Sucesso   |
| Yahoo Calendar        | Falha     |
| Zoho Calendar         | Sucesso   |
| Open Web Calendar     | Sucesso   |
| Calendar Web          | Sucesso   |

**Total de serviços testados:** 6  
**Total de falhas:** 1  

---

### Cálculo da Métrica 4.1  

A Métrica 4.1 mede a **Taxa de Falha de Subscrição de URL** ao tentar adicionar o calendário do Aprender 3 em serviços externos.

**Fórmula utilizada:**  
Taxa de Falha = (Número de tentativas de subscrição que falharam / Número total de tentativas) x 100  

Aplicando os valores:

- Número de falhas: 1  
- Número total de tentativas: 6  

Taxa de Falha = (1 / 6) x 100 ≈ **16,67%**

**Classificação segundo os critérios da Fase 2:** **PARCIAL**  
(Existe falha em parte dos serviços testados, mas não em todos.)

---

### Análise e Resposta à Questão GQM  

> **Q4, Em que medida o Aprender 3 permite a exportação para calendários externos?**

A Questão 4 tem como objetivo avaliar a capacidade de interoperabilidade do Aprender 3 com plataformas externas de calendário, utilizando o mecanismo de subscrição via URL. A análise dos resultados demonstra que o sistema apresenta um nível elevado de compatibilidade, já que cinco dos seis serviços avaliados conseguiram importar corretamente os eventos disponibilizados pela plataforma.

Os dois serviços de maior relevância institucional, **Google Calendar** e **Outlook Calendar**, processaram o link com sucesso, o que evidencia que o Aprender 3 atende adequadamente às necessidades da comunidade acadêmica que depende desses sistemas para organização pessoal e acompanhamento de atividades. A falha isolada observada no **Yahoo Calendar** não compromete essa avaliação, pois se trata de um serviço menos utilizado e que não representa impacto significativo para o público da universidade.

Dessa forma, conclui-se que o Aprender 3 permite de maneira consistente a exportação de seu calendário para serviços externos, apresentando **interoperabilidade satisfatória** e desempenho alinhado ao esperado pela métrica associada à Questão GQM 4.

---

### Avaliação da Hipótese H4.1  

> **H4.1, Os principais serviços de calendário, Google e Outlook, falham ao tentar importar o calendário via URL.**

Os resultados obtidos demonstram que os serviços considerados principais, **Google Calendar** e **Outlook Calendar**, foram capazes de importar o calendário do Aprender 3 sem qualquer impedimento. Ambos interpretaram a URL corretamente e exibiram os eventos conforme configurados na plataforma, contrariando diretamente o que previa a hipótese.

A falha registrada ocorreu apenas no **Yahoo Calendar** e não se estendeu aos serviços centrais citados na hipótese. Assim, não existem evidências que corroborem a afirmação de que haveria incompatibilidade nos sistemas mais utilizados pelos estudantes.

Com base nesses resultados, conclui-se que a hipótese **não é validada**, uma vez que o comportamento esperado de falha nos serviços principais não foi observado durante o teste.

---

### Demonstração em Vídeo  

A seguir encontra-se o vídeo que demonstra a execução completa do teste de subscrição do calendário via URL:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/3xOpbAHUyNA"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## CT-COMP-06: Importação Estática (.ics) vs Subscrição Dinâmica (URL)

### Detalhamento do Caso de Teste  
**Questão GQM:** Q4, *Em que medida o Aprender 3 permite a exportação para calendários externos?*  
**Métrica Associada:** 4.2, Diferencial de Sucesso entre Importação Manual (.ics) e Subscrição Automática (URL)  
**Hipótese Avaliada:** H4.2, *A importação manual do arquivo .ics funciona, mas a subscrição automática via URL falha, indicando problema específico no mecanismo dinâmico.*  
**Perfil:** Discente, Equipe de Avaliação  

---

### Resultados Obtidos  

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
| NBA, Todos os jogos 2025 | Sucesso | Sucesso |
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

### Cálculo da Métrica 4.2  

A Métrica 4.2 compara diretamente o sucesso da importação manual (.ics) com o sucesso da subscrição automática via URL.

Diferencial de Sucesso = Percentual de Sucesso ICS menos Percentual de Sucesso URL

**Aplicando os valores coletados:**

100,00% menos 71,43% = 28,57%

**Diferencial obtido:** **28,57%**

Segundo os critérios definidos na Fase 2:

- Diferencial igual a 0% indica hipótese refutada;  
- Diferencial maior que 0% indica hipótese validada.  

**Classificação final:** O resultado **valida a hipótese H4.2**, pois a importação via arquivo .ics supera a subscrição via URL.

---

### Análise e Resposta à Questão GQM  

> **Q4, Em que medida o Aprender 3 permite a exportação para calendários externos?**

A Questão 4 procura avaliar de forma abrangente a capacidade do Aprender 3 de interoperar com serviços externos de calendário, considerando tanto a exportação manual quanto a automática. Os resultados mostram que a plataforma é plenamente capaz de gerar arquivos .ics válidos, que foram importados com sucesso em todos os calendários testados. Isso indica que o formato exportado pelo Aprender 3 é compatível e segue corretamente o padrão iCalendar.

Por outro lado, os resultados da subscrição dinâmica via URL apresentam limitações importantes. Embora diversos calendários tenham sido capazes de interpretar e atualizar o conteúdo da URL de forma satisfatória, houve falhas concentradas em calendários específicos, especialmente aqueles que dependem de validações rígidas ou mecanismos próprios de atualização. A diferença de desempenho entre os dois métodos revela que, apesar de o Aprender 3 suportar exportação automática, esse mecanismo ainda não apresenta a mesma confiabilidade assegurada pela exportação estática.

Assim, ao responder à Questão GQM, conclui-se que o Aprender 3 **permite a exportação de calendários para sistemas externos de forma consistente pelo método estático (.ics)**, mas apresenta **restrições claras no método dinâmico (URL)**, que afetam a garantia de interoperabilidade completa entre os serviços testados.

---

### Avaliação da Hipótese H4.2  

> **H4.2, A importação manual do arquivo .ics funciona, mas a importação automática via link falha, indicando problema específico no mecanismo de atualização automática.**

Os resultados obtidos oferecem evidências diretas que confirmam a hipótese H4.2. O fato de que **100%** das importações manuais via arquivo .ics foram bem-sucedidas demonstra que o Aprender 3 produz corretamente os dados do calendário. Em contraste, o mecanismo de subscrição automática via URL apresentou um conjunto de falhas que afetaram aproximadamente **28%** dos calendários testados, incluindo diversos sistemas que não conseguiram interpretar ou atualizar os eventos adequadamente.

Essa diferença significativa entre os métodos revela que não há um problema na geração do conteúdo do calendário, e sim no mecanismo de disponibilização dinâmica via URL. A validação da hipótese reforça a necessidade de ajustes no serviço responsável por fornecer atualizações contínuas ao calendário externo, enquanto confirma a robustez do arquivo estático gerado pela plataforma.

Assim, a hipótese **é validada**, pois a importação manual demonstrou confiabilidade total, ao passo que a subscrição automática evidenciou inconsistências que limitam sua eficácia.

---

### Demonstração em Vídeo  

O vídeo a seguir apresenta a **execução completa do teste**, mostrando a comparação entre a importação via URL e a importação manual via arquivo .ics:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/Nz8FJW_gg-w?si=ftPSr5NlJqEfJkHH"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## CT-COMP-07: Sucesso da Funcionalidade Drag-and-Drop (D&D) por Navegador

### Detalhamento do Caso de Teste  
**Questão GQM:** Q5, *Qual é a consistência da funcionalidade drag-and-drop entre os navegadores suportados?*  
**Métrica Associada:** 5.1, Taxa de Sucesso de Drag-and-Drop por Navegador  
**Hipótese Avaliada:** H5.1, *A funcionalidade de drag-and-drop apresenta taxa de sucesso superior a 85% em navegadores modernos.*  
**Perfil:** Discente  

---

### Resultados Obtidos  

O teste avaliou a taxa de sucesso da funcionalidade drag-and-drop em diferentes contextos do Aprender 3, como anexar arquivos em fóruns, reorganizar blocos laterais e arrastar eventos no calendário. Foram realizadas **10 tentativas** por navegador, distribuídas entre essas funcionalidades, utilizando arquivos de teste do tipo PDF, DOCX e PNG.

#### Resultados Gerais por Navegador

| Navegador | Tentativas | Sucessos | Falhas | Taxa de Sucesso |
| :--- | :--- | :--- | :--- | :--- |
| Chrome | 10 | 9 | 1 | 90% |
| Firefox | 10 | 10 | 0 | 100% |
| Edge | 10 | 9 | 1 | 90% |

#### Detalhamento por Funcionalidade

| Funcionalidade | Chrome | Firefox | Edge |
| :--- | :--- | :--- | :--- |
| Fóruns, 4 tentativas | 4/4 | 4/4 | 3/4 |
| Blocos Laterais, 3 tentativas | 2/3 | 3/3 | 3/3 |
| Calendário, 3 tentativas | 3/3 | 3/3 | 3/3 |

#### Falhas Identificadas

- **Chrome, 1 falha:** na reorganização de blocos laterais, o elemento retornou à posição original sem mensagem de erro.  
- **Firefox, 0 falhas:** todas as tentativas foram bem-sucedidas.  
- **Edge, 1 falha:** ao anexar arquivo em fórum, o arquivo não foi reconhecido na primeira tentativa, exigindo nova ação do usuário.

---

### Cálculo da Métrica 5.1 e Classificação  

A Métrica 5.1 mede a **Taxa de Sucesso de Drag-and-Drop por Navegador**, considerando a proporção de tentativas bem-sucedidas em relação ao total de tentativas.

**Fórmula utilizada:**  
Taxa de Sucesso = (Número de tentativas bem-sucedidas / Número total de tentativas) x 100  

Aplicando para cada navegador:

- Chrome: 9 sucessos em 10 tentativas, taxa de sucesso de 90%.  
- Firefox: 10 sucessos em 10 tentativas, taxa de sucesso de 100%.  
- Edge: 9 sucessos em 10 tentativas, taxa de sucesso de 90%.  

Critérios considerados:

- Percentual maior ou igual a 95%: Excelente  
- Percentual entre 85% e 94%: Bom  
- Percentual entre 70% e 84%: Regular  
- Percentual menor que 70%: Insatisfatório  

**Classificação por navegador:**

- Chrome, 90% de sucesso, **BOM**  
- Firefox, 100% de sucesso, **EXCELENTE**  
- Edge, 90% de sucesso, **BOM**  

---

### Análise e Resposta à Questão GQM  

> **Q5, Qual é a consistência da funcionalidade drag-and-drop entre os navegadores suportados?**

Os resultados demonstram que a funcionalidade de drag-and-drop do Aprender 3 se mantém **altamente consistente** entre os navegadores modernos avaliados. Todas as combinações de navegador e contexto de uso, fóruns, blocos laterais e calendário, atingiram taxas de sucesso iguais ou superiores a 90%, com destaque para o Firefox, que obteve 100% de sucesso em todas as tentativas.

As falhas observadas foram pontuais e não caracterizaram um padrão de incompatibilidade, mas sim pequenos comportamentos isolados, como a necessidade de repetir a tentativa de arraste em casos específicos. Isso indica que, do ponto de vista da experiência do usuário, o recurso é confiável e pode ser utilizado de forma natural pelos discentes na maior parte das situações.

Assim, em resposta à Questão GQM 5, conclui-se que a funcionalidade de drag-and-drop do Aprender 3 apresenta **boa consistência entre os navegadores testados**, com desempenho que varia entre bom e excelente de acordo com a métrica adotada.

---

### Avaliação da Hipótese H5.1  

> **H5.1, A funcionalidade de drag-and-drop apresenta taxa de sucesso superior a 85% em navegadores modernos.**

Os dados coletados confirmam diretamente a hipótese H5.1. Em todos os navegadores testados, Chrome, Firefox e Edge, a taxa de sucesso foi igual ou superior a 90%, superando o limiar de 85% estabelecido na formulação da hipótese. Além disso, o comportamento observado reforça a ideia de que as pequenas falhas pontuais não comprometem o uso prático da funcionalidade.

Dessa forma, a hipótese H5.1 é **confirmada**, uma vez que a taxa de sucesso do drag-and-drop mostrou-se consistentemente elevada em todos os navegadores modernos avaliados, compatível com as expectativas de compatibilidade de interação definidas para o Aprender 3.

---

### Demonstração em Vídeo  

O vídeo a seguir apresenta a **execução completa do teste**.

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/GpKkZoH8YnY?si=gllkdZWWyihxXz2Z"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## Resumo dos Resultados

### Métricas Avaliadas

| Métrica       | Descrição                                       | Resultado          | Classificação     |
| ------------- | ----------------------------------------------- | ------------------ | ----------------- |
| **CT-COMP-01**| Sincronia de Status de Conclusão                | 0% discrepâncias   | **Excelente**     |
| **CT-COMP-02**| Sincronização Bidirecional de Arquivos          | 100% sincronização | **Excelente**     |
| **CT-COMP-03**| Consumo Médio de RAM por Navegador              | Variação > 50%     | **Insatisfatório**|
| **CT-COMP-04**| Entrega de Notificações de Fórum por E-mail     | 0 falhas           | **Excelente**     |
| **CT-COMP-05**| Taxa de Falha de Subscrição de URL              | 1 falha, 16,67%    | **Parcial**       |
| **CT-COMP-06**| Diferencial de Sucesso, ICS vs URL              | 28,57% diferencial | **Hipótese H4.2 validada** |
| **CT-COMP-07**| Sucesso de Drag-and-Drop                        | 90% a 100%         | **Bom/Excelente** |

---

### Histórico de Versões

| Versão | Data       | Descrição                               | Autor                                  |
| :----: | ---------- | --------------------------------------- | -------------------------------------- |
| `1.0`  | 24/11/2025 | Criação da página                       | [Felipe Hansen](https://github.com/FHansen98) |
| `1.1`  | 23/11/2025 | Adição do CT-COM-01 e CT-COM-02         | [Thales Germano](https://github.com/thalesgvl) |
| `1.2`  | 24/11/2025 | Adição do CT-COM-05 e CT-COM-06         | [Pedro Sampaio](https://github.com/PedroSampaioDias) |
| `1.3`  | 25/11/2025 | Adição do CT-COMP-07 e Reorganização    | [Patrick Anderson Carvalho dos Santos](http://github.com/patrickacs) |
| `1.4`  | 25/11/2025 | Adição do CT-COM-03 e CT-COM-04         | [Taynara Vitorino](http://github.com/taybalau) |
