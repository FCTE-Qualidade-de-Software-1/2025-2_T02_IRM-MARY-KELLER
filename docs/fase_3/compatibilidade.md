# Casos de Teste – Compatibilidade

Esta seção descreve os **Casos de Teste (CTs)** projetados para avaliar a característica de **Compatibilidade** do Aprender 3, de acordo com o modelo **GQM** definido na Fase 2.

Cada CT está explicitamente associado a:

- uma **Questão GQM**,  
- uma **Métrica** (conforme definido na Fase 2),  
- e, quando aplicável, às **Hipóteses** correspondentes.

O cálculo numérico de cada métrica e a classificação dos resultados **devem seguir exatamente as fórmulas e critérios de julgamento definidos na Fase 2** (Excelente, Bom, Regular, Insatisfatório).

> **Ambiente de teste (padrão):**  
> - Sistema Operacional: **Windows 10/11** ou **Linux (Ubuntu 22.04 LTS ou equivalente)**, desde que o **SO utilizado seja explicitamente registrado** nos resultados.  
> - Navegadores: **Google Chrome**, **Mozilla Firefox**, **Microsoft Edge**, em suas versões estáveis mais recentes.  
> - Aplicativo: **App Moodle** (Android, versão mais recente).

---

## CT-COMP-01: Sincronia de Status de Conclusão

- **Questão GQM:** Q1 (Sincronia de Dados)  
- **Métrica Associada:** Métrica 1.1 – Percentual de Discrepância de Status de Conclusão  
- **Hipótese Relacionada:** H1.1 – Inconsistência de status “concluída” entre Web e App  
- **Perfil Principal:** Discente (conta de estudante de teste)

**Objetivo:**  
Verificar se o status de **conclusão de atividades** marcado na interface **Web** é corretamente refletido no **App Moodle**, medindo a discrepância entre os dois ambientes.

**Pré-condições:**

- Conta de estudante de teste cadastrada no Aprender 3.
- Curso de teste com pelo menos **N atividades** configuradas com **rastreamento de conclusão**.
- Acesso ao Aprender 3 via navegador (Web) e ao **App Moodle** no Android.
- SO utilizado (Windows ou Linux) registrado no plano de execução.

**Passos de Execução:**

1. [Web] Acessar o Aprender 3 (`https://aprender3.unb.br/`) com a conta de estudante de teste.
2. Entrar no curso de teste que contém as atividades com conclusão configurada.
3. Selecionar uma amostra de **N atividades** (por exemplo, tarefas, questionários, páginas).
4. Para cada uma das N atividades, marcar manualmente como **“concluída”** na interface Web (por meio de checkboxes, critérios automáticos ou botão “Marcar como concluída”, conforme configuração).
5. [App] Abrir o **App Moodle** no dispositivo Android, acessar a mesma conta de estudante e o mesmo curso.
6. Forçar a sincronização/atualização do curso (puxar para atualizar ou usar opção de sincronização do app).
7. Verificar, para cada uma das N atividades da amostra, se o status exibido no App Moodle corresponde ao status exibido na Web.
8. Registrar, em planilha, para cada atividade:  
   - ID da atividade  
   - Status na Web  
   - Status no App  
   - Indicador de **coerência** (Sim/Não).

**Resultado Esperado:**

- Idealmente, **todas** as atividades apresentam o mesmo status de conclusão em ambos os ambientes (0 discrepâncias).
- Eventuais discrepâncias devem ser quantificadas e descritas (ex.: atividades marcadas como concluídas na Web mas não no App).

**Cálculo da Métrica e Classificação:**

- Aplicar, sobre os dados coletados, a **fórmula da Métrica 1.1** definida na Fase 2.  
- Classificar o resultado conforme os **critérios de julgamento da Métrica 1.1** (Excelente, Bom, Regular, Insatisfatório) estabelecidos na Fase 2.

---

## CT-COMP-02: Sincronização Bidirecional de Arquivos

- **Questão GQM:** Q1 (Sincronia de Dados)  
- **Métrica Associada:** Métrica 1.2 – Taxa de Sucesso de Sincronização Bidirecional de Arquivos  
- **Hipótese Relacionada:** H1.2 – Problemas de sincronização de “Arquivos privados” entre Web e App  
- **Perfil Principal:** Discente

**Objetivo:**  
Avaliar se operações de **upload e sincronização de arquivos** na área **“Arquivos privados”** são bem-sucedidas tanto da **Web para o App** quanto do **App para a Web**.

**Pré-condições:**

- Conta de estudante de teste com acesso à área **“Arquivos privados”**.
- Conjunto de arquivos de teste (por exemplo: PDF, DOCX, imagens).
- Acesso Web (navegador) e App Moodle (Android).
- SO utilizado (Windows ou Linux) registrado nos resultados.

