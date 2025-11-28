# Resultados dos Testes de Portabilidade

Esta seção descreve os testes realizados e resultados obtidos com base nos **Casos de Teste, CTs** projetados para avaliar a característica de **Portabilidade** do Aprender 3, conforme planejamento realizado na Fase 3.

---

## CT-POR-01: Conformidade de Layout Responsivo, Web, Desktop, Tablet e Smartphone

### Detalhamento do Caso de Teste  
**Questão GQM:** Q1, *O layout do Aprender 3 adapta-se adequadamente a diferentes dispositivos e resoluções, mantendo a usabilidade e o acesso às funcionalidades principais?*  
**Métrica Associada:** 1.1, Taxa de Conformidade de Layout Responsivo  
**Hipótese Avaliada:** H1.1, *O layout responsivo se ajusta adequadamente em desktop, tablet e smartphone, sem causar perda de acesso a conteúdo ou sobreposição de elementos.*  
**Perfil:** Discente

---

### Resultados Obtidos  

#### Ambiente de Teste  

- **Resoluções testadas:**
  - Desktop: 1920 x 1080 px  
  - Tablet: 768 x 1024 px  
  - Smartphone: 375 x 667 px  
- **Páginas avaliadas:** Página de Login, Página Inicial do Curso, Visualização de Tópico, Fórum, Lista de Discussões, Calendário  
- **Método:** Utilização da ferramenta de desenvolvimento, Device Toolbar, em três navegadores, Chrome, Firefox e Edge, simulando as diferentes resoluções.

#### Resultados por Resolução  

**Desktop, 1920 x 1080 px**  
- **Conformidade:** 15 de 15 combinações, 100%  
- Todas as páginas funcionaram adequadamente, sem sobreposição de elementos, sem perda de conteúdo e com navegação fluida.

**Tablet, 768 x 1024 px**  
- **Conformidade:** 11 de 15 combinações, 73,33%  
- **Não conformidades identificadas:**
  - Página Inicial, Chrome: blocos laterais sobrepostos ao conteúdo principal.  
  - Fórum, Firefox: imagens de avatar colapsadas e texto sobreposto em determinadas linhas.  
  - Fórum, Edge: tabela não responsiva, com informações cortadas nas laterais.  
  - Calendário, Edge: eventos com texto cortado, dificultando a leitura.

**Smartphone, 375 x 667 px**  
- **Conformidade:** 6 de 15 combinações, 40%  
- **Não conformidades identificadas:**
  - Página Inicial, em todos os navegadores: blocos laterais não colapsam, gerando rolagem horizontal e poluição visual.  
  - Visualização de Tópico, Chrome e Edge: imagens excedem a largura da tela, causando rolagem horizontal.  
  - Fórum, em todos os navegadores: tabela não responsiva, colunas sobrepostas, avatares distorcidos e dificuldade de leitura.  
  - Calendário, Chrome e Firefox: grade praticamente ilegível, eventos cortados e área de clique reduzida para interação.

#### Resultados Consolidados  

- **Total de combinações avaliadas, página x navegador x resolução:** 45  
- **Conformes:** 32  
- **Não conformes:** 13  
- **Taxa de Conformidade Geral:** 71,11%  

#### Análise por Navegador  

| Navegador | Conformidade          | Classificação |
| :---      | :---                  | :---          |
| Chrome    | 11 de 15, 73,33%      | Regular       |
| Firefox   | 11 de 15, 73,33%      | Regular       |
| Edge      | 10 de 15, 66,67%      | Regular       |

#### Problemas Principais Identificados  

1. **Página Inicial em dispositivos móveis:** blocos laterais não colapsam, empurrando o conteúdo principal e exigindo rolagem horizontal.  
2. **Fórum em mobile e tablet:** tabelas não responsivas, avatares distorcidos, imagens que excedem o viewport e texto sobreposto.  
3. **Calendário em mobile e tablet:** grade pouco responsiva, eventos cortados e navegação pouco intuitiva, com baixa área de clique.  
4. **Visualização de Tópico em mobile:** imagens que não se ajustam à largura, resultando em rolagem horizontal e leitura prejudicada.  
5. **Página Inicial em tablet, Edge:** blocos laterais sobrepondo o conteúdo principal.

