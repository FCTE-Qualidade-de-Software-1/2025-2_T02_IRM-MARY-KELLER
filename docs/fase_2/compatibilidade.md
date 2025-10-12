## Objetivo de Medição 2: Compatibilidade

**Tabela 2** - Objetivo de Medição 2: Compatibilidade.

| Analisar | Descrição |
| :--- | :--- |
| **Para o propósito de** | Caracterizar o nível de **compatibilidade** (incluindo interoperabilidade e coexistência) do **Aprender 3** com diversos ambientes de operação e outros sistemas essenciais. |
| **Com respeito a** | A funcionalidade do sistema e a troca de informações em navegadores, dispositivos móveis e a coexistência entre o acesso via Web e via aplicativo Moodle. |
| **Do ponto de vista da** | **Comunidade acadêmica (professores e estudantes)**, que depende de uma experiência fluida e integrada em múltiplas plataformas. |
| **No contexto da** | **Operação em produção** do ambiente virtual de aprendizagem (`https://aprender3.unb.br/`) durante o semestre letivo. |

---

### Perguntas e Hipóteses de Medição

**Questão 1: Em que medida o Aprender 3 demonstra interoperabilidade com os navegadores web mais utilizados pela comunidade?**
> Qual é a taxa de sucesso das interações-chave do usuário em navegadores *mainstream* e em navegadores secundários ou desatualizados?

* **Hipótese 1.1 (H1.1):** A taxa de sucesso em funcionalidades de interface (e.g., edição de texto, *drag-and-drop*) será menor em navegadores que não estejam na versão *N* ou *N-1* (onde *N* é a versão mais recente).

**Questão 2: Qual o grau de adaptabilidade do Aprender 3 a diferentes tamanhos e tipos de dispositivos móveis?**
> A experiência do usuário, em termos de eficiência e eficácia, é mantida ao acessar o sistema em *smartphones* e *tablets* (via *browser* ou aplicativo)?

* **Hipótese 2.1 (H2.1):** Tarefas que envolvem o envio de documentos (e.g., submissão de trabalhos) exigem um **número significativamente maior de cliques ou interações** em telas pequenas (*smartphones*) comparadas a *desktops*, indicando menor eficiência.
* **Hipótese 2.2 (H2.2):** A **proporção de tempo gasto** por usuário na plataforma via *desktop* é significativamente maior do que via celular, indicando que os usuários preferem (ou necessitam) da tela maior para atividades essenciais.

**Questão 3: O Aprender 3 coexiste eficientemente entre seus diferentes pontos de acesso (Web e Aplicativo Moodle) e em sistemas operacionais de uso geral (Windows, Linux, macOS)?**
> A consistência de conteúdo entre a interface Web e o aplicativo Moodle (Coexistência) e o desempenho sob diferentes sistemas operacionais (Coexistência) são adequados?

* **Hipótese 3.1 (H3.1):** A **proporção de cursos** que apresentam uma diferença na contagem de atividades e recursos entre o aplicativo Moodle e a interface Web do Aprender 3 é inferior a 1%, garantindo a **Coexistência** de conteúdo.
* **Hipótese 3.2 (H3.2):** O **Consumo de Recursos (CPU/RAM)** do navegador ao rodar o Aprender 3 não varia significativamente entre os principais Sistemas Operacionais de uso geral (Coexistência).

---

### Seleção das Métricas

**Questão 1: Em que medida o Aprender 3 demonstra interoperabilidade com os navegadores web mais utilizados pela comunidade?**

* **Métrica 1.1: Índice de Conformidade de Navegador (ICN)**
    * **Definição:** Porcentagem de funcionalidades críticas que passam nos testes automatizados ou manuais de compatibilidade (Testes de Regressão) em uma suíte predefinida de navegadores/versões.
    * **Fórmula:** ICN = (Funcionalidades Aprovadas / Total de Funcionalidades Testadas) x 100
    * **Coleta:** Resultados de ferramentas de automação de testes *cross-browser* ou relatórios de *QA*.
    * **Propósito:** Medir a **Interoperabilidade** do *front-end* com diferentes implementações de padrões web.

**Questão 2: Qual o grau de adaptabilidade do Aprender 3 a diferentes tamanhos e tipos de dispositivos móveis?**

* **Métrica 2.1: Índice de Esforço de Interação (IEI)**
    * **Definição:** Razão entre o número médio de cliques (ou toques) necessários para completar uma tarefa padrão (e.g., enviar um documento) em dispositivos móveis versus desktops.
    * **Fórmula:** IEI = (Média de Cliques no Dispositivo Móvel) / (Média de Cliques no Desktop)
    * **Coleta:** Ferramentas de análise de produto (*product analytics*) que rastreiam eventos de clique em funis de tarefas predefinidos, segmentados por tipo de dispositivo.
    * **Propósito:** Medir a **eficiência da interface** e o esforço do usuário (ligados à Adaptabilidade) em diferentes formatos de tela. Um índice maior que 1 indica maior esforço no ambiente móvel.

* **Métrica 2.2: Tempo para Conclusão de Tarefa em Diferentes Fatores de Forma (TCT-FF)**
    * **Definição:** Tempo médio gasto pelos usuários para completar uma tarefa padrão (e.g., visualizar notas ou responder a um fórum) em *desktop* vs. *smartphone*.
    * **Fórmula:** TCT-FF = (Tempo Médio no Smartphone) / (Tempo Médio no Desktop)
    * **Coleta:** Logs de interação do usuário ou estudos de usabilidade cronometrados.
    * **Propósito:** Medir a **Eficiência de Operação** (ligada à Adaptabilidade) em diferentes formatos de tela.

**Questão 3: O Aprender 3 coexiste eficientemente entre seus diferentes pontos de acesso e em sistemas operacionais de uso geral?**

* **Métrica 3.1: Taxa de Discrepância de Conteúdo (TDC)**
    * **Definição:** Proporção de cursos amostrados onde a contagem total de atividades e recursos visíveis na interface Web difere da contagem total no aplicativo Moodle.
    * **Fórmula:** TDC = (Cursos com Contagem de Atividades Diferente / Total de Cursos Amostrados)
    * **Coleta:** Testes automatizados ou manuais de comparação de *endpoint* (Web vs. App) para uma amostra de cursos.
    * **Propósito:** Medir a **Coexistência** (consistência de dados) entre o acesso Web e o aplicativo móvel.

* **Métrica 3.2: Variação no Uso de Recursos (VUR) por Sistema Operacional (SO)**
    * **Definição:** Desvio padrão do consumo de CPU e Memória (RAM) do *browser* ao rodar o Aprender 3, agrupado por Sistema Operacional. (Uma variação baixa indica melhor coexistência).
    * **Fórmula:** VUR = Desvio Padrão (Uso de Recursos) por SO
    * **Coleta:** Testes de desempenho em ambiente controlado.
    * **Propósito:** Medir a **Coexistência** e a estabilidade da carga de recursos em diferentes S.O.s.
