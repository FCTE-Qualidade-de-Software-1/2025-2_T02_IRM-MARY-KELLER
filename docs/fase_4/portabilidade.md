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

### 1.3 Resultados dos Testes

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

### 1.4 Cálculo da Métrica 1.2

| Funcionalidade            | Status  | Considerada no Cálculo |
| ------------------------- | ------- | ---------------------- |
| Login e Autenticação      | Sucesso | Sim                    |
| Visualização de Conteúdos | Parcial | Sim                    |
| Envio de Tarefas          | Sucesso | Sim                    |
| Participação em Fóruns    | Sucesso | Sim                    |
| Acesso Offline            | Sucesso | Sim                    |

**Total de Funcionalidades Testadas:** 5

### 1.5 Taxa de Sucesso

- **Login:** 100% (1/1)
- **Visualização de Conteúdos:** 85,7% (6/7)
- **Envio de Tarefas:** 100% (5/5)
- **Fóruns:** 100% (4/4)
- **Acesso Offline:** 100% (1/1)

```
Taxa de Sucesso = (100% + 85,7% + 100% + 100% + 100%) ÷ 5 = 97,14%
```

---

### 1.6. Classificação da Métrica 1.2

Conforme critérios definidos na Fase 2:

| Faixa de Resultado | Classificação  |
| ------------------ | -------------- |
| **> 90%**          | **Excelente**  |
| 75% a 90%          | Bom            |
| 60% a 74%          | Regular        |
| < 60%              | Insatisfatório |

**Classificação Obtida:** **EXCELENTE**

---

## Histórico de Versões

| Versão | Data       | Descrição                               | Autor                                  |
| :----: | ---------- | --------------------------------------- | -------------------------------------- |
| `1.0`  | 23/11/2025 | Criação da página e Adição do CT-POR-02 | [Yago Amin](https://github.com/yagoas) |