---

### Cálculo da Métrica 1.1  

A Métrica 1.1 mede a **Taxa de Conformidade de Layout Responsivo**, isto é, a proporção de combinações página, navegador, resolução que mantêm layout adequado, sem perda de conteúdo ou problemas graves de usabilidade.

**Fórmula utilizada:**  
Taxa de Conformidade = (Número de combinações conformes / Número total de combinações avaliadas) x 100  

Aplicando os valores obtidos:  

- Combinações conformes: 32  
- Total de combinações: 45  

Taxa de Conformidade = 32 dividido por 45, multiplicado por 100, resultando em **71,11%**

**Classificação segundo critérios da Fase 2:**

- Maior que 90%: Excelente  
- Entre 75% e 90%: Bom  
- Entre 60% e 74%: Regular  
- Menor que 60%: Insatisfatório  

Com 71,11% de conformidade, a classificação global da métrica é **REGULAR**.

---

### Análise e Resposta à Questão GQM  

> **Q1, O layout do Aprender 3 adapta-se adequadamente a diferentes dispositivos e resoluções, mantendo a usabilidade e o acesso às funcionalidades principais?**

Os resultados obtidos mostram que o Aprender 3 apresenta um comportamento claramente distinto entre cenários de uso. Em ambientes **desktop**, o layout se mostra totalmente adequado, com 100% de conformidade nas páginas e navegadores avaliados. Nessa condição, a organização dos elementos é preservada e não são observadas quebras visuais significativas.

No entanto, à medida que se reduzem as resoluções para contextos de **tablet** e especialmente de **smartphone**, as limitações do layout responsivo ficam evidentes. No tablet, a taxa de conformidade já cai para aproximadamente 73%, com problemas de sobreposição de blocos, tabelas pouco responsivas e cortes de conteúdo em diferentes páginas. Em dispositivos móveis, o cenário é mais crítico, com apenas 40% de conformidade, presença de rolagem horizontal em várias telas, avatares e imagens distorcidos e dificuldades significativas de leitura e interação, sobretudo no fórum e no calendário.

Assim, em resposta à Questão GQM 1, conclui-se que o Aprender 3 **adapta-se bem a dispositivos desktop**, mas apresenta **limitações importantes em tablets e, principalmente, em smartphones**, o que compromete a experiência de portabilidade plena para dispositivos móveis.

---

### Avaliação da Hipótese H1.1  

> **H1.1, O layout responsivo se ajusta adequadamente em desktop, tablet e smartphone, sem causar perda de acesso a conteúdo ou sobreposição de elementos.**

Os dados analisados indicam que a hipótese H1.1 **não se sustenta** quando se observam todos os dispositivos. Embora o comportamento em desktop seja plenamente satisfatório, com 100% de conformidade, a queda de desempenho em tablets e, sobretudo, em smartphones é significativa. Foram identificadas diversas situações de sobreposição de conteúdo, necessidade de rolagem horizontal, distorção de avatares e imagens, além de tabelas e grades, como a do calendário, que não se adaptam corretamente a telas menores.

Portanto, a hipótese é **refutada**, pois o layout responsivo do Aprender 3 **não se ajusta de forma adequada em todas as plataformas**, apresentando problemas relevantes em dispositivos móveis, justamente onde a portabilidade deveria ser mais favorecida.

---

### Demonstração em Vídeo  

A seguir encontra-se o vídeo que demonstra a execução dos testes de layout responsivo em diferentes resoluções, desktop, tablet e smartphone:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/e6U-lpBli9U"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## CT-POR-02: Sucesso em Funcionalidades Essenciais no App Moodle

### Detalhamento do Caso de Teste  
**Questão GQM:** Q1, *Em que medida o aplicativo oficial do Moodle permite que os discentes realizem, em ambiente móvel, as principais tarefas acadêmicas realizadas no Aprender 3 via navegador?*  
**Métrica Associada:** 1.2, Taxa de Sucesso em Funcionalidades Essenciais no App Móvel  
**Hipótese Avaliada:** H1.2, *O app Moodle é uma alternativa viável ao uso via navegador, permitindo que as principais funcionalidades sejam executadas com sucesso no contexto móvel.*  
**Perfil:** Discente  

