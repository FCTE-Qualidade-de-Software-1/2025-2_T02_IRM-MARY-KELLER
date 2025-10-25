## Objetivo de Medição 1: Compatibilidade

| Analisar | Descrição |
| :--- | :--- |
| **Para o propósito de** | Avaliar |
| **Com respeito a** | Compatibilidade |
| **Do ponto de vista da** | Comunidade discente |
| **No contexto da** | Operação em produção |

**Tabela 2** - Objetivo de Medição 1: Compatibilidade.

---

### Perguntas e Hipóteses de Medição

**Questão 1 (Sincronia de Dados):**
> Qual é a consistência dos dados do discente entre o Aprender 3 (Web) e o App Moodle?

* **Hipótese 1.1 (H1.1):** O status de conclusão de atividades (marcar como "feita") fica inconsistente entre a plataforma Web e o aplicativo móvel.
* **Hipótese 1.2 (H1.2):** Os arquivos na área "Arquivos privados" não são sincronizados corretamente entre a versão Web e o App.

**Questão 2 (Recursos do Navegador):**
> Qual é a variação no consumo de recursos (CPU/RAM) do Aprender 3 entre diferentes navegadores?

* **Hipótese 2.1 (H2.1):** O consumo de memória RAM do Aprender 3 é visivelmente maior em um navegador (ex: Chrome) comparado a outro (ex: Firefox), atrapalhando o uso de outros programas pelo discente.

**Questão 3 (Notificações de Fórum):**
> Em que medida o discente recebe notificações por e-mail sobre novas postagens em fóruns de discussão subscritos?

* **Hipótese 3.1 (H3.1):** O discente não recebe os e-mails de notificação de novas mensagens em fóruns que acompanha, mesmo com a opção ativada.

**Questão 4 (Calendário Externo):**
> Em que medida o Aprender 3 permite a exportação para calendários externos?

* **Hipótese 4.1 (H4.1):** Os principais serviços de calendário (Google, Outlook) falham ao tentar importar o calendário do Aprender 3 usando o link de subscrição (URL).
* **Hipótese 4.2 (H4.2):** A importação manual (arquivo `.ics`) funciona, mas a importação automática (via link) falha, indicando um problema específico no mecanismo de atualização automática.

**Questão 5 (Compatibilidade de Interação):**
> Qual é a consistência da funcionalidade drag-and-drop entre os navegadores suportados?

* **Hipótese 5.1 (H5.1):** A funcionalidade de "arrastar e soltar" arquivos (ex: envio de tarefas) falha muito mais em navegadores específicos (ex: Firefox, Safari) do que no navegador principal (ex: Chrome).

---

### Critérios de Julgamento da Característica (Compatibilidade)

Em conformidade com o Estabelecimento de Critérios de Julgamento, são definidos os critérios para o julgamento final da característica **Compatibilidade** como um todo. Os níveis de pontuação das métricas individuais (Excelente, Bom, Regular, Insatisfatório) serão agregados para fornecer um veredito final, conforme a tabela abaixo:

| Julgamento Final | Critério de Agregação |
| :--- | :--- |
| **Aceitável** | No mínimo 70% das métricas avaliadas obtiveram pontuação "Bom" ou "Excelente" E nenhuma métrica obteve pontuação "Insatisfatório". |
| **Parcialmente aceitável** | No mínimo 50% das métricas avaliadas obtiveram pontuação "Regular" ou superior, OU se alguma métrica-chave (ex: M1.1, M3.1) obteve pontuação "Insatisfatório". |
| **Inaceitável** | Mais de 30% das métricas avaliadas obtiveram pontuação "Insatisfatório", indicando falhas sistêmicas na compatibilidade. |

---

### Seleção das Métricas

**Questão 1 (Sincronia de Dados):**

