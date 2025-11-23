# Resultados dos Testes de Portabilidade

Esta seção descreve os testes realizados e resultados obtidos com base nos **Casos de Teste (CTs)** projetados para avaliar a característica de **Portabilidade** do Aprender 3, conforme planejamento realizado na Fase 3.

---

## 1. CT-POR-02: Sucesso em Funcionalidades Essenciais no App Moodle

### 1.1 Informações do Teste

- **Questão GQM:** Q1 (Adaptabilidade)
- **Métrica Associada:** Métrica 1.2 – Taxa de Sucesso em Funcionalidades no App Móvel
- **Hipótese Relacionada:** H1.2 – App Moodle é alternativa viável ao navegador
- **Perfil Principal:** Discente

### 1.2 Ambiente de Teste

- **Dispositivo:** Pixel 9 Pro (Emulado)
- **Sistema Operacional:** Android 16.0 ("Baklava")
- **Versão do App Moodle:** 5.0.0 (atualizado em 27/06/2025)
- **Conexão:** Dados móveis (emulado)

### 1.3 Testes Realizados

O video da execução do teste está disponível a seguir:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/-wHRkMZcDag"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>

---

### 1.4 Resultados dos Testes

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

### 1.5 Cálculo da Métrica 1.2

| Funcionalidade            | Status  | Considerada no Cálculo |
| ------------------------- | ------- | ---------------------- |
| Login e Autenticação      | Sucesso | Sim                    |
| Visualização de Conteúdos | Parcial | Sim                    |
| Envio de Tarefas          | Sucesso | Sim                    |
| Participação em Fóruns    | Sucesso | Sim                    |
| Acesso Offline            | Sucesso | Sim                    |

Total de Funcionalidades Testadas: **5**

### 1.6 Taxa de Sucesso

- **Login:** 100% (1/1)
- **Visualização de Conteúdos:** 85,7% (6/7)
- **Envio de Tarefas:** 100% (5/5)
- **Fóruns:** 100% (4/4)
- **Acesso Offline:** 100% (1/1)

```
Taxa de Sucesso = (100% + 85,7% + 100% + 100% + 100%) ÷ 5 = 97,14%
```

---

### 1.7 Classificação da Métrica 1.1

Conforme critérios definidos na Fase 2:

| Faixa de Resultado | Classificação  |
| ------------------ | -------------- |
| **> 90%**          | **Excelente**  |
| 75% a 90%          | Bom            |
| 60% a 74%          | Regular        |
| < 60%              | Insatisfatório |

Classificação Obtida: **Excelente**

---

## 2. CT-POR-03: Verificação de Histórico de Migração

### 2.1 Informações do Teste

- **Questão GQM:** Q2 (Substituibilidade)
- **Métrica Associada:** Métrica 2.1 – Verificação de Histórico de Migração
- **Hipótese Relacionada:** H2.1 – Migração evidencia capacidade de substituição
- **Perfil Principal:** Equipe Técnica / Pesquisadores

### 2.2 Objetivo do Teste

Documentar evidências que comprovem a existência e o sucesso da migração/evolução do Aprender, validando a capacidade da plataforma de ser substituída por versões mais novas.

---

### 2.3 Resultados da Pesquisa

**Tabela de Fontes de Evidência**

| Fonte               | Acesso/Publicação | URL/Referência                                                                                                                            | Observações                                      |
| ------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| **Comunicado CEAD** | Novembro de 2025  | [Ambientes Virtuais de Aprendizagem](https://cead.unb.br/ambientes-virtuais-de-aprendizagem/)                                             | Histórico resumido do Moodle na UnB desde 2004   |
| **Comunicado UnB**  | 03/08/2020        | [Ambientes disponíveis no Moodle](https://noticias.unb.br/ensino/4340-descubra-os-ambientes-disponiveis-no-moodle-para-publicos-diversos) | Notícia oficial sobre diferenças entre ambientes |

---

### 2.4 Análise dos Resultados

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

### 2.5 Cálculo da Métrica 2.1

**Critério de Avaliação:** Métrica binária (Sim/Não)

- **Sim:** Pelo menos 2 fontes documentadas confirmando a migração/evolução

```
Resultado da Métrica 2.1: Sim
```

---

### 2.6 Classificação da Métrica 2.1

Conforme critérios definidos na Fase 2:

| Valor              | Interpretação          |
| ------------------ | ---------------------- |
| **Sim**            | **Hipótese validada**  |
| Não                | Hipótese refutada      |

Classificação Obtida: **Sim**

---

## Resumo dos Resultados

### Métricas Avaliadas

| Métrica       | Descrição                                       | Resultado  | Classificação |
| ------------- | ----------------------------------------------- | ---------- | ------------- |
| **CT-POR-02** | Taxa de Sucesso em Funcionalidades no App Móvel | 97,14%     | **Excelente** |
| **CT-POR-03** | Verificação de Histórico de Migração            | Confirmado | **Sim**       |

---

## Histórico de Versões

| Versão | Data       | Descrição                               | Autor                                  |
| :----: | ---------- | --------------------------------------- | -------------------------------------- |
| `1.0`  | 23/11/2025 | Criação da página e Adição do CT-POR-02 | [Yago Amin](https://github.com/yagoas) |
| `1.1`  | 23/11/2025 | Adição do CT-POR-03                     | [Yago Amin](https://github.com/yagoas) |