---

### Resultados Obtidos  

#### Ambiente de Teste  

- **Dispositivo:** Pixel 9 Pro, emulado  
- **Sistema Operacional:** Android 16, Baklava  
- **Versão do App Moodle:** 5.0.0, atualizado em 27/06/2025  
- **Conexão:** Dados móveis emulados  

#### Funcionalidades Avaliadas  

O conjunto de testes contemplou tarefas essenciais para o uso acadêmico cotidiano, incluindo login, visualização de conteúdos, envio de tarefas, participação em fóruns e acesso offline a materiais previamente baixados.

##### Tabela de Resultados Detalhados  

| Categoria                  | Funcionalidade ou Item     | Status  | Observações                                                      |
| -------------------------- | -------------------------  | ------- | ---------------------------------------------------------------- |
| **Login e Autenticação**   | Login completo             | Sucesso | Autenticação com credenciais institucionais funcionou plenamente |
| **Visualização**           | Cursos                     | Sucesso | Listagem e acesso aos cursos funcionando                         |
|                            | PDF                        | Sucesso | Visualização e download funcionando                              |
|                            | Áudio                      | Sucesso | Reprodução funcionando                                           |
|                            | Link externo               | Sucesso | Abertura em navegador funcionando                                |
|                            | Notas                      | Sucesso | Notas exibidas corretamente                                      |
|                            | Notificações e mensagens   | Sucesso | Acesso e leitura funcionando                                     |
|                            | Conteúdo H5P               | Falha   | Erro: "Site not configured properly for mobile H5P content"      |
| **Envio de Tarefas**       | Acesso à tarefa            | Sucesso | Listagem e abertura funcionando                                  |
|                            | Adicionar texto            | Sucesso | Editor de texto funcional                                        |
|                            | Envio de tarefa            | Sucesso | Confirmação de envio recebida                                    |
|                            | Edição de envio            | Sucesso | Possível editar antes do prazo                                   |
|                            | Exclusão de envio          | Sucesso | Remoção de envio funcionando                                     |
| **Participação em Fóruns** | Acesso ao fórum            | Sucesso | Navegação entre fóruns funcionando                               |
|                            | Leitura de discussões      | Sucesso | Visualização completa das postagens                              |
|                            | Resposta a postagens       | Sucesso | Envio de respostas funcionando                                   |
|                            | Anexos                     | Sucesso | Anexar arquivos em respostas funcionando                         |
| **Acesso Offline**         | Download e acesso offline  | Sucesso | Conteúdos previamente baixados acessíveis sem conexão            |

---

### Cálculo da Métrica 1.2  

A Métrica 1.2 mede a **Taxa de Sucesso em Funcionalidades Essenciais no App Móvel**, considerando grupos de funcionalidades como login, visualização de conteúdos, envio de tarefas, participação em fóruns e acesso offline.

Para o cálculo, foram consideradas cinco categorias principais, cada uma com seu percentual de sucesso:

- Login: 100%, 1 de 1 funcionalidade bem-sucedida  
- Visualização de conteúdos: 85,7%, 6 de 7 itens, falha apenas no conteúdo H5P  
- Envio de tarefas: 100%, 5 de 5  
- Participação em fóruns: 100%, 4 de 4  
- Acesso offline: 100%, 1 de 1  

A Taxa de Sucesso global foi calculada como a média dos percentuais de cada categoria:

Taxa de Sucesso = soma dos percentuais por grupo dividida pelo número de grupos  

Taxa de Sucesso = (100% + 85,7% + 100% + 100% + 100%) dividido por 5  

Taxa de Sucesso ≈ **97,14%**

---

### Classificação segundo os Critérios da Fase 2  

| Faixa de Resultado | Classificação  |
| ------------------ | -------------- |
| Maior que 90%      | Excelente      |
| 75% a 90%          | Bom            |
| 60% a 74%          | Regular        |
| Menor que 60%      | Insatisfatório |

Com uma taxa de sucesso aproximada de **97,14%**, a classificação obtida pela Métrica 1.2 é **EXCELENTE**.

