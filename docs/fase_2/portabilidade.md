# Portabilidade

## Objetivo de Medição 2: Portabilidade

**Tabela 2** - Objetivo de Medição 2: Portabilidade.

| **Analisar**           | A portabilidade do site "Aprender". |
|------------------------|------------------------------------------------------------------------------------------------|
| **Para o propósito de**| Garantir que ele possa ser facilmente adaptado e executado em diferentes ambientes.              |
| **Com respeito a**     | Sua adaptabilidade a navegadores e facilidade de instalação.                                   |
| **Do ponto de vista da** | Equipe de desenvolvimento.                                                                     |
| **No contexto da**     | Manutenção e implantação do site "Aprender".                                                   |

---

### Perguntas e Hipóteses de Medição

**Questão 1: Quão adaptável é o site a diferentes navegadores dispositivos?**
> A tecnologia usada no desenvolvimento do site garante que ele funcione corretamente nos navegadores mais populares?

* **Hipótese 1.1 (H1.1):** O layout responsivo do Aprender 3 se ajusta adequadamente a diferentes tamanhos de tela, e diferentes navegadores, garantindo sua usabilidade.
* **Hipótese 1.2 (H1.2):** O acesso via aplicativo oficial do Moodle oferece uma alternativa viável e funcional ao navegador, ampliando a portabilidade para o ecossistema móvel.

**Questão 2: A plataforma Moodle demonstra capacidade de substituibilidade, permitindo atualizações e migrações?**
> A arquitetura do Aprender 3 facilita a evolução do sistema, como a migração de dados de versões anteriores e a atualização de seus componentes?

* **Hipótese 2.1 (H2.1):** A migração bem-sucedida do Aprender 2 para o Aprender 3 evidencia a capacidade da plataforma de ser substituída por versões mais novas, mantendo a continuidade dos serviços.
* **Hipótese 2.2 (H2.2):** A natureza modular do Moodle permite a atualização e substituição de componentes (plugins e temas), garantindo sua evolução tecnológica e funcional.

---

### Seleção das Métricas

**Questão 1: Quão adaptável é o site a diferentes navegadores dispositivos?**

* **Métrica 1.1: Compatibilidade do Layout entre Navegadores**

    * **Definição:** Avalia o layout e as funcionalidades do site em diferentes resoluções de tela (desktop, tablet, smartphone) e em navegadores alvo.
    * **Coleta:** Teste manual, acessando o site `aprender3.unb.br` e executando tarefas (acessar um curso, visualizar notas, abrir um fórum) em cada tipo de dispositivo e diferentes navegadores (Google Chrome, Mozilla Firefox e Safari).
    * **Resultado:** O layout do Aprender 3 é responsivo e se adapta bem à maioria dos dispositivos, embora alguns elementos complexos, como tabelas de notas, possam exigir rolagem horizontal em telas menores.

* **Métrica 1.2: Funcionalidade do Aplicativo Móvel**
    * **Definição:** Verifica a disponibilidade e a funcionalidade do aplicativo oficial do Moodle como meio de acesso ao Aprender 3.
    * **Coleta:** Instalação do aplicativo Moodle em um dispositivo móvel (Android ou iOS), configuração do site `aprender3.unb.br` e teste de funcionalidades básicas.
    * **Resultado:** O aplicativo oficial do Moodle se conecta com sucesso ao Aprender 3, oferecendo uma interface para dispositivos móveis e confirmando a portabilidade da plataforma.

**Questão 2: A plataforma Moodle demonstra capacidade de substituibilidade, permitindo atualizações e migrações?**

* **Métrica 2.1: Histórico de Migração bem-sucedida**
    * **Definição:** Verifica a existência de evidências de migração de versões anteriores.
    * **Coleta:** Análise do histórico do projeto (ex: a transição do Aprender 2 para o Aprender 3).
    * **Resultado:** A existência do Aprender 3 como uma evolução do Aprender 2 é uma evidência da substituibilidade da plataforma.

<!-- * **Métrica 2.2: Análise da Arquitetura Modular**
    * **Definição:** Avalia a capacidade de atualizar ou trocar componentes individuais do sistema (plugins, temas).
    * **Coleta:** Análise da documentação oficial do Moodle e da lista de plugins instalados no próprio Aprender 3.
    * **Resultado:** A arquitetura do Moodle é reconhecidamente modular. Isso permite que a UnB atualize e adicione novos plugins de atividades, demonstrando capacidade de substituibilidade de componentes. -->