**Passos de Execução (Web → App):**

1. [Web] Fazer login no Aprender 3 como estudante de teste.
2. Acessar a área **“Arquivos privados”**.
3. Fazer upload de **N arquivos de teste** (registrar nomes e tipos).
4. Salvar as alterações (se aplicável).
5. [App] Abrir o App Moodle, acessar a mesma conta e navegar até a área equivalente de arquivos.
6. Sincronizar/atualizar o app.
7. Verificar se **todos os N arquivos** aparecem corretamente no App (nome, tipo e possibilidade de download/visualização).
8. Registrar, em planilha, quantos arquivos foram sincronizados com sucesso na direção **Web → App**.

**Passos de Execução (App → Web):**

9. [App] Na área de arquivos, enviar **M novos arquivos** (diferentes dos anteriores, se possível).
10. Sincronizar o App (se necessário).
11. [Web] Reabrir o Aprender 3 no navegador e acessar a área **“Arquivos privados”**.
12. Verificar se **todos os M arquivos** enviados via App aparecem corretamente na Web.
13. Registrar, em planilha, quantos arquivos foram sincronizados com sucesso na direção **App → Web**.

**Resultado Esperado:**

- A sincronização deve ser bem-sucedida em **ambas as direções**, sem perda de arquivos ou inconsistência de visualização.

**Cálculo da Métrica e Classificação:**

- Aplicar, aos dados Web → App e App → Web, a **fórmula da Métrica 1.2** definida na Fase 2.  
- Classificar a taxa de sucesso resultante conforme os **critérios de julgamento da Métrica 1.2** na Fase 2.

---

## CT-COMP-03: Consumo Médio de RAM por Navegador

- **Questão GQM:** Q2 (Recursos do Navegador)  
- **Métrica Associada:** Métrica 2.1 – Consumo Médio de RAM por Navegador  
- **Hipótese Relacionada:** H2.1 – Consumo de RAM maior em um navegador específico prejudicando o uso do discente  
- **Perfil Principal:** Técnico/Equipe de Avaliação

**Objetivo:**  
Medir e comparar o **consumo médio de memória RAM** do Aprender 3 em diferentes navegadores (Chrome, Firefox, Edge) para um cenário de uso padrão.

**Pré-condições:**

- Um computador com SO definido (Windows ou Linux) e registrado no relatório.
- Navegadores instalados: **Chrome**, **Firefox** e **Edge**, nas versões estáveis mais recentes.
- Conta de estudante de teste com acesso a um curso com conteúdo (tópicos, fóruns, tarefas).

**Cenário de Teste Padrão:**

- Login no Aprender 3, abertura de um curso, navegação por tópicos, abertura de fórum e tarefa, rolagem até o fim da página.

**Passos de Execução:**

1. Fechar todos os navegadores e aguardar alguns segundos para estabilizar o uso de RAM.
2. Abrir apenas o **Navegador A** (por exemplo, Chrome).
3. Executar o **cenário de teste padrão** no Aprender 3.
4. Utilizar o **gerenciador de tarefas** do sistema ou do próprio navegador para registrar o consumo de RAM (em MB) do processo principal do navegador.
5. Anotar o valor em planilha.
6. Fechar o navegador A por completo.
7. Repetir os passos 2 a 6 **ao menos N vezes** para o Navegador A (por exemplo, 3 repetições) e registrar todos os valores.
8. Repetir o mesmo procedimento para o **Navegador B** (Firefox) e para o **Navegador C** (Edge), mantendo o mesmo cenário e número de repetições.
9. Calcular, em planilha, o **consumo médio de RAM** para cada navegador (A, B, C).

**Resultado Esperado:**

- Espera-se que a variação de consumo médio de RAM entre navegadores não seja excessiva a ponto de comprometer o uso do Aprender 3 para os alunos.

**Cálculo da Métrica e Classificação:**

- A partir das médias calculadas por navegador, aplicar a **definição da Métrica 2.1** e a forma de comparação estabelecida na Fase 2.  
- Classificar a variação percentual entre o navegador mais leve e o mais pesado conforme os **critérios de julgamento da Métrica 2.1** definidos na Fase 2.

---

## CT-COMP-04: Entrega de Notificações de Fórum por E-mail

- **Questão GQM:** Q3 (Notificações de Fórum)  
- **Métrica Associada:** Métrica 3.1 – Taxa de Falha de Entrega de Notificação  
- **Hipótese Relacionada:** H3.1 – Discente não recebe e-mails de novas mensagens em fóruns subscritos  
- **Perfil Principal:** Discente / Equipe Técnica (para logs)

**Objetivo:**  
Verificar se o Aprender 3 envia corretamente **e-mails de notificação** para um discente subscrito em um fórum, após novas postagens.

