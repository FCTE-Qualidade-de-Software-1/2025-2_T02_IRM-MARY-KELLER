# 2. Casos de Teste – Portabilidade

Esta seção apresenta os **Casos de Teste (CTs)** projetados para avaliar a característica **Portabilidade** do Aprender 3, conforme o Objetivo de Medição 2 definido no modelo GQM.

Cada CT está explicitamente associado a:

- uma **Questão GQM**;
- uma **Métrica**;
- as **Hipóteses** correspondentes (quando aplicável);
- os **critérios de julgamento** definidos na Fase 2 (Excelente, Bom, Regular, Insatisfatório).

O cálculo numérico das métricas deve seguir **exatamente** as fórmulas definidas na Fase 2.

---

## 2.1. Casos de Teste de Portabilidade

### CT-POR-01: Conformidade de Layout Responsivo (Web – Desktop, Tablet e Smartphone)

- **Questão GQM:** Q1 (Adaptabilidade)  
- **Métrica Associada:** Métrica 1.1 – Taxa de Conformidade de Layout Responsivo  
- **Hipótese Relacionada:** H1.1 – Layout responsivo se ajusta adequadamente  
- **Perfil Principal:** Discente / Equipe Técnica

#### Objetivo

Verificar se as principais páginas e funcionalidades do Aprender 3 mantêm layout funcional, sem quebras ou perda de elementos, em diferentes navegadores e resoluções (desktop, tablet, smartphone).

#### Pré-condições

- Navegadores instalados (versões estáveis mais recentes):  
  - Google Chrome  
  - Mozilla Firefox  
  - Microsoft Edge (ou Safari, se aplicável)
- Possibilidade de testar nas seguintes resoluções:
  - **Desktop:** largura > 1200 px  
  - **Tablet:** ~768 px  
  - **Smartphone:** ~375–480 px
- Conta de estudante ativa no Aprender 3.
- Lista de **N** páginas/funcionalidades críticas, por exemplo:
  - Página de login
  - Página inicial do curso
  - Visualização de tópico
  - Fórum (lista e visualização de discussão)
  - Envio de tarefa (tela de upload)
  - Calendário

#### Ambiente de Teste

- **Sistema Operacional:** Windows 10/11 ou Linux (Ubuntu 22.04 LTS ou equivalente) – registrar qual foi utilizado.  
- **Navegadores:** Chrome, Firefox, Edge.  
- **Resoluções:** Desktop / Tablet / Smartphone (via redimensionamento ou ferramentas de desenvolvedor).

#### Passos de Execução

1. Selecionar a lista de **N** páginas/funcionalidades críticas.
2. Para o **Navegador A** (por exemplo, Chrome):
   1. Ajustar para resolução **Desktop**.
   2. Acessar cada página da lista e verificar:
      - Elementos não sobrepostos;
      - Botões acessíveis;
      - Formulários utilizáveis.
   3. Registrar **Conforme / Não Conforme** para cada página.
   4. Repetir os passos para resolução **Tablet**.
   5. Repetir os passos para resolução **Smartphone**.
3. Repetir o mesmo procedimento para os Navegadores B (Firefox) e C (Edge).
4. Registrar todos os resultados em planilha.

#### Resultado Esperado

Idealmente, a grande maioria das combinações (página × navegador × resolução) apresenta layout conforme, sem perda de elementos essenciais.

#### Cálculo da Métrica 1.1

Calcular a porcentagem de combinações que ficaram conformes em relação ao total de combinações testadas.  
Ou seja, dividir o número de combinações conformes pelo número total de combinações avaliadas e multiplicar o resultado por 100 para obter o valor em percentual de conformidade.



#### Classificação (Métrica 1.1)

| Faixa de Resultado           | Classificação   |
|------------------------------|-----------------|
| > 90% de conformidade        | Excelente       |
| 75% a 90% de conformidade    | Bom             |
| 60% a 74% de conformidade    | Regular         |
| < 60% de conformidade        | Insatisfatório  |

---

### CT-POR-02: Sucesso em Funcionalidades Essenciais no App Moodle

- **Questão GQM:** Q1 (Adaptabilidade)  
- **Métrica Associada:** Métrica 1.2 – Taxa de Sucesso em Funcionalidades no App Móvel  
- **Hipótese Relacionada:** H1.2 – App Moodle é alternativa viável ao navegador  
- **Perfil Principal:** Discente

#### Objetivo

Avaliar se o aplicativo oficial do Moodle permite a execução bem-sucedida de tarefas essenciais realizadas normalmente via navegador.

#### Pré-condições

- App Moodle instalado em dispositivo Android ou iOS (versão atual).
- Conta de estudante de teste cadastrada no Aprender 3.
- Checklist de tarefas críticas, por exemplo:
  - Visualizar disciplinas matriculadas.
  - Visualizar notas.
  - Acessar um fórum e responder a uma discussão.
  - Enviar uma tarefa com upload de arquivo.
  - Visualizar calendário com eventos.
  - Enviar mensagem a um professor/colega.