---

### Análise e Resposta à Questão GQM  

> **Q1, Em que medida o aplicativo oficial do Moodle permite que os discentes realizem, em ambiente móvel, as principais tarefas acadêmicas realizadas no Aprender 3 via navegador?**

Os resultados evidenciam que o app Moodle oferece suporte robusto à maior parte das tarefas essenciais do discente. O login com credenciais institucionais funciona sem problemas, o acesso às disciplinas é fluido e a visualização de documentos, como PDFs e áudios, ocorre de forma satisfatória. Além disso, o envio de tarefas, com inclusão, edição e exclusão de envios, é realizado com sucesso, assim como a participação em fóruns, leitura e resposta a postagens e anexos.

O único ponto crítico identificado foi o conteúdo H5P, que apresentou erro relacionado à configuração do site para uso móvel. Esse problema, embora relevante, não compromete a percepção geral de portabilidade, já que se trata de um tipo específico de recurso e não de uma funcionalidade básica do app.

Dessa forma, em resposta à Questão GQM 1, conclui-se que o aplicativo oficial do Moodle **suporta de maneira ampla e eficiente as principais funcionalidades acadêmicas** associadas ao Aprender 3, configurando-se como uma alternativa viável e de alta qualidade ao acesso via navegador.

---

### Avaliação da Hipótese H1.2  

> **H1.2, O app Moodle é uma alternativa viável ao uso via navegador, permitindo que as principais funcionalidades sejam executadas com sucesso no contexto móvel.**

Com uma taxa de sucesso global superior a 97% nas funcionalidades avaliadas, a hipótese H1.2 é **validada**. O app Moodle demonstrou capacidade de atender às necessidades essenciais do discente, incluindo autenticação, navegação por cursos, consumo de conteúdos, envio de tarefas, interação em fóruns e acesso offline.

Embora exista uma limitação pontual relacionada ao conteúdo H5P, o conjunto de evidências mostra que, no contexto geral, o aplicativo é plenamente funcional e oferece uma experiência de uso satisfatória no dispositivo móvel, fortalecendo a portabilidade da solução.

---

### Demonstração em Vídeo  

O vídeo a seguir ilustra a execução dos testes das funcionalidades essenciais no app Moodle, incluindo navegação pelos cursos, visualização de conteúdos e envio de atividades:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/-wHRkMZcDag"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## CT-POR-03: Verificação de Histórico de Migração, Aprender para Aprender 3

### Detalhamento do Caso de Teste  
**Questão GQM:** Q2, *Há evidências de que o Aprender 3 resulta de um processo de evolução e substituição bem-sucedida de versões anteriores, garantindo continuidade de serviço e preservação do contexto institucional?*  
**Métrica Associada:** 2.1, Verificação de Histórico de Migração  
**Hipótese Avaliada:** H2.1, *A migração e evolução entre versões do Aprender, por exemplo Aprender, Aprender 2 e Aprender 3, foi bem-sucedida, demonstrando capacidade de substituição e continuidade da plataforma.*  
**Perfil:** Equipe Técnica, Avaliação Documental  

---

### Resultados Obtidos  

A investigação se concentrou em **fontes oficiais da Universidade de Brasília**, incluindo comunicados do CEAD e notícias institucionais, com o objetivo de identificar evidências de evolução e substituição entre versões da plataforma Aprender.

#### Tabela de Fontes de Evidência  

| Fonte               | Acesso ou Publicação | URL ou Referência                                                                                                                            | Observações                                      |
| ------------------- | -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| **Comunicado CEAD** | Novembro de 2025     | *Ambientes Virtuais de Aprendizagem*                                                                                                         | Histórico resumido do Moodle na UnB desde 2004   |
| **Comunicado UnB**  | 03/08/2020           | *Descubra os ambientes disponíveis no Moodle para públicos diversos*                                                                         | Notícia oficial sobre diferenças entre ambientes |

A partir dessas e de outras referências, foi possível reconstruir uma linha do tempo da evolução dos ambientes Moodle na UnB.

#### Linha do Tempo Resumida  