**Pré-condições:**

- Conta de estudante de teste com endereço de e-mail funcional (institucional ou de laboratório).
- Curso de teste com um **fórum configurado**.
- Acesso ao painel de administração/logs de e-mail (se autorizado).
- Tarefas agendadas (cron) do Moodle corretamente configuradas no ambiente de teste ou produção.

**Passos de Execução:**

1. Selecionar um fórum de teste em um curso do Aprender 3.
2. [Estudante de teste] Fazer login na Web e se **inscrever/subscrever** ao fórum (caso a inscrição não seja automática).
3. Confirmar que a opção de **notificação por e-mail** está ativada para o usuário.
4. Criar uma sequência de **N postagens** de teste no fórum (podem ser feitas por diferentes contas para simular uso real).
5. Garantir que o **cron** do Moodle seja executado (automaticamente ou manualmente, conforme ambiente).
6. Monitorar a caixa de entrada do e-mail do estudante de teste por um período adequado (por exemplo, até o ciclo completo de execução do cron + atraso normal esperado).
7. Registrar, em planilha, para cada uma das N postagens:
   - Data/hora da postagem  
   - Se o e-mail de notificação foi recebido ou não  
   - Eventuais atrasos significativos (se forem relevantes ao contexto).
8. Quando possível, consultar os **logs de e-mail** no servidor/Moodle para confirmar o envio das mensagens.

**Resultado Esperado:**

- Idealmente, todas as **N postagens** geram e-mails de notificação corretamente entregues ao discente (0 falhas).

**Cálculo da Métrica e Classificação:**

- Aplicar a **fórmula da Métrica 3.1**, conforme definida na Fase 2, sobre o número de notificações esperadas versus recebidas.  
- Classificar a taxa de falha obtida utilizando os **critérios da Métrica 3.1** definidos na Fase 2.

---

## CT-COMP-05: Subscrição de Calendário via URL

- **Questão GQM:** Q4 (Calendário Externo)  
- **Métrica Associada:** Métrica 4.1 – Taxa de Falha de Subscrição de URL  
- **Hipótese Relacionada:** H4.1 – Falhas na subscrição do calendário do Aprender 3 por serviços externos  
- **Perfil Principal:** Discente / Equipe de Avaliação

**Objetivo:**  
Testar se o calendário do Aprender 3 pode ser corretamente **assinado via URL** em serviços externos, como **Google Calendar** e **Outlook Calendar**.

**Pré-condições:**

- Conta de estudante de teste no Aprender 3, com calendário acadêmico configurado (atividades com datas, prazos).
- Conta de teste no **Google Calendar**.
- Conta de teste no **Outlook Calendar**.
- Acesso à funcionalidade do Aprender 3 que gera o **link de subscrição (URL)** do calendário.

**Passos de Execução:**

1. [Aprender 3] Fazer login como estudante de teste e acessar a área de **Calendário**.
2. Gerar/copiar o **link de subscrição (URL)** fornecido pelo Aprender 3 para integração com calendários externos.
3. [Google Calendar] Acessar a conta de teste e usar a opção **“Adicionar calendário a partir de URL”**.
4. Colar o link gerado pelo Aprender 3 e confirmar.
5. Verificar se o calendário é adicionado com sucesso e se os eventos aparecem (após eventual tempo de sincronização).
6. Registrar o resultado da tentativa (Sucesso/Falha) em planilha.
7. [Outlook Calendar] Repetir o procedimento na conta de teste do Outlook (adicionar calendário a partir de URL).
8. Verificar se o calendário é adicionado e sincroniza corretamente; registrar o resultado (Sucesso/Falha).
9. Ao final, contabilizar o número total de tentativas e o número de falhas por serviço.

**Resultado Esperado:**

- O calendário do Aprender 3 é subscrito corretamente em todos os serviços testados (Google e Outlook).

**Cálculo da Métrica e Classificação:**

- Calcular, com base nas tentativas realizadas, a taxa conforme a **Métrica 4.1** definida na Fase 2.  
- Classificar a situação (0%, 50%, 100% de falha) conforme os **critérios de julgamento da Métrica 4.1** estabelecidos na Fase 2.

---

## CT-COMP-06: Importação Estática (.ics) vs Subscrição Dinâmica (URL)

- **Questão GQM:** Q4 (Calendário Externo)  
- **Métrica Associada:** Métrica 4.2 – Diferencial de Sucesso (Importação Estática vs Dinâmica)  
- **Hipótese Relacionada:** H4.2 – Problema específico na subscrição automática, com importação manual funcionando melhor  
- **Perfil Principal:** Discente / Equipe de Avaliação

