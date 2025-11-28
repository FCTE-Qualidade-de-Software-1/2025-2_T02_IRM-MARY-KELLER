# Fase 3 - Projetar a Avaliação

## Plano de Avaliação

Avaliar as características de **Portabilidade** e **Compatibilidade** da plataforma Aprender 3, com base no plano de medição GQM (Goal-Question-Metric) definido na Fase 2. O objetivo é executar a coleta de dados de forma sistemática, reproduzível e alinhada à ISO/IEC 25010 e 25023, identificando limitações de acesso em diferentes dispositivos e navegadores, problemas de interoperabilidade e falhas de integração com serviços externos, validando as hipóteses de portabilidade e compatibilidade formuladas anteriormente.

---

## 1. Método de Avaliação

Será utilizada uma abordagem baseada no plano GQM de Portabilidade e Compatibilidade. A coleta de dados combinará:

- **Testes funcionais manuais** em diferentes navegadores, resoluções e dispositivos.
- **Uso do aplicativo Moodle (Android/iOS)** para verificação da experiência móvel.
- **Inspeção de configuração e documentação** do Aprender 3 e do Moodle.
- **Observação de usuários de teste**, em cenários guiados.
- **Integração com serviços externos** (e-mail institucional, Google Calendar, Outlook).

A Tabela a seguir resume, para cada **dimensão**, as **questões GQM**, **métricas associadas**, as **fontes de dados** e um link para o respectivo **plano de coleta** detalhado em outra página.

| **Dimensão** | **Questão (GQM)** | **Métrica (GQM)** | **Ferramenta / Fonte de Dados** | **Plano de Coleta** |
| --- | --- | --- | --- | --- |
| **Compatibilidade** | Q1: Qual é a consistência dos dados do discente entre o Aprender 3 (Web) e o App Moodle? | **Métrica 1.1: Percentual de Discrepância de Status de Conclusão** | Conta de estudante de teste, curso de teste, acesso Web e App Moodle — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../compatibilidade/#ct-comp-01-sincronia-de-status-de-conclusao) |
| | | **Métrica 1.2: Taxa de Sucesso de Sincronização Bidirecional de Arquivos** | Área “Arquivos privados”, acesso Web e App, arquivos de teste — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../compatibilidade/#ct-comp-02-sincronizacao-bidirecional-de-arquivos) |
| **Compatibilidade** | Q2: Qual é a variação no consumo de recursos (CPU/RAM) do Aprender 3 entre diferentes navegadores? | **Métrica 2.1: Consumo Médio de RAM por Navegador** | Navegadores (Chrome, Firefox, Edge), gerenciador de tarefas — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../compatibilidade/#ct-comp-03-consumo-medio-de-ram-por-navegador) |
| **Compatibilidade** | Q3: Em que medida o discente recebe notificações por e-mail sobre novas postagens em fóruns de discussão subscritos? | **Métrica 3.1: Taxa de Falha de Entrega de Notificação** | Usuário de teste, fórum de teste, e-mail institucional, logs — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../compatibilidade/#ct-comp-04-entrega-de-notificacoes-de-forum-por-e-mail) |
| **Compatibilidade** | Q4: Em que medida o Aprender 3 permite a exportação para calendários externos? | **Métrica 4.1: Taxa de Falha de Subscrição de URL** | Interface de calendário, Google Calendar, Outlook Calendar — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../compatibilidade/#ct-comp-05-subscricao-de-calendario-via-url) |
| | | **Métrica 4.2: Diferencial de Sucesso (Importação Estática vs. Dinâmica)** | Mesmo ambiente da métrica 4.1, arquivo `.ics` — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../compatibilidade/#ct-comp-06-importacao-estatica-ics-vs-subscricao-dinamica-url) |
| **Compatibilidade** | Q5: Qual é a consistência da funcionalidade *drag-and-drop* entre os navegadores suportados? | **Métrica 5.1: Taxa de Sucesso de Drag-and-Drop (D&D)** | Navegadores (Chrome, Firefox, Edge), página de envio de tarefa — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../compatibilidade/#ct-comp-07-sucesso-da-funcionalidade-drag-and-drop-dd-por-navegador) |
| **Portabilidade** | Q1: A tecnologia usada no desenvolvimento do site garante funcionamento correto nos navegadores mais populares e dispositivos móveis? | **Métrica 1.1: Taxa de Conformidade de Layout Responsivo** | Navegadores (Chrome, Firefox, Edge), Desktop/Tablet/Smartphone — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../portabilidade/#ct-por-01-conformidade-de-layout-responsivo-web-desktop-tablet-e-smartphone) |
| | | **Métrica 1.2: Taxa de Sucesso em Funcionalidades no App Móvel** | App Moodle (Android), conta de teste — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../portabilidade/#ct-por-02-sucesso-em-funcionalidades-essenciais-no-app-moodle) |
| **Portabilidade** | Q2: A arquitetura do Aprender 3 facilita migração de dados e atualização de componentes? | **Métrica 2.1: Verificação de Histórico de Migração** | Comunicados UnB e CEAD, notas técnicas, documentação — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../portabilidade/#ct-por-03-verificacao-de-historico-de-migracao-aprender-2-aprender-3) |
| **Portabilidade** | Q3: O acesso via app ou navegador pode ser configurado sem conhecimentos técnicos avançados? | **Métrica 3.1: Taxa de Sucesso na Configuração do App** | Usuários de teste, App Moodle — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../portabilidade/#ct-por-05-sucesso-na-configuracao-do-app-moodle-por-novos-usuarios) |
| | | **Métrica 3.2: Verificação de Dependências de Navegador** | Navegadores padrão (Chrome, Firefox, Edge) — [Ver detalhes](../ferramentas) | [Ver plano de coleta](../portabilidade/#ct-por-06-verificacao-de-dependencias-de-navegador-navegador-limpo) |