* **Métrica 1.1: Percentual de Discrepância de Status de Conclusão**
    * **Definição:** A porcentagem de atividades que, após serem marcadas como "concluídas" em uma plataforma (Web ou App) e a ação de sincronização ser executada, não refletem essa mudança na outra plataforma.
    * **Fórmula:** (% Discrepância) = (Nº de atividades com status diferente / Nº total de atividades testadas) x 100
    * **Coleta:**
        1. Selecionar uma amostra de N atividades para o teste.
        2. Na plataforma A (ex: Web), marcar a atividade como "concluída".
        3. Executar a ação de sincronização na plataforma B (ex: App).
        4. Verificar se o status da atividade na plataforma B foi atualizado para "concluída".
        5. Registrar o resultado (sucesso ou discrepância) e repetir para N atividades.
    * **Propósito:** Medir a compatibilidade da sincronização do progresso do aluno entre os dois ambientes.
    * **Critérios de Julgamento:**
    
    | Excelente | Bom | Regular | Insatisfatório |
    | :--- | :--- | :--- | :--- |
    | 0% de discrepância | <= 2% de discrepância | 2% a 5% de discrepância | > 5% de discrepância |

* **Métrica 1.2: Taxa de Sucesso de Sincronização Bidirecional de Arquivos**
    * **Definição:** A taxa de sucesso de operações de arquivo (criar, enviar, deletar) na área privada do usuário, testadas em ambas as direções (da Web para o App e do App para a Web).
    * **Fórmula:** Média ( (Sucesso Web-para-App / Total) , (Sucesso App-para-Web / Total) ) x 100
    * **Coleta:**
        1. (Web-para-App): Fazer upload de N arquivos na área "Arquivos Privados" via Web.
        2. (Web-para-App): Sincronizar o App e verificar se os N arquivos estão visíveis.
        3. (App-para-Web): Fazer upload de M arquivos na área "Arquivos Privados" via App.
        4. (App-para-Web): Atualizar a página Web e verificar se os M arquivos estão visíveis.
        5. Registrar o número de sucessos em cada direção.
    * **Propósito:** Garantir que os arquivos do usuário estejam consistentes e acessíveis em ambos os locais.
    * **Critérios de Julgamento:**

    | Excelente | Bom | Regular | Insatisfatório |
    | :--- | :--- | :--- | :--- |
    | 100% de sucesso | 98% a 99.9% de sucesso | 90% a 97.9% de sucesso | < 90% de sucesso |

**Questão 2 (Recursos do Navegador):**

* **Métrica 2.1: Consumo Médio de RAM por Navegador**
    * **Definição:** A média de memória RAM (em Megabytes) usada pelo navegador após executar um cenário de teste padrão (ex: logar, abrir um curso, rolar a página).
    * **Fórmula:** Média(RAM)_Browser A vs Média(RAM)_Browser B vs Média(RAM)_Browser C
    * **Coleta:**
        1. Definir um cenário de teste padrão (ex: login, abrir curso X, rolar a página até o fim).
        2. Abrir o Navegador A (ex: Chrome) em um estado "limpo" (sem outras abas).
        3. Executar o cenário de teste padrão.
        4. Usar o gerenciador de tarefas do navegador para medir a RAM (em MB) usada pelo processo.
        5. Fechar, reabrir e repetir N vezes para o Navegador A para obter a média.
        6. Repetir todos os passos para o Navegador B (ex: Firefox) e C (ex: Safari).
    * **Propósito:** Avaliar o impacto de desempenho da plataforma em diferentes navegadores.
    * **Critérios de Julgamento:** (Baseado na variação entre o navegador mais leve e o mais pesado)

    | Excelente | Bom | Regular | Insatisfatório |
    | :--- | :--- | :--- | :--- |
    | Variação < 15% | Variação de 15% a 30% | Variação de 30% a 50% | Variação > 50% |

**Questão 3 (Notificações de Fórum):**

* **Métrica 3.1: Taxa de Falha de Entrega de Notificação**
    * **Definição:** A porcentagem de novas postagens em fóruns que não geraram um e-mail de notificação para o usuário após a execução do serviço de envio de mensagens do Moodle.
    * **Fórmula:** (Nº de postagens que NÃO geraram e-mail / Nº total de postagens de teste) x 100
    * **Coleta:**
        1. Configurar um usuário de teste subscrito em um Fórum A.
        2. Criar N postagens de teste no Fórum A.
        3. Executar manualmente o serviço agendado ("cron") de notificações do Moodle.
        4. Verificar a caixa de entrada do usuário de teste e os logs do servidor de e-mail.
        5. Contar quantos dos N e-mails esperados não foram recebidos.
    * **Propósito:** Verificar a compatibilidade do sistema de alertas por e-mail, que é vital para a comunicação.
    * **Critérios de Julgamento:**

    | Excelente | Bom | Regular | Insatisfatório |
    | :--- | :--- | :--- | :--- |
    | 0% de falha | <= 1% de falha | 1% a 5% de falha | > 5% de falha |