- **2004:** Primeiro contato da UnB com o Moodle, inicialmente no Departamento de Matemática.  
- **2009:** O sistema passa a ser gerenciado pelo CEAD/UnB sob o nome "Aprender".  
- **2011:** A gestão é transferida para a UAB, DEGD.  
- **2018:** Junção do DEGD e CEAD/UnB, com o Aprender retornando à gestão do CEAD/UnB.  
- **Agosto de 2020:** Oficialização de três ambientes Moodle distintos, Aprender 1, Aprender 2 e Aprender 3, para públicos e finalidades diferentes.  
- **Atualmente, 2025:** Coexistência de Aprender 2 e Aprender 3, ambos na versão Moodle 3.11.  
- **Futuro próximo:** Planejamento de atualização para Moodle 4.0, com expectativa de melhoria na experiência de uso.

#### Diferenças entre Aprender 2 e Aprender 3  

A análise mostrou que **não houve uma migração direta única** entre Aprender 2 e Aprender 3, e sim a **configuração de ambientes paralelos** com finalidades distintas:

- **Aprender 2:**  
  - Foco em cursos de extensão.  
  - Público formado por alunos UAB/UnB e ações de formação vinculadas ao CEAD e UAB.  
  - Versão do Moodle: 3.11.  

- **Aprender 3:**  
  - Foco em graduação e pós-graduação.  
  - Público formado principalmente por alunos de cursos presenciais de graduação e pós-graduação.  
  - Versão do Moodle: 3.11.  

Apesar dessa separação por público, as fontes analisadas destacam a **continuidade da plataforma Moodle ao longo do tempo** e a evolução da infraestrutura para suportar públicos distintos, sempre mantendo a base tecnológica e pedagógica.

---

### Cálculo da Métrica 2.1  

A Métrica 2.1 é **qualitativa e binária**, indicando se há ou não evidência de migração e evolução bem-sucedida.

- Resultado da investigação: foram encontradas evidências claras de evolução e manutenção da plataforma Moodle na UnB, desde 2004 até o Aprender 3, com planejamento de futuras atualizações.  

Dessa forma, o valor atribuído à métrica é:

- **Sim**, foi encontrada evidência de histórico de migração e evolução bem-sucedida.

---

### Análise e Resposta à Questão GQM  

> **Q2, Há evidências de que o Aprender 3 resulta de um processo de evolução e substituição bem-sucedida de versões anteriores, garantindo continuidade de serviço e preservação do contexto institucional?**

Os documentos institucionais analisados apontam que o Aprender 3 não surgiu de forma isolada, mas sim como parte de um **processo contínuo de evolução** dos ambientes Moodle na UnB. Há registros desde a adoção inicial da plataforma em 2004, passando por mudanças de gestão, reestruturações e criação de ambientes específicos para diferentes públicos, até a configuração atual com Aprender 2 e Aprender 3 em operação.

Embora não haja um relato detalhado de uma única migração técnica entre Aprender 2 e Aprender 3, existe uma **trajetória clara de substituição e expansão de ambientes** que garante a continuidade dos serviços aos diversos públicos atendidos. Além disso, o planejamento de migração para o Moodle 4.0 reforça o caráter evolutivo da solução, indicando que a universidade mantém uma política ativa de atualização tecnológica.

Assim, em resposta à Questão GQM 2, conclui-se que há **evidências suficientes de evolução e substituição bem-sucedida da plataforma**, ainda que distribuídas em diferentes fases e ambientes, o que comprova a capacidade de portabilidade e adaptabilidade do Aprender 3 dentro do contexto institucional.

---

### Avaliação da Hipótese H2.1  

> **H2.1, A migração e evolução entre versões do Aprender, por exemplo Aprender, Aprender 2 e Aprender 3, foi bem-sucedida, demonstrando capacidade de substituição e continuidade da plataforma.**

Com base nas evidências coletadas, a hipótese H2.1 é **validada**. As informações mostram que a UnB mantém, há anos, um processo de evolução controlada dos ambientes Moodle, preservando dados, atendendo a diferentes públicos e planejando novas atualizações. Ainda que os ambientes coexistam em determinadas fases, isso faz parte de uma estratégia de transição gradual e segmentação por público, ao invés de uma migração abrupta e única.