#### Ambiente de Teste

- **Dispositivo:** Smartphone Android ou iOS.
- **Conectividade:** Wi-Fi estável ou rede móvel – registrar condição.

#### Passos de Execução

1. Abrir o App Moodle no dispositivo de teste.
2. Configurar a conexão com o Aprender 3 (aprender3.unb.br), se ainda não estiver configurado.
3. Acessar a conta de estudante de teste.
4. Executar cada item do checklist de tarefas, registrando:
   - **Sucesso (S)**: tarefa concluída sem erros que impeçam o uso.
   - **Falha (F)**: não foi possível concluir a tarefa ou houve erro impeditivo.
5. Registrar as observações relevantes (mensagens de erro, lentidão anormal etc.).

#### Resultado Esperado

- A maioria das tarefas críticas deve ser concluída com sucesso pelo App.

#### Cálculo da Métrica 1.2

Calcular a porcentagem de tarefas bem-sucedidas no aplicativo em relação ao total de tarefas testadas.  
Ou seja, dividir o número de tarefas concluídas com sucesso pelo número total de tarefas avaliadas e multiplicar o resultado por 100 para obter o percentual de sucesso no app.


#### Classificação (Métrica 1.2)

| Faixa de Resultado          | Classificação   |
|-----------------------------|-----------------|
| > 90% de sucesso            | Excelente       |
| 75% a 90% de sucesso        | Bom             |
| 60% a 74% de sucesso        | Regular         |
| < 60% de sucesso            | Insatisfatório  |

---

### CT-POR-03: Verificação de Histórico de Migração (Aprender 2 → Aprender 3)

- **Questão GQM:** Q2 (Substituibilidade)  
- **Métrica Associada:** Métrica 2.1 – Verificação de Histórico de Migração  
- **Hipótese Relacionada:** H2.1 – Migração bem-sucedida entre versões  
- **Perfil Principal:** Equipe Técnica / Avaliação Documental

#### Objetivo

Verificar se há evidências concretas de que o Aprender 3 resultou de uma migração bem-sucedida a partir de versões anteriores (ex.: Aprender 2), mantendo a continuidade dos serviços e dados.

#### Pré-condições

- Acesso:
  - a documentos institucionais (atas, relatórios, comunicados oficiais da UnB);
  - a páginas informativas sobre o projeto Aprender 3;
  - a possíveis registros de migração técnica.

#### Passos de Execução

1. Pesquisar, em fontes oficiais da UnB, comunicados sobre a migração:
   - Site da UnB;
   - Comunicados da STI;
   - Documentação interna da equipe responsável.
2. Procurar evidências de:
   - Migração de dados (disciplinas, usuários, históricos etc.);
   - Período de transição entre Aprender 2 e Aprender 3;
   - Relatos de conclusão bem-sucedida da transição.
3. Registrar:
   - Se existe evidência explícita de migração bem-sucedida (**Sim/Não**).
   - Referências das fontes (data, link, documento).


#### Resultado Esperado

- Deve existir, ao menos, uma evidência clara de que a migração foi realizada com sucesso e o sistema se manteve operacional.

#### Cálculo da Métrica 2.1

Métrica qualitativa/binária:

- **Sim (S):** foi encontrada evidência clara de migração bem-sucedida.  
- **Não (N):** não foi encontrada evidência suficiente.

#### Classificação (Métrica 2.1)

| Valor | Interpretação        |
|-------|----------------------|
| Sim   | Hipótese validada    |
| Não   | Hipótese refutada    |

---

### CT-POR-04: Compatibilidade de Plugins e Temas na Atualização do Moodle

- **Questão GQM:** Q2 (Substituibilidade)  
- **Métrica Associada:** Métrica 2.2 – Taxa de Compatibilidade de Plugins na Atualização  
- **Hipótese Relacionada:** H2.2 – Natureza modular permite atualização de componentes  
- **Perfil Principal:** Equipe Técnica / Administração do Moodle

#### Objetivo

Avaliar o grau de dependência do Aprender 3 em relação a plugins e temas que não sejam compatíveis com a versão mais recente/planejada do Moodle.

#### Pré-condições

- Acesso à lista completa de plugins e temas do Aprender 3:
  - Plugins de atividade;
  - Blocos;
  - Temas;
  - Outros tipos de extensões.
- Versão atual do Moodle e versão-alvo de atualização (se houver).
- Acesso ao diretório oficial de plugins do Moodle.

#### Passos de Execução

1. Exportar/listar todos os plugins e temas instalados no Aprender 3.
2. Para cada plugin/tema:
   1. Buscar no diretório oficial de plugins do Moodle.
   2. Verificar se é compatível com a versão-alvo (ou com versões recentes).
   3. Registrar como:
      - **Compatível**;
      - **Não compatível**;
      - **Não encontrado** (se aplicável).
