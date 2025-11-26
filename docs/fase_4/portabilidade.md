# Resultados dos Testes de Portabilidade

Esta seção descreve os testes realizados e resultados obtidos com base nos **Casos de Teste (CTs)** projetados para avaliar a característica de **Portabilidade** do Aprender 3, conforme planejamento realizado na Fase 3.

---

## CT-POR-01: Conformidade de Layout Responsivo (Web – Desktop, Tablet e Smartphone)

### Informações do Teste
- **Métrica:** 1.1 - Conformidade de Layout Responsivo
- **Objetivo:** Verificar se as páginas mantêm layout funcional em diferentes resoluções.
- **Hipótese:** H1.1: O layout responsivo se ajusta adequadamente em desktop, tablet e smartphone.

### Ambiente de Teste
- **Resoluções Testadas:**
    - Desktop: 1920x1080px
    - Tablet: 768x1024px
    - Smartphone: 375x667px
- **Páginas Avaliadas:** Página de Login, Página Inicial do Curso, Visualização de Tópico, Fórum - Lista de Discussões, Calendário.
- **Método:** Teste via Inspecionar Elemento (Device Toolbar) em 3 navegadores.

### Testes Realizados

O video da execução do teste está disponível a seguir:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/e6U-lpBli9U"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

### Resultados dos Testes

#### Resultados por Resolução

**Desktop (1920x1080px):**
- **Conformidade:** 15/15 (100%)
- Todas as páginas funcionaram perfeitamente.

**Tablet (768x1024px):**
- **Conformidade:** 11/15 (73,33%)
- **Não conformidades:**
    - Página Inicial (Chrome): Blocos laterais sobrepostos ao conteúdo.
    - Fórum (Firefox): Imagens de avatar colapsadas, texto sobreposto.
    - Fórum (Edge): Tabela não responsiva, informações cortadas.
    - Calendário (Edge): Eventos com texto cortado.

**Smartphone (375x667px):**
- **Conformidade:** 6/15 (40%)
- **Não conformidades:**
    - Página Inicial (todos navegadores): Blocos laterais não colapsam, scroll horizontal necessário.
    - Visualização de Tópico (Chrome, Edge): Imagens excedem largura da tela.
    - Fórum (todos navegadores): Tabela não responsiva, colunas sobrepostas, avatares distorcidos.
    - Calendário (Chrome, Firefox): Grade completamente ilegível, eventos não clicáveis.

#### Resultados Consolidados

- **Total de Combinações:** 45
- **Conformes:** 32
- **Não Conformes:** 13
- **Taxa de Conformidade Geral:** 71,11%

#### Análise por Navegador

| Navegador | Conformidade | Classificação |
| :--- | :--- | :--- |
| Chrome | 11/15 (73,33%) | Regular |
| Firefox | 11/15 (73,33%) | Regular |
| Edge | 10/15 (66,67%) | Regular |

### Problemas Principais Identificados

1. **Página Inicial - Mobile:** Blocos laterais não colapsam, conteúdo empurrado, scroll horizontal, menu não converte.
2. **Fórum - Mobile/Tablet:** Tabela não responsiva, avatares distorcidos, imagens excedem viewport, sobreposição de texto.
3. **Calendário - Mobile/Tablet:** Grade não responsiva, eventos cortados, navegação difícil, área de clique pequena.
4. **Visualização de Tópico - Mobile:** Imagens não ajustam à largura, scroll horizontal, colapso de textos.
5. **Página Inicial - Tablet Edge:** Blocos laterais sobrepõem conteúdo.

### Classificação da Métrica 1.1

Critérios (ISO/IEC 25010):
- 90%: Excelente
- 75-90%: Bom
- 60-74%: Regular
- < 60%: Insatisfatório

**Resultado: 71,11% - REGULAR**

### Validação da Hipótese

**H1.1: REFUTADA**

O layout se ajusta adequadamente apenas em desktop (100%). Em tablet apresentou conformidade regular (73,33%) e em smartphone foi insatisfatória (40%). A plataforma não atende adequadamente aos requisitos de responsividade, especialmente para dispositivos móveis, onde imagens e textos colapsam ou se sobrepõem frequentemente.

---

## CT-POR-02: Sucesso em Funcionalidades Essenciais no App Moodle

### Ambiente de Teste