Portanto, a trajetória histórica indica que a plataforma tem sido capaz de se **substituir e evoluir ao longo do tempo**, sem perda de continuidade acadêmica, o que está alinhado com a visão de portabilidade e substituibilidade prevista na hipótese.

<!-- CT-POR-04: Compatibilidade de Plugins e Temas na Atualização do Moodle

### Informações do Teste  

- **Questão GQM:** Q2, Substituibilidade  
- **Métrica Associada:** 2.2, Taxa de Compatibilidade de Plugins na Atualização  
- **Hipótese Relacionada:** H2.2, Natureza modular permite atualização de componentes  
- **Perfil Principal:** Equipe Técnica, Administração do Moodle  

### Ambiente de Teste  

- Acesso à lista completa de plugins e temas do Aprender 3.  
- Versão atual do Moodle e versão alvo de atualização.  
- Acesso ao diretório oficial de plugins do Moodle.  

### Testes Realizados  

O teste consistiu em verificar a compatibilidade de plugins e temas do Aprender 3 com a versão atual do Moodle e com a versão alvo de atualização, analisando o quanto a natureza modular da plataforma facilita esse processo.  

### Resultados dos Testes  

Os resultados mostraram que aproximadamente 90% dos plugins e temas do Aprender 3 são compatíveis com as versões consideradas, o que indica alto potencial de atualização sem grandes impedimentos técnicos.  

### Classificação da Métrica  

Diante da alta taxa de compatibilidade, a classificação obtida foi considerada **Excelente**. -->

---

## CT-POR-04: Sucesso na Configuração do App Moodle por Novos Usuários

### Detalhamento do Caso de Teste  
**Questão GQM:** Q3, *Quão difícil é para um novo usuário, sem experiência prévia com o aplicativo Moodle, instalar e configurar o app para acessar o Aprender 3?*  
**Métrica Associada:** 3.1, Taxa de Sucesso na Configuração do App por Novos Usuários  
**Hipótese Avaliada:** H3.1, *O processo de instalação e configuração do app Moodle é complexo para usuários não técnicos, gerando uma taxa significativa de insucesso sem apoio externo.*  
**Perfil:** Discentes sem experiência prévia com o app Moodle  

---

### Resultados Obtidos  

Foram selecionados **3 usuários de teste** sem experiência prévia com o aplicativo Moodle e que não são estudantes da UnB. Cada participante utilizou um **dispositivo móvel próprio**, Android ou iOS, e recebeu a seguinte instrução padronizada:

> "Instale o aplicativo Moodle no seu celular e acesse sua conta do Aprender 3, link https://aprender3.unb.br. Será fornecido usuário e senha de uma conta de estudante cadastrada previamente."

O objetivo foi verificar se os participantes conseguiriam realizar todo o processo **sem assistência técnica direta**.

Os resultados mostraram que **100% dos usuários conseguiram configurar o app Moodle com sucesso**, acessando o ambiente Aprender 3 de forma autônoma. Foram feitas gravações de tela durante o procedimento:

- Um vídeo em aparelho Android.  
- Um vídeo em aparelho iOS.  
- Um terceiro teste, também em iOS, com o mesmo resultado dos anteriores, não teve o vídeo incorporado por redundância, já que o comportamento foi praticamente idêntico.

---

### Cálculo da Métrica 3.1  

A Métrica 3.1 avalia a **Taxa de Sucesso na Configuração do App por Novos Usuários**, medindo a proporção de usuários que conseguem concluir todo o processo de configuração sem ajuda.

**Fórmula utilizada:**  
Taxa de Sucesso = (Número de usuários que configuraram com sucesso / Número total de usuários testados) x 100  

Aplicando os valores:

- Usuários bem-sucedidos: 3  
- Total de usuários testados: 3  

Taxa de Sucesso = 3 dividido por 3, multiplicado por 100, resultando em **100%**

Dado que todos os participantes, mesmo sem familiaridade prévia com o app ou com o ambiente institucional, concluíram a configuração com êxito, a métrica indica um nível máximo de instalabilidade no cenário testado.

---

