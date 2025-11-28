## Evidências e Dados Brutos da Execução

Todos os dados coletados durante a execução dos testes, como: tabelas de medições, capturas de tela, registros observados e vídeos completos dos testes. Estão disponibilizados de forma organizada e rastreável.  
Cada caso de teste contém:

- **tabelas de dados brutos**, diretamente utilizadas no cálculo das métricas;
- **vídeo**, servindo como comprovação visual da coleta;  
- **texto de referência cruzada** entre métrica, questão GQM;

A rastreabilidade é direta: cada métrica possui dados brutos claramente identificados, o cálculo da métrica correspondente, e a classificação produzida conforme os critérios definidos na Fase 2.

## Resumo dos Resultados de Compatibilidade

A Tabela a seguir resume, para cada **caso de teste de Compatibilidade**, a **questão GQM**, **métrica**, **resultado numérico**, **classificação** e a situação da **hipótese**.

| **Dimensão**      | **CT / Questão (GQM)**   | **Métrica (GQM)**    | **Resultado da Métrica**     | **Classificação / Hipótese**            | **Seção de Resultados** |
|-------------------|----------------------|--------------------------------------------|-----------------|------------------------------------------|--------------------------|
| **Compatibilidade** | CT-COMP-01 – Q1: Consistência dos dados Web × App                                   | Métrica 1.1: Percentual de Discrepância de Status de Conclusão           | 0 discrepâncias em 10 atividades (0%)                          | **Excelente**; H1.1 (*inconsistência Web × App*) **refutada** | [Ver resultados](../compatibilidade/#ct-comp-01-sincronia-de-status-de-conclusao) |
| **Compatibilidade** | CT-COMP-02 – Q1: Consistência dos dados Web × App                                   | Métrica 1.2: Taxa de Sucesso de Sincronização Bidirecional de Arquivos   | 2/2 sincronizações bem-sucedidas (100%)                        | **Excelente**; H1.2 (*falhas em “Arquivos privados”*) **refutada** | [Ver resultados](../compatibilidade/#ct-comp-02-sincronizacao-bidirecional-de-arquivos) |
| **Compatibilidade** | CT-COMP-03 – Q2: Variação de consumo de RAM entre navegadores                       | Métrica 2.1: Consumo Médio de RAM por Navegador                          | Variação máxima ≈ 76,69% (Edge vs. Chrome)                     | **Insatisfatório**; H2.1 (*um navegador consome bem mais RAM*) **validada** | [Ver resultados](../compatibilidade/#ct-comp-03-consumo-medio-de-ram-por-navegador) |
| **Compatibilidade** | CT-COMP-04 – Q3: Entrega de notificações de fórum por e-mail                        | Métrica 3.1: Taxa de Falha de Entrega de Notificação                     | 0 falhas em 4 notificações (0% de falha)                       | **Excelente**; H3.1 (*discente não recebe e-mails*) **refutada** | [Ver resultados](../compatibilidade/#ct-comp-04-entrega-de-notificacoes-de-forum-por-e-mail) |
| **Compatibilidade** | CT-COMP-05 – Q4: Exportação para calendários externos (subscrição via URL)          | Métrica 4.1: Taxa de Falha de Subscrição de URL                          | 1 falha em 6 serviços (≈16,7% de falha)                        | **Parcial**; H4.1 (*Google/Outlook falham via URL*) **refutada** | [Ver resultados](../compatibilidade/#ct-comp-05-subscricao-de-calendario-via-url) |
| **Compatibilidade** | CT-COMP-06 – Q4: Exportação estática (.ics) vs dinâmica (URL)                       | Métrica 4.2: Diferencial de Sucesso (Importação Estática vs Dinâmica)    | URL: 71,43%; ICS: 100%; diferencial = 28,57 p.p.               | **Hipótese H4.2 validada** (ICS funciona melhor que URL)      | [Ver resultados](../compatibilidade/#ct-comp-06-importacao-estatica-ics-vs-subscricao-dinamica-url) |
| **Compatibilidade** | CT-COMP-07 – Q5: Sucesso da funcionalidade drag-and-drop por navegador              | Métrica 5.1: Taxa de Sucesso de Drag-and-Drop (D&D) por Navegador        | Chrome: 90%; Firefox: 100%; Edge: 90%                          | **Bom (Chrome/Edge)** / **Excelente (Firefox)**; H5.1 **confirmada** | [Ver resultados](../compatibilidade/#ct-comp-07-sucesso-da-funcionalidade-drag-and-drop-dd-por-navegador) |

Os resultados de Compatibilidade mostram que o Aprender 3 apresenta desempenho sólido em quase todos os cenários avaliados, com exceções pontuais. No caso **CT-COMP-01**, a sincronização do status de conclusão entre Web e App foi perfeita: não houve discrepâncias em nenhuma das 10 atividades avaliadas, classificando a métrica como **Excelente** e refutando totalmente a hipótese de inconsistência. Da mesma forma, no **CT-COMP-02**, a sincronização bidirecional de arquivos também obteve **100% de sucesso**, demonstrando funcionamento consistente da área “Arquivos privados” e refutando a hipótese de falhas nesse processo.

O **CT-COMP-03**, por outro lado, revelou uma limitação importante: a variação de consumo de RAM entre navegadores chegou a aproximadamente **76,69%**, especialmente no Edge, o que classificou a métrica como **Insatisfatória**. Esse resultado confirma a hipótese de que um dos navegadores consome significativamente mais memória, indicando um problema de compatibilidade de desempenho.

No **CT-COMP-04**, avaliando notificações de fórum por e-mail, o desempenho foi impecável: todas as 4 notificações foram entregues corretamente, resultando em classificação **Excelente** e refutando a hipótese de falha no recebimento de e-mails. Resultados positivos também apareceram no **CT-COMP-05**, onde a integração via URL com calendários externos funcionou em 5 dos 6 serviços. Apesar da falha isolada no Yahoo Calendar, a métrica recebe classificação **Parcial**, e a hipótese de que Google e Outlook falhariam foi refutada.

O **CT-COMP-06** comparou a exportação dinâmica (URL) com a exportação estática (.ics) e identificou um diferencial de **28,57 p.p.**, com desempenho muito superior do método .ics. Esse achado confirma a hipótese de que a importação estática é mais confiável que a subscrição via URL. Por fim, o **CT-COMP-07** avaliou a funcionalidade de *drag-and-drop*: Firefox atingiu **100%**, enquanto Chrome e Edge registraram **90%**. Assim, a métrica foi classificada como **Excelente/Bom**, confirmando a hipótese de alta taxa de sucesso nos navegadores modernos.

Em conjunto, os resultados mostram que o Aprender 3 é amplamente compatível entre plataformas e funcionalidades essenciais, com limitações técnicas específicas em consumo de RAM e subscrição dinâmica de calendários.

---

## Resumo dos Resultados de Portabilidade

A Tabela a seguir resume, para cada **caso de teste de Portabilidade**, a **questão GQM**, **métrica**, **resultado**, **classificação** e a situação da **hipótese**.

| **Dimensão**    | **CT / Questão (GQM)**     | **Métrica (GQM)**    | **Resultado da Métrica**   | **Classificação / Hipótese**   | **Seção de Resultados** |
|-----------------|---------------------------------|-----------------------------------|-----------------------|---------------------------------------|--------------------------|
| **Portabilidade** | CT-POR-01 – Q1: Funcionamento correto em navegadores e dispositivos móveis                           | Métrica 1.1: Taxa de Conformidade de Layout Responsivo              | 32/45 combinações conformes (71,11%)                          | **Regular**; H1.1 (*layout se ajusta adequadamente em todos os dispositivos*) **refutada** | [Ver resultados](../portabilidade/#ct-por-01-conformidade-de-layout-responsivo-web--desktop-tablet-e-smartphone) |
| **Portabilidade** | CT-POR-02 – Q1: Sucesso em funcionalidades no App Moodle                                              | Métrica 1.2: Taxa de Sucesso em Funcionalidades no App Móvel        | Taxa média de sucesso ≈ 97,14%                                | **Excelente**; H1.2 (*app é alternativa viável ao navegador*) **validada**       | [Ver resultados](../portabilidade/#ct-por-02-sucesso-em-funcionalidades-essenciais-no-app-moodle) |
| **Portabilidade** | CT-POR-03 – Q2: Facilidade de migração/evolução da plataforma                                        | Métrica 2.1: Verificação de Histórico de Migração                   | Evidência de evolução e substituição bem-sucedida (linha do tempo CEAD/UnB) | **Sim (evidência encontrada)**; H2.1 **validada**                                | [Ver resultados](../portabilidade/#ct-por-03-verificacao-de-historico-de-migracao-aprender-para-aprender-3) |
| **Portabilidade** | CT-POR-04 – Q2: Compatibilidade de plugins e temas na atualização do Moodle                          | Métrica 2.2: Taxa de Compatibilidade de Plugins na Atualização      | 100% dos plugins/temas considerados compatíveis               | **Excelente**; H2.2 (*natureza modular permite atualização de componentes*) **validada** | *(seção de plugins, quando inserida)* |
| **Portabilidade** | CT-POR-04 (execução prática) – Q3: Configuração do App Moodle por novos usuários                     | Métrica 3.1: Taxa de Sucesso na Configuração do App por Novos Usuários | 3/3 usuários configuraram com sucesso (100%)                  | **Excelente**; H3.1 (*configuração é complexa para usuários não técnicos*) **refutada** | [Ver resultados](../portabilidade/#ct-por-04-sucesso-na-configuracao-do-app-moodle-por-novos-usuarios) |
| **Portabilidade** | CT-POR-05 – Q3: Dependências de navegador para funcionamento básico (navegador “limpo”)              | Métrica 3.2: Verificação de Dependências de Navegador               | Nenhum plugin/extensão adicional necessário                   | **Excelente (Portável)**; H3.2 (*não exige instalação de plugins específicos*) **validada** | [Ver resultados](../portabilidade/#ct-por-05-verificacao-de-dependencias-de-navegador-navegador-limpo) |

Os resultados de Portabilidade revelam uma distinção clara entre os testes de interface Web e o desempenho do aplicativo móvel. No **CT-POR-01**, que avaliou a conformidade do layout responsivo em diferentes resoluções e navegadores, apenas **71,11%** das combinações foram consideradas conformes. Esse percentual classifica a métrica como **Regular** e refuta a hipótese de que o layout se ajustaria adequadamente em todos os dispositivos. O principal problema identificado refere-se ao mau desempenho da interface em tablets e smartphones.

Em contraste, o **CT-POR-02** demonstrou que o aplicativo Moodle apresenta excelente portabilidade, com uma taxa média de sucesso nas funcionalidades avaliadas de **97,14%**, validando a hipótese de que o app é uma alternativa viável ao acesso por navegador. No **CT-POR-03**, verificou-se evidência documental consistente de evolução e substituição da plataforma ao longo do tempo, validando a hipótese de migração bem-sucedida e capacidade de evolução tecnológica.

O **CT-POR-04** também apresentou resultados amplamente positivos: todos os plugins e temas analisados foram considerados compatíveis com a versão-alvo de atualização do Moodle, classificando a métrica como **Excelente** e validando a hipótese de modularidade. Na execução prática do mesmo caso de teste (configuração do app Moodle por novos usuários), os três participantes conseguiram completar o processo sem dificuldades, resultando em **100% de sucesso** e refutando a hipótese de que a configuração seria complexa.

Finalmente, no **CT-POR-05**, a verificação de dependências de navegador confirmou que o Aprender 3 funciona plenamente em um navegador “limpo”, sem necessidade de extensões adicionais, o que classifica a métrica como **Excelente (Portável)** e valida a hipótese correspondente.

De forma geral, os testes de Portabilidade indicam que a maior fragilidade do Aprender 3 encontra-se no layout responsivo da versão Web, enquanto o aplicativo Moodle e a arquitetura modular demonstram alta maturidade e excelente capacidade de adaptação a diferentes ambientes e usuários.

---

## Recomendações e Ações de Melhoria

Com base nas métricas calculadas e nas respostas às Questões GQM, foram identificadas oportunidades de melhoria diretamente relacionadas às características de Compatibilidade e Portabilidade avaliadas:

### 1. Otimizar o desempenho em navegadores (CT-COMP-03)
A grande variação de consumo de RAM entre navegadores indica necessidade de:

- Revisar elementos de interface que causem maior overhead em navegadores específicos (Edge e Firefox);
- Avaliar possíveis otimizações no tema instalado no Aprender 3;
- Executar testes de desativação de plugins que possam impactar desempenho.

### 2. Melhorar a responsividade do layout em tablets e smartphones (CT-POR-01)
Os problemas encontrados apontam para:

- Ajuste no CSS responsivo do tema atual;
- Configuração para colapso automático de blocos laterais em resoluções menores;
- Revisão da renderização de tabelas em fóruns e no calendário;
- Revisão de estilos de imagens para impedir overflow horizontal.

### 3. Revisar o mecanismo de subscrição dinâmica por URL (CT-COMP-05 e CT-COMP-06)
A inconsistência no suporte entre serviços sugere:

- Revisão do endpoint iCal gerado pelo Aprender 3;
- Testes de validação do feed em validadores externos (RFC 5545);
- Investigação de caching ou atraso de atualização no servidor.

### 4. Corrigir suporte ao conteúdo H5P no App Moodle (CT-POR-02)
- Verificar configuração da opção “Mobile H5P Support” no servidor Moodle;
- Validar permissões do plugin H5P nas APIs móveis.

Essas ações derivam diretamente dos resultados medidos nesta Fase 4 e oferecem ao requisitante um conjunto de decisões concretas para melhorar Compatibilidade e Portabilidade do Aprender 3.

---

## Relação com o Propósito da Avaliação (Fase 1)

Os resultados obtidos nesta Fase 4 estão diretamente alinhados ao propósito estabelecido na Fase 1, cujo foco é a avaliação das características de **Compatibilidade** e **Portabilidade** do Aprender 3.  
As medições realizadas, as respostas às Questões GQM e o julgamento das hipóteses forneceram evidências concretas sobre o desempenho da plataforma nessas duas características, permitindo que o requisitante compreenda de forma objetiva como essas dimensões se manifestam no uso real do sistema.  
Dessa forma, o julgamento final apresentado nesta fase atende totalmente ao propósito e ao uso pretendido definidos no escopo do projeto.