**Objetivo:**  
Comparar a **taxa de sucesso** entre:
- a **subscrição automática via URL** (já testada no CT-COMP-05)  
e
- a **importação manual via arquivo `.ics`**,

identificando se há diferença significativa entre os dois métodos.

**Pré-condições:**

- Mesmas contas e configurações utilizadas no CT-COMP-05 (Aprender 3, Google Calendar, Outlook Calendar).
- Acesso à funcionalidade do Aprender 3 que permite **exportar o calendário como arquivo `.ics`**.

**Passos de Execução:**

1. Reutilizar os resultados de subscrição por URL obtidos no **CT-COMP-05** (não é necessário repetir).
2. [Aprender 3] Acessar o calendário do estudante de teste e exportar o calendário em formato **`.ics`**.
3. [Google Calendar] Acessar a conta de teste e usar a opção **“Importar”** para carregar o arquivo `.ics`.
4. Verificar se os eventos são importados corretamente (sem erros de arquivo).
5. Registrar o resultado (Sucesso/Falha) em planilha.
6. [Outlook Calendar] Repetir o procedimento de importação manual do arquivo `.ics` na conta de teste.
7. Verificar se o calendário é importado corretamente; registrar o resultado.
8. Ao final, contabilizar a taxa de sucesso da **importação manual** e comparar com a taxa de sucesso da **subscrição via URL** obtida no CT-COMP-05.

**Resultado Esperado:**

- Idealmente, não deve haver diferença de sucesso entre método manual (.ics) e método dinâmico (URL).

**Cálculo da Métrica e Classificação:**

- Aplicar a **definição da Métrica 4.2** (diferencial entre taxas) conforme estabelecida na Fase 2.  
- Avaliar se o resultado **valida ou refuta a hipótese H4.2**, seguindo a interpretação indicada nos **critérios da Métrica 4.2** na Fase 2.

---

## CT-COMP-07: Sucesso da Funcionalidade Drag-and-Drop (D&D) por Navegador

- **Questão GQM:** Q5 (Compatibilidade de Interação)  
- **Métrica Associada:** Métrica 5.1 – Taxa de Sucesso de Drag-and-Drop (D&D) por Navegador  
- **Hipótese Relacionada:** H5.1 – Falhas concentradas em navegadores específicos na funcionalidade de arrastar e soltar  
- **Perfil Principal:** Discente

**Objetivo:**  
Medir a **taxa de sucesso** da funcionalidade de **“arrastar e soltar” (drag-and-drop)** de arquivos na área de envio de tarefas do Aprender 3 para diferentes navegadores (Chrome, Firefox, Edge).

**Pré-condições:**

- Conta de estudante de teste matriculada em um curso que possua uma atividade de **envio de tarefa** com upload de arquivos habilitado.
- Conjunto de arquivos de teste (PDF, DOCX, imagens).
- Navegadores Chrome, Firefox e Edge instalados, em suas versões estáveis mais recentes.
- SO utilizado (Windows ou Linux) registrado nos resultados.

**Passos de Execução:**

1. Selecionar uma atividade de **envio de tarefa** no curso de teste (a mesma atividade será usada em todos os navegadores).
2. Definir o número de tentativas **N** por navegador (por exemplo, N = 10 tentativas).
3. Para o **Navegador A** (por exemplo, Chrome):
   1. Abrir o Aprender 3 e acessar a tarefa de envio de arquivos.
   2. Para cada uma das N tentativas:
      - Arrastar um arquivo do explorador de arquivos até a área de upload da tarefa.
      - Verificar se o arquivo é reconhecido e enviado corretamente (aparece na listagem de arquivos da tarefa).
      - Registrar **Sucesso** ou **Falha** em planilha.
   3. Ao final, contabilizar o número de sucessos no Navegador A.
4. Repetir o mesmo procedimento para o **Navegador B** (Firefox) e para o **Navegador C** (Edge), utilizando os mesmos arquivos ou conjunto equivalente.
5. Ao final de todos os testes, registrar em planilha:
   - Nº de tentativas por navegador  
   - Nº de sucessos por navegador  
   - Comentários sobre falhas observadas (mensagens de erro, comportamento da interface, etc.).

**Resultado Esperado:**

- Idealmente, a taxa de sucesso do D&D é **alta e consistente** em todos os navegadores, sem falhas recorrentes em um navegador específico.

**Cálculo da Métrica e Classificação:**

- A partir das contagens de sucessos e tentativas, aplicar a **Métrica 5.1** definida na Fase 2 para cada navegador.  
- Classificar os resultados de acordo com os **critérios de julgamento da Métrica 5.1** (Excelente, Bom, Regular, Insatisfatório) estabelecidos na Fase 2, verificando se a hipótese H5.1 é suportada ou refutada.

---