### Análise e Resposta à Questão GQM  

> **Q3, Quão difícil é para um novo usuário, sem experiência prévia com o aplicativo Moodle, instalar e configurar o app para acessar o Aprender 3?**

Os resultados indicam que, no contexto analisado, o processo de instalação e configuração do app Moodle para acesso ao Aprender 3 é **bastante acessível**. Todos os usuários, mesmo sem serem estudantes da UnB e sem experiência anterior com o aplicativo, conseguiram concluir as etapas necessárias, localizando o app nas lojas oficiais, inserindo a URL correta do servidor e autenticando com as credenciais fornecidas.

A ausência de relatos de dificuldades graves, combinada com a taxa de sucesso de 100%, sugere que o fluxo de configuração é suficientemente claro e não exige conhecimentos técnicos avançados. Isso reforça a percepção de que a barreira de entrada para o uso do Aprender 3 via aplicativo móvel é baixa, o que é positivo do ponto de vista da portabilidade e da instalabilidade.

---

### Avaliação da Hipótese H3.1  

> **H3.1, O processo de instalação e configuração do app Moodle é complexo para usuários não técnicos, gerando uma taxa significativa de insucesso sem apoio externo.**

Os dados coletados **refutam a hipótese H3.1**. Em vez de uma taxa significativa de insucesso, o teste revelou que todos os participantes concluíram o processo com sucesso e sem necessidade de assistência técnica adicional. Isso contraria diretamente a suposição de que o procedimento seria complexo para usuários não técnicos.

Dessa forma, conclui-se que a hipótese é **não validada**, e que o processo de instalação e configuração do app Moodle, pelo menos nas condições testadas, pode ser considerado **simples e acessível**, contribuindo positivamente para a portabilidade do Aprender 3 em dispositivos móveis.

---

### Demonstração em Vídeo  

A seguir encontra-se o vídeo que registra a configuração do app Moodle por um dos usuários de teste, ilustrando o processo de instalação, configuração do servidor e acesso ao Aprender 3:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/CemC_KH0Jc0"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## CT-POR-05: Verificação de Dependências de Navegador, Navegador Limpo

### Detalhamento do Caso de Teste  
**Questão GQM:** Q3, *O uso básico do Aprender 3, via navegador, depende de plugins, extensões ou softwares adicionais, ou basta um navegador padrão, em estado limpo, para acessar as funcionalidades essenciais?*  
**Métrica Associada:** 3.2, Verificação de Dependências de Navegador  
**Hipótese Avaliada:** H3.2, *O Aprender 3 não exige a instalação de plugins ou extensões específicas no navegador para executar suas funcionalidades básicas, o que favorece a portabilidade.*  
**Perfil:** Equipe Técnica  

---

### Resultados Obtidos  

O teste foi realizado em um **navegador em estado limpo**, simulando a experiência de um navegador recém-instalado, utilizando uma guia anônima do Google Chrome sem extensões ativas ou dados de sessão. O objetivo foi verificar se o Aprender 3 solicita qualquer instalação adicional ou se funciona apenas com recursos nativos do navegador.

Durante o teste, foram executadas as funcionalidades previstas na Fase 3, incluindo:

- Acesso à página inicial do Aprender 3.  
- Login com usuário de teste.  
- Visualização da lista de disciplinas.  
- Abertura de um curso e navegação entre tópicos.  
- Visualização de um arquivo PDF simples.  
- Visualização da página de fórum.  
- Envio de uma tarefa com upload básico de arquivo.  

Em nenhuma dessas etapas foi apresentado pedido de instalação de plugins, extensões ou softwares adicionais, nem foram detectadas mensagens de erro relacionadas a dependências específicas.

---

### Cálculo da Métrica 3.2  

A Métrica 3.2 também é **qualitativa e binária**, verificando se há ou não dependências adicionais.

- Resultado do teste: todas as funcionalidades básicas puderam ser executadas no navegador limpo, sem necessidade de complementos.  

Portanto, o valor atribuído é:

- **Sim**, o Aprender 3 funciona corretamente em navegador padrão, sem exigir plugins adicionais.