3. Contabilizar o total de plugins e o total de plugins compatíveis.


#### Resultado Esperado

- A maioria dos plugins e temas deve ser compatível com a versão-alvo, permitindo evolução da plataforma sem grandes impedimentos.

#### Cálculo da Métrica 2.2

Calcular a porcentagem de plugins compatíveis em relação ao total de plugins instalados.  
Ou seja, dividir o número de plugins compatíveis pelo número total de plugins e multiplicar o resultado por 100 para obter o percentual de compatibilidade de plugins.



#### Classificação (Métrica 2.2)

| Faixa de Resultado           | Classificação   |
|------------------------------|-----------------|
| > 90% compatíveis           | Excelente       |
| 75% a 90% compatíveis       | Bom             |
| 60% a 74% compatíveis       | Regular         |
| < 60% compatíveis           | Insatisfatório  |

---

### CT-POR-05: Sucesso na Configuração do App Moodle por Novos Usuários

- **Questão GQM:** Q3 (Instalabilidade)  
- **Métrica Associada:** Métrica 3.1 – Taxa de Sucesso na Configuração do App por Novos Usuários  
- **Hipótese Relacionada:** H3.1 – Processo complexo para usuários não técnicos  
- **Perfil Principal:** Discentes sem experiência prévia com o app

#### Objetivo

Medir a dificuldade real que novos usuários encontram para instalar e configurar o aplicativo Moodle a fim de acessar o Aprender 3.

#### Pré-condições

- Grupo de **N** usuários de teste sem experiência prévia com o app Moodle.
- Dispositivos móveis (Android/iOS), um por participante.
- A mesma instrução para todos:  
  > “Instale o aplicativo Moodle no seu celular e acesse sua conta do Aprender 3 (aprender3.unb.br).”

#### Passos de Execução

1. Entregar a instrução aos participantes, sem qualquer orientação adicional.
2. Observar o processo, sem interferir, até um tempo máximo pré-definido (por exemplo, 20–30 minutos).
3. Para cada participante, registrar:
   - Se conseguiu configurar e acessar o Aprender 3 sozinho (**Sucesso**);
   - Se não conseguiu sem ajuda (**Falha**);
   - Principais dificuldades relatadas (ex.: não encontrou o servidor, erro na URL, dúvidas de login).


#### Resultado Esperado

- A maior parte dos usuários deve obter **Sucesso (S)** sem auxílio técnico, indicando boa instalabilidade.

#### Cálculo da Métrica 3.1

Calcular a porcentagem de usuários que conseguiram configurar o aplicativo com sucesso em relação ao total de usuários testados.  
Ou seja, dividir o número de usuários bem-sucedidos pelo número total de participantes e multiplicar o resultado por 100 para obter o percentual de sucesso na configuração.


#### Classificação (Métrica 3.1)

| Faixa de Resultado         | Classificação   |
|----------------------------|-----------------|
| > 90% de sucesso           | Excelente       |
| 75% a 90% de sucesso       | Bom             |
| 60% a 74% de sucesso       | Regular         |
| < 60% de sucesso           | Insatisfatório  |

---

### CT-POR-06: Verificação de Dependências de Navegador (Navegador Limpo)

- **Questão GQM:** Q3 (Instalabilidade)  
- **Métrica Associada:** Métrica 3.2 – Verificação de Dependências de Navegador  
- **Hipótese Relacionada:** H3.2 – Não exige instalação de plugins específicos  
- **Perfil Principal:** Equipe Técnica

#### Objetivo

Verificar se o funcionamento básico do Aprender 3 exige a instalação de qualquer software, plugin ou extensão adicional no navegador, o que impactaria negativamente a portabilidade.

#### Pré-condições

- Navegador recém-instalado, em estado “limpo” (sem extensões de terceiros).
- Acesso ao Aprender 3.

#### Passos de Execução

1. Abrir o navegador recém-instalado (Chrome, Firefox ou Edge) em sua configuração padrão.
2. Acessar o endereço do Aprender 3.
3. Executar o seguinte checklist mínimo de funcionalidades:
   - Realizar login com usuário de teste.
   - Visualizar a lista de disciplinas.
   - Acessar um curso.
   - Visualizar conteúdo (página, arquivo PDF básico, página de fórum).
   - Enviar uma tarefa com upload simples de arquivo.
4. Verificar se, durante qualquer uma das funcionalidades, o sistema:
   - Solicita instalação de plugins, extensões ou software adicional;
   - Exige componentes proprietários (fora dos padrões HTML5, por exemplo).
5. Registrar o resultado da verificação.


#### Resultado Esperado

- Nenhuma funcionalidade básica deve exigir instalação de plugins/extensões adicionais.

#### Cálculo da Métrica 3.2

Métrica qualitativa/binária:

- **Sim:** funcionamento básico sem dependências extras.  
- **Não:** há exigência de plugins ou softwares adicionais.

---