- **Dispositivo:** Pixel 9 Pro (Emulado)
- **Sistema Operacional:** Android 16.0 ("Baklava")
- **Versão do App Moodle:** 5.0.0 (atualizado em 27/06/2025)
- **Conexão:** Dados móveis (emulado)

### Testes Realizados

O video da execução do teste está disponível a seguir:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/-wHRkMZcDag"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

### Resultados dos Testes

| Categoria                  | Funcionalidade/Item       | Status  | Observações                                                      |
| -------------------------- | ------------------------- | ------- | ---------------------------------------------------------------- |
| **Login e Autenticação**   | Login completo            | Sucesso | Autenticação com credenciais institucionais funcionou plenamente |
| **Visualização**           | Cursos                    | Sucesso | Listagem e acesso aos cursos funcionando                         |
|                            | PDF                       | Sucesso | Visualização e download funcionando                              |
|                            | Áudio                     | Sucesso | Reprodução funcionando                                           |
|                            | Link externo              | Sucesso | Abertura em navegador funcionando                                |
|                            | Notas                     | Sucesso | Notas exibidas corretamente                                      |
|                            | Notificações e mensagens  | Sucesso | Acesso e leitura funcionando                                     |
|                            | Conteúdo H5P              | Falha   | Erro: "Site not configured properly for mobile H5P content"      |
| **Envio de Tarefas**       | Acesso à tarefa           | Sucesso | Listagem e abertura funcionando                                  |
|                            | Adicionar texto           | Sucesso | Editor de texto funcional                                        |
|                            | Envio de tarefa           | Sucesso | Confirmação de envio recebida                                    |
|                            | Edição de envio           | Sucesso | Possível editar antes do prazo                                   |
|                            | Exclusão de envio         | Sucesso | Remoção de envio funcionando                                     |
| **Participação em Fóruns** | Acesso ao fórum           | Sucesso | Navegação entre fóruns funcionando                               |
|                            | Leitura de discussões     | Sucesso | Visualização completa das postagens                              |
|                            | Resposta a postagens      | Sucesso | Envio de respostas funcionando                                   |
|                            | Anexos                    | Sucesso | Anexar arquivos em respostas OK                                  |
| **Acesso Offline**         | Download e acesso offline | Sucesso | Conteúdos previamente baixados acessíveis sem conexão            |

---

### Cálculo da Métrica 1.2

| Funcionalidade            | Status  | Considerada no Cálculo |
| ------------------------- | ------- | ---------------------- |
| Login e Autenticação      | Sucesso | Sim                    |
| Visualização de Conteúdos | Parcial | Sim                    |
| Envio de Tarefas          | Sucesso | Sim                    |
| Participação em Fóruns    | Sucesso | Sim                    |
| Acesso Offline            | Sucesso | Sim                    |

Total de Funcionalidades Testadas: **5**

### Taxa de Sucesso

- **Login:** 100% (1/1)
- **Visualização de Conteúdos:** 85,7% (6/7)
- **Envio de Tarefas:** 100% (5/5)
- **Fóruns:** 100% (4/4)
- **Acesso Offline:** 100% (1/1)

```
Taxa de Sucesso = (100% + 85,7% + 100% + 100% + 100%) ÷ 5 = 97,14%
```

---

### Classificação da Métrica 1.1

Conforme critérios definidos na Fase 2:

| Faixa de Resultado | Classificação  |
| ------------------ | -------------- |
| **> 90%**          | **Excelente**  |
| 75% a 90%          | Bom            |
| 60% a 74%          | Regular        |
| < 60%              | Insatisfatório |

Classificação Obtida: **Excelente**

---

### Validação da Hipótese

**H1.2: VALIDADA**

O acesso via aplicativo oficial do Moodle é uma alternativa viável e funcional ao navegador, ampliando a portabilidade para o ecossistema móvel.

---

## CT-POR-03: Verificação de Histórico de Migração

### Resultados da Pesquisa

**Tabela de Fontes de Evidência**