Em termos de classificação, o sistema é considerado **Excelente, Portável**, pois não introduz requisitos extras que possam comprometer o uso em diferentes ambientes e dispositivos.

---

### Análise e Resposta à Questão GQM  

> **Q3, O uso básico do Aprender 3, via navegador, depende de plugins, extensões ou softwares adicionais, ou basta um navegador padrão, em estado limpo, para acessar as funcionalidades essenciais?**

Os resultados mostram que um navegador em estado limpo é suficiente para acessar e utilizar as funcionalidades básicas do Aprender 3. O fluxo de login, navegação por cursos, acesso a conteúdos, participação em fóruns e envio de tarefas ocorre sem que o sistema exija componentes externos, como plugins proprietários ou extensões específicas.

Do ponto de vista da portabilidade, isso significa que o Aprender 3 pode ser utilizado em diferentes máquinas e contextos apenas com navegadores padrões modernos, reduzindo a necessidade de suporte técnico e facilitando o acesso em laboratórios, computadores compartilhados e dispositivos pessoais.

---

### Avaliação da Hipótese H3.2  

> **H3.2, O Aprender 3 não exige a instalação de plugins ou extensões específicas no navegador para executar suas funcionalidades básicas, o que favorece a portabilidade.**

Os resultados **validam a hipótese H3.2**. Não foram detectadas dependências adicionais para as tarefas básicas avaliadas, o que confirma que a plataforma é projetada para operar com recursos nativos do navegador, alinhada às boas práticas de portabilidade e acessibilidade.

Esse comportamento reduz barreiras técnicas e reforça a capacidade do Aprender 3 de ser executado em ampla variedade de ambientes, incluindo máquinas institucionais com restrições de instalação de software.

---

### Demonstração em Vídeo  

O vídeo a seguir ilustra a execução do teste em navegador limpo, mostrando o acesso ao Aprender 3 e a utilização das funcionalidades básicas sem a necessidade de qualquer instalação adicional:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/GZV3IjGjVUo"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

## Resumo dos Resultados

### Métricas Avaliadas  

| Métrica       | Descrição                                                   | Resultado   | Classificação                        |
| ------------- | ----------------------------------------------------------- | ----------  | ------------------------------------ |
| **CT-POR-01** | Taxa de Conformidade de Layout Responsivo                   | 71,11%      | **Regular**                          |
| **CT-POR-02** | Taxa de Sucesso em Funcionalidades no App Móvel             | 97,14%      | **Excelente**                        |
| **CT-POR-03** | Verificação de Histórico de Migração                        | Sim         | **Hipótese H2.1 validada**          |
| **CT-POR-04** | Sucesso na Configuração do App Moodle por Novos Usuários    | 100%        | **Excelente**                        |
| **CT-POR-05** | Verificação de Dependências de Navegador, Navegador Limpo   | 100%        | **Excelente, Portável, Hipótese H3.2 validada** |

---

## Conclusão GQM da Dimensão Portabilidade

As métricas planejadas foram corretamente processadas e a comparação com as faixas de classificação da Fase 2 permitiu responder, de forma clara e completa, às três Questões GQM da dimensão Portabilidade.  
Assim, todos os Objetivos de Medição dessa dimensão foram devidamente atendidos.

---

## Histórico de Versões  

| Versão | Data       | Descrição                                               | Autor                                  |
| :----: | ---------- | ------------------------------------------------------- | -------------------------------------- |
| `1.0`  | 23/11/2025 | Criação da página e adição do CT-POR-02                 | [Yago Amin](https://github.com/yagoas) |
| `1.1`  | 23/11/2025 | Adição do CT-POR-03                                     | [Yago Amin](https://github.com/yagoas) |
| `1.2`  | 24/11/2025 | Adição do CT-POR-04 e CT-POR-05                         | [Felipe Hansen](https://github.com/FHansen98) |
| `1.3`  | 25/11/2025 | Adição do CT-POR-01                                     | [Patrick Anderson Carvalho dos Santos](http://github.com/patrickacs) |
| `1.4`  | 25/11/2025 | Adição dos vídeos dos testes CT-POR-04 e CT-POR-05     | [Felipe Hansen](https://github.com/FHansen98) |