**Questão 4 (Calendário Externo):**

* **Métrica 4.1: Taxa de Falha de Subscrição de URL (Interoperabilidade)**
    * **Definição:** A taxa de falha ao tentar adicionar o calendário do Aprender 3 em serviços de terceiros (Google, Outlook) usando o link de subscrição dinâmico (URL).
    * **Fórmula:** (Nº de tentativas de subscrição que falharam / Nº total de tentativas) x 100
    * **Coleta:**
        1. Gerar o link (URL) de subscrição de calendário no Aprender 3.
        2. Acessar uma conta de teste no Google Calendar.
        3. Tentar adicionar o calendário "a partir do URL" usando o link gerado.
        4. Registrar se a operação inicial foi bem-sucedida.
        5. Repetir o processo para o Outlook Calendar.
    * **Propósito:** Validar se o link de calendário automático é compatível com os serviços mais populares.
    * **Critérios de Julgamento:** (Baseado no % de serviços testados que falharam)

    | Excelente | Parcial | Insatisfatório |
    | :--- | :--- | :--- |
    | 0% de falha (Funciona em todos) | 50% de falha (Ex: Funciona no Google, falha no Outlook) | 100% de falha (Não funciona em nenhum) |

* **Métrica 4.2: Diferencial de Sucesso (Importação Estática vs. Dinâmica)**
    * **Definição:** Uma métrica que compara a taxa de sucesso da importação manual (arquivo .ics) com a taxa de sucesso da subscrição automática (link URL).
    * **Fórmula:** (% Sucesso Importação Manual .ics) - (% Sucesso Subscrição URL)
    * **Coleta:**
        1. Executar o teste da Métrica 4.1 (Subscrição de URL) e registrar a taxa de sucesso (% Sucesso URL).
        2. No Aprender 3, exportar o mesmo calendário como um arquivo estático `.ics`.
        3. No Google Calendar (e Outlook), usar a opção "Importar" para o arquivo `.ics`.
        4. Registrar a taxa de sucesso da importação manual (% Sucesso Manual).
        5. Calcular a diferença (Fórmula).
    * **Propósito:** Diagnosticar se as falhas (H4.2) estão na geração dos dados (no arquivo .ics) ou no mecanismo que fornece o link dinâmico.
    * **Critérios de Julgamento:** (Resultado binário que valida ou refuta a H4.2)

    | Hipótese Refutada (Resultado Ideal) | Hipótese Validada (Problema Encontrado) |
    | :--- | :--- |
    | Diferencial = 0% (URL funciona tão bem quanto o arquivo) | Diferencial > 0% (Manual funciona, mas URL falha) |

**Questão 5 (Compatibilidade de Interação):**

* **Métrica 5.1: Taxa de Sucesso de Drag-and-Drop (D&D) por Navegador**
    * **Definição:** A porcentagem de tentativas de "arrastar e soltar" arquivos que funcionam corretamente na área de envio de tarefas, medida para cada navegador.
    * **Fórmula:** (% Sucesso D&D) = (Nº de uploads via D&D bem-sucedidos / Nº total de tentativas D&D) x 100
    * **Coleta:**
        1. Abrir o Navegador A (ex: Chrome) em uma página de envio de tarefa.
        2. Arrastar um arquivo do explorador de arquivos local para a caixa de upload designada.
        3. Verificar se o arquivo foi reconhecido e carregado com sucesso.
        4. Repetir N vezes para garantir consistência.
        5. Repetir todos os passos para o Navegador B (Firefox) e C (Safari).
    * **Propósito:** Medir a consistência da interface de usuário, garantindo que formas de interação essenciais funcionem para todos.
    * **Critérios de Julgamento:**

    | Excelente | Bom | Regular | Insatisfatório |
    | :--- | :--- | :--- | :--- |
    | 100% de sucesso em todos os navegadores | 100% no Chrome e Firefox; >95% no Safari | 100% no Chrome; falhas notáveis (50-95%) nos demais | Falha total (< 50%) em qualquer navegador |

---

## Diagrama GQM - (Representação Estrutural)

![Diagrama GQM de Compatibilidade](./imagens/diagrama_compatibilidade.svg)