| Fonte               | Acesso/Publicação | URL/Referência                                                                                                                            | Observações                                      |
| ------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| **Comunicado CEAD** | Novembro de 2025  | [Ambientes Virtuais de Aprendizagem](https://cead.unb.br/ambientes-virtuais-de-aprendizagem/)                                             | Histórico resumido do Moodle na UnB desde 2004   |
| **Comunicado UnB**  | 03/08/2020        | [Ambientes disponíveis no Moodle](https://noticias.unb.br/ensino/4340-descubra-os-ambientes-disponiveis-no-moodle-para-publicos-diversos) | Notícia oficial sobre diferenças entre ambientes |

---

### Análise dos Resultados

**Linha do Tempo da Evolução do Moodle na UnB**

- **2004:** Primeiro contato da UnB com Moodle (Departamento de Matemática)

- **2009:** Sistema passa a ser gerenciado pelo CEAD/UnB com o nome "Aprender"

- **2011:** Gestão transferida para UAB (DEGD)

- **2018:** Junção do DEGD e CEAD/UnB, Aprender retorna à gestão do CEAD/UnB

- **agosto de 2020:** Oficialização dos três ambientes Moodle distintos

- **Atualmente (2025):** Coexistem Aprender 2 e Aprender 3, ambos na versão Moodle 3.11

- **Futuro:** Planejada atualização para Moodle 4.0

**Diferenças entre Aprender 2 e Aprender 3**

A pesquisa revelou que **não houve uma migração** entre o aprender 2 e 3, mas sim a **criação de ambientes paralelos** para atender públicos distintos:

**Aprender 2:**

- **Foco:** Cursos de extensão
- **Público:** Alunos UAB/UnB e ações de formação pelo CEAD e UAB
- **Versão:** Moodle 3.11

**Aprender 3:**

- **Foco:** Graduação e pós-graduação
- **Público:** Alunos dos cursos presenciais de graduação e pós-graduação
- **Versão:** Moodle 3.11

**Migração do Aprender para o Aprender 3**

Embora não tenha sido identificada nenhuma documentação sobre a migração entre as diferentes versões do Aprender, há evidências de que a plataforma evoluiu, demonstrando a capacidade de substituição e adaptação ao longo do tempo.

A diretora do CEAD em 2020, Letícia Leite, confirma essa evolução: "Cada uma das plataformas é adequada a um público. Por exemplo: no Aprender 1, nós temos cursos que haviam iniciado em 2020/1 no Moodle, antes da suspensão do calendário acadêmico. Alguns professores estavam usando o Moodle no início do semestre. Outros já tinham as suas disciplinas no ambiente e gostariam de manter por mais um tempo essas informações, para que mais adiante eles consigam migrar esses dados. Ainda, é a plataforma usada por diversos cursos de extensão". [[Referência](https://noticias.unb.br/ensino/4340-descubra-os-ambientes-disponiveis-no-moodle-para-publicos-diversos)]

Assim como a futura atualização planejada para o Moodle 4.0, essas mudanças indicam uma trajetória de evolução contínua da plataforma, conforme comunicado pelo CEAD: "Apesar da identidade visual distinta, ambos possuem a mesma versão do Moodle, a 3.11. É a mais recente disponível a comunidade. Mas salienta-se a iminência da versão 4.0, que promete dar um salto na qualidade de experiência". [[Referência](https://cead.unb.br/ambientes-virtuais-de-aprendizagem/)]

---

### Cálculo da Métrica 2.1

- **Sim:** foi encontrada evidência clara de migração bem-sucedida

---

### Validação da Hipótese

**H2.1: VALIDADA**

O Aprender 3 demonstra capacidade de substituição e evolução, com evidências documentadas de migração bem-sucedida ao longo do tempo evidenciando a capacidade da plataforma de ser substituída por versões mais novas, mantendo a continuidade dos serviços.

---


<!-- ---

## 3. CT-POR-04: Compatibilidade de Plugins e Temas na Atualização do Moodle

### 3.1 Informações do Teste

- **Questão GQM:** Q2 (Substituibilidade)
- **Métrica Associada:** Métrica 2.2 – Taxa de Compatibilidade de Plugins na Atualização
- **Hipótese Relacionada:** H2.2 – Natureza modular permite atualização de componentes
- **Perfil Principal:** Equipe Técnica / Administração do Moodle

### 3.2 Ambiente de Teste

- Acesso à lista completa de plugins e temas do Aprender 3.
- Versão atual do Moodle e versão-alvo de atualização.
- Acesso ao diretório oficial de plugins do Moodle.

### 3.3 Testes Realizados

O teste consistiu em verificar a compatibilidade de plugins e temas do Aprender 3 com a versão atual do Moodle e a versão-alvo de atualização.

### 3.4 Resultados dos Testes

Os resultados dos testes mostraram que 90% dos plugins e temas do Aprender 3 são compatíveis com a versão atual do Moodle e a versão-alvo de atualização.


### 3.5 Classificação da Métrica


Classificação Obtida: **Excelente** -->

---

## CT-POR-04: Sucesso na Configuração do App Moodle por Novos Usuários

### Testes Realizados

- Grupo de 3 usuários de teste sem experiência prévia com o app Moodle e que não são estudantes da UnB.
- Dispositivos móveis (Android/iOS), um por participante.

O teste consiste em verificar a capacidade dos usuários de configurar o app Moodle sem assistência técnica.

### Resultados dos Testes

Os resultados dos testes mostraram que 100% dos usuários conseguiram configurar o app Moodle sem assistência técnica. A seguir está linkado o vídeo da gravação de tela dos smartphones realizados durante os testes. Um vídeo foi realizado em um aparelho android e o outro em um aparelho iOS. O terceiro teste também foi realizado em um smartphone iOS e como obteve o mesmo resultado não se fez necessário adicionar seu vídeo, por já possuir um video praticamente igual

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/CemC_KH0Jc0"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

### Cálculo da Métrica
Taxa de Sucesso na Configuração do App por Novos Usuários = (3 / 3) x 100 = 100%. Como todos os testes foram bem-sucedidos por usuários que não estão acostumados com a tecnologia e em diferentes dispositivos, a portabilidade do app é considerada excelente.

Classificação Obtida: **Excelente**

---

## CT-POR-05: Verificação de Dependências de Navegador (Navegador Limpo)

### Testes Realizados

O teste consistiu em verificar se o Aprender 3 funciona corretamente em um navegador limpo, simulado a partir de uma guia anônima, sem extensões ou dados de sessão.

### Resultados dos Testes

Os resultados dos testes mostraram que as funções listadas no teste funcionam corretamente no Aprender 3 em um navegador limpo, sem a necessidade da instalação de plugins adicionais ou de configurações específicas, demonstrando alta portabilidade. O teste foi realizado em uma guia anônima do Google Chrome e realizou todas as funcionalidades listadas na fase 3. O vídeo do teste encontra-se disponível abaixo.

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/GZV3IjGjVUo"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

### Cálculo da Métrica

De acordo com a métrica binária definida, como nenhuma plugin ou extensão adicional foi necessária para o funcionamento correto, a verificação de dependências de navegador foi bem-sucedida e o sistema foi classificado com **Excelente (Portável)**, por não exigir dependências adicionais em nenhuma das tarefas de teste descritas.


---

## Resumo dos Resultados

### Métricas Avaliadas

| Métrica       | Descrição                                       | Resultado  | Classificação |
| ------------- | ----------------------------------------------- | ---------- | ------------- |
| **CT-POR-01** | Taxa de Conformidade de Layout Responsivo       | 71,11%     | **Regular**   |
| **CT-POR-02** | Taxa de Sucesso em Funcionalidades no App Móvel | 97,14%     | **Excelente** |
| **CT-POR-03** | Verificação de Histórico de Migração            | Confirmado | **Sim**       |
| **CT-POR-04** | Compatibilidade de Plugins e Temas na Atualização do Moodle | 100% | **Excelente** |
| **CT-POR-05** | Sucesso na Configuração do App Moodle por Novos Usuários | 100% | **Excelente (Portável)** |

---

## Histórico de Versões

| Versão | Data       | Descrição                               | Autor                                  |
| :----: | ---------- | --------------------------------------- | -------------------------------------- |
| `1.0`  | 23/11/2025 | Criação da página e Adição do CT-POR-02 | [Yago Amin](https://github.com/yagoas) |
| `1.1`  | 23/11/2025 | Adição do CT-POR-03                     | [Yago Amin](https://github.com/yagoas) |
| `1.2`  | 24/11/2025 | Adição do CT-POR-04 e CT-POR-05         | [Felipe Hansen](https://github.com/FHansen98) |
| `1.3`  | 25/11/2025 | Adição do CT-POR-01                     | [Patrick Anderson Carvalho dos Santos](http://github.com/patrickacs) |
| `1.4`  | 25/11/2025 | Adição dos vídeos dos testes CT-POR-04 e CT-POR-05 | [Felipe Hansen](https://github.com/FHansen98) |

