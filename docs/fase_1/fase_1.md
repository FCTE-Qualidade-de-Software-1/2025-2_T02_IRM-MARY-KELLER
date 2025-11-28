# Fase 1 - Processo de Avaliação

---

## 1. Contexto de Trabalho

Este trabalho foi desenvolvido na disciplina Qualidade de Software com o objetivo de aplicar, na prática, técnicas, normas e boas práticas que garantem a qualidade de produtos e processos ao longo do ciclo de vida do software. Como atividade central, realizamos uma análise crítica de uma aplicação real, avaliando critérios como usabilidade, confiabilidade, segurança, portabilidade e outros atributos de qualidade relevantes. O resultado esperado é identificar pontos fortes, não conformidades e oportunidades de melhoria, propondo recomendações objetivas para elevar o nível de qualidade do software analisado.

---

## 2. Aplicação Escolhida

O software avaliado neste trabalho é o [Aprender 3](https://aprender3.unb.br/), o ambiente virtual de aprendizagem institucional da Universidade de Brasília, construído sobre a plataforma Moodle [3]. A ferramenta apoia disciplinas de modalidades presencial, híbrida e a distância, centralizando a publicação de conteúdos, a realização de atividades como tarefas e questionários, a comunicação por meio de fóruns e avisos, e o acompanhamento do desempenho dos estudantes. O Aprender 3 sucedeu a versão anterior, Aprender 2, consolidando a migração da UnB para uma base tecnológica mais moderna, estável e escalável.

Como uma instância do Moodle, o Aprender 3 herda uma arquitetura modular e extensível, com uma vasta biblioteca de plugins que incluem fóruns, rubricas, bancos de questões e o sistema de notas. Seus mecanismos de análise de uso apoiam tanto a docência quanto a gestão acadêmica. A filosofia de código aberto do Moodle permite a evolução contínua das funcionalidades sem dependência de fornecedores proprietários, além de favorecer análises de engajamento e usabilidade no contexto educacional [3].

A natureza aberta da plataforma Moodle alinha-se aos princípios da educação pública, como transparência, auditabilidade e colaboração, promovendo a melhoria contínua pela comunidade e garantindo a independência tecnológica da universidade. Para a UnB, isso se traduz em um ecossistema sustentável, que facilita a adaptação pedagógica, a acessibilidade e a interoperabilidade.

A avaliação do software considera critérios de qualidade essenciais como a portabilidade e a compatibilidade. A portabilidade é a capacidade de um software ser executado em diferentes ambientes computacionais com mínima modificação, como uma aplicação web que funciona em múltiplos navegadores e plataformas. Já a compatibilidade abrange tanto a habilidade de um software coexistir com outros sistemas sem gerar conflitos, a exemplo de uma aplicação que funciona dentro de um ecossistema maior como o Moodle, quanto a sua capacidade de interoperar, ou seja, de trocar informações com serviços externos para executar funções, como ao se integrar a um sistema de e-mail para enviar notificações.

---

## 3. Requisitante e Partes Interessadas


Em conformidade com o processo SQuaRE, foram identificadas as partes interessadas relevantes para o software:

-   **Requisitante:** Professora responsável pela disciplina de Qualidade de Software.
    
-   **Demais Stakeholders:** Estudantes e docentes usuários do Aprender3, equipe técnica e administradores do ambiente, coordenações de curso, departamentos acadêmicos e a gestão universitária.

---

## 4. Classificação do Tipo de Produto

A classificação do produto Aprender 3, essencial para definir o escopo de implementação e manutenção, é a seguinte:

- **Tipo de software:** Aplicação web educacional.
- **Categoria:** Ambiente Virtual de Aprendizagem (AVA).
- **Natureza:** Sistema multiusuário, modular, responsivo, baseado em navegador.
- **Modelo de implantação:** Hospedado institucionalmente (on-premise), acessado via web ou aplicativo móvel.
- **Base tecnológica:** Moodle (PHP), banco de dados MySQL/MariaDB e plugins educacionais.

---

## 5. Propósito da Avaliação e Uso Pretendido dos Resultados


O propósito desta avaliação é analisar a qualidade do Aprender 3 com foco exclusivo nas características de **Portabilidade** e **Compatibilidade**, conforme orientação da professora. Os resultados obtidos serão utilizados para:

-   documentar a situação atual da qualidade do software, atendendo às necessidades institucionais e aos requisitos da disciplina;
    
-   identificar possíveis problemas, falhas e oportunidades de melhoria relacionados às características avaliadas;
    
-   aplicar e consolidar, na prática, os conceitos estudados na disciplina de Qualidade de Software.

---

## 6. Modelo de Qualidade (ISO/IEC 25010) e Adaptação

O modelo de qualidade adotado segue a norma ISO/IEC 25010 (SQuaRE). No entanto, conforme orientação da disciplina, apenas **Portabilidade** e **Compatibilidade** serão avaliadas nesta fase. As demais características do modelo não serão consideradas para métricas, escopo ou análise detalhada nesta etapa.

### **Características Selecionadas para Avaliação**

#### Portabilidade  
A Portabilidade avalia o quão facilmente o software pode ser transferido para diferentes ambientes computacionais, garantindo acesso amplo pela comunidade universitária. Inclui:

- **Adaptabilidade:** capacidade do sistema de ajustar-se a diferentes resoluções, navegadores e dispositivos.
- **Instalabilidade:** facilidade de uso tanto via navegador quanto por aplicativo móvel oficial.
- **Substituibilidade:** potencial de substituir versões anteriores do ambiente (ex.: migração do Aprender 2 para o Aprender 3).

#### Compatibilidade  
A Compatibilidade mede o modo como o software se comporta ao coexistir com outros sistemas e se integra ao ecossistema institucional. Inclui:

- **Coexistência:** operação simultânea com serviços institucionais e plugins do Moodle.
- **Interoperabilidade:** troca de dados com serviços externos, como e-mail institucional, calendários e SIGAA.

### **Características Não Consideradas nesta Fase (mantidas apenas para registro histórico)**

- Adequação Funcional  
- Eficiência  
- Confiabilidade  
- Segurança  
- Manutenibilidade  
- Usabilidade (vetada pela professora)

---

## 7. Classificação e Ênfase das Características de Qualidade

A decisão sobre a prioridade das características de qualidade para o Aprender3 foi alcançada através de uma votação no canal do Discord da equipe.

### Método de Votação  

Cada membro da equipe recebeu **2 votos** para distribuir entre as características consideradas mais importantes, totalizando **12 votos**. Após a contabilização e uma discussão coletiva, os resultados foram convertidos para uma **escala qualitativa de 0 a 5**, utilizada para representar o nível de prioridade atribuído pelo grupo:

- **5** — prioridade máxima  
- **2** — prioridade baixa  
- **1** — prioridade mínima  
- **0** — característica excluída da análise (vetada)

Com base nesse processo, a classificação final das características de qualidade ficou definida conforme a tabela abaixo.

---

### **Tabela de Ênfase das Características de Qualidade**

| Característica | Ênfase (0–5) | Justificativa |
| :--- | :---: | :--- |
| **Compatibilidade** | **5 – grande interesse** | Considerada foco principal da equipe. É essencial para que o Aprender3 opere de forma integrada ao ecossistema tecnológico da UnB (como e-mail institucional, SIGAA e serviços de calendários), garantindo um fluxo de trabalho contínuo, estável e interoperável para alunos e professores. |
| **Portabilidade** | **5 – grande interesse** | Também definida como foco principal. Fundamental para assegurar que a plataforma seja acessível e funcional em diversos dispositivos (computadores, tablets, celulares) e navegadores, atendendo à diversidade de perfis e contextos de acesso dos usuários da comunidade acadêmica. |
| **Adequação Funcional** | **2 – baixo interesse** | O Moodle já oferece um conjunto robusto de funcionalidades consolidadas ao longo dos anos. Por esse motivo, o grupo entendeu que as funções essenciais já atendem às necessidades da universidade, não sendo prioridade aprofundar essa característica nesta avaliação. |
| **Confiabilidade** | **2 – baixo interesse** | Embora importante, a confiabilidade foi tratada como um critério secundário, pois o Aprender3 já está em operação e sob administração da equipe de TI da UnB. Considerou-se que a estabilidade atual do sistema é suficiente para os objetivos desta análise. |
| **Eficiência (Desempenho)** | **2 – baixo interesse** | A eficiência foi reconhecida como relevante, mas não prioritária para esta etapa. Como o desempenho depende fortemente da infraestrutura institucional (servidores, rede, banco de dados), a equipe optou por concentrar esforços nas dimensões de integração e acesso multiplataforma. |
| **Segurança** | **1 – nenhum interesse** | A segurança é tratada como um requisito institucional já estabelecido pela universidade e, portanto, não foi incluída no escopo desta análise de qualidade. |
| **Manutenibilidade** | **1 – nenhum interesse** | A manutenibilidade é considerada uma responsabilidade da equipe técnica encarregada do desenvolvimento e manutenção do Moodle na UnB, não sendo um foco desta avaliação. |
| **Usabilidade** | **0 – fora da votação** | A característica foi explicitamente vetada pela professora para esta fase do projeto, por isso não participou da votação nem da priorização. |

*(Esta seção é mantida integralmente por ser parte do processo histórico de escolha, embora apenas Portabilidade e Compatibilidade sejam realmente utilizadas no modelo de qualidade desta fase.)*

---

## 8. Escopo, Profundidade e Objetos da Avaliação

### **Escopo**
- Interface web do Aprender3.
- Funcionalidade dos módulos essenciais (tarefas, questionários, fóruns).
- Acesso via navegadores comuns, como: Chrome, Firefox e Edge.
- Acesso via desktop e dispositivos móveis.
- Integração com serviços institucionais (e-mail institucional e calendários).

### **Fora do Escopo**
- Testes de desempenho de infraestrutura.
- Testes que dependam de código.
- Segurança de servidores e banco de dados.
- Avaliação de código-fonte.
- Análise de usabilidade ou características não escolhidas.

### **Profundidade**
- Avaliação funcional de alto nível.
- Testes manuais.
- Verificação de consistência entre dispositivos e navegadores.

### **Objetos Avaliados**
- Responsividade e layout.
- Coexistência com sistemas institucionais.
- Interoperabilidade com serviços externos.
- Consistência funcional entre plataformas.


### **Relação com o processo de avaliação**

Esta fase corresponde ao início da avaliação, responsável por definir o escopo, os critérios de qualidade e o direcionamento teórico do projeto. Ela estabelece as bases conceituais e metodológicas que orientam toda a análise realizada sobre a plataforma Aprender3.

## 9. Proposta de Avaliação e Melhoria de Qualidade

A proposta busca elevar a qualidade da plataforma Aprender3 a partir da perspectiva dos seus usuários. A avaliação será conduzida por meio de testes manuais, focados em cenários de uso real. Serão utilizados métricas para verificar consistência da interface em diferentes navegadores e dispositivos, além de testes manuais para testar integração com outros sistemas, como o sistema de e-mail. 

### Público-Alvo

Embora o público principal do Aprender3 seja composto por professores e estudantes da UnB, é fundamental reconhecer os diferentes perfis e níveis de familiaridade e acessibilidade dos usuários para com a plataforma Moodle. Em geral, a aplicação abrange a gestão de:

- Disciplinas de Graduação e Pós-graduação;   

---

## 10. Conexão com ODS da ONU

O Aprender 3, como ambiente virtual de aprendizagem institucional da UnB construído sobre o Moodle, conecta-se aos Objetivos de Desenvolvimento Sustentável da Agenda 2030 ao ampliar acesso, apoiar práticas pedagógicas inovadoras e facilitar colaboração acadêmica [4].

| ODS | Contribuição do Aprender 3 |
| --- | --- |
| **ODS 4 – Educação de Qualidade** | Disponibiliza conteúdos on-line, flexibiliza modalidades de ensino e apoia avaliação formativa. |
| **ODS 5 – Igualdade de Gênero** | Favorece acesso igualitário a ambientes de ensino e permanência acadêmica. |
| **ODS 9 – Indústria, Inovação e Infraestrutura** | Sustenta infraestrutura digital e estimula inovação pedagógica via plugins e ferramentas tecnológicas. |
| **ODS 10 – Redução das Desigualdades** | Facilita acesso remoto e inclui recursos essenciais de acessibilidade. |
| **ODS 17 – Parcerias e Meios de Implementação** | Apoia cooperação acadêmica, cursos online e compartilhamento de boas práticas. |

---

## 11. Referências Bibliográficas

> [1] ISO/IEC 25010. Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models.  
> [2] ISO/IEC 25023:2016. Systems and software engineering — Measurement of system and software product quality.  
> [3] Moodle. Moodle - Open-source learning platform.  
> [4] ONU Brasil. Objetivos de Desenvolvimento Sustentável.

---

## 12. Histórico de Versões

| Versão | Data | Descrição | Autor |
|:-----:|------|-----------|--------|
| `1.0` | 28/09/2025 | Criação do documento | Pedro Sampaio |
| `1.1` | 29/09/2025 | Adição da Proposta de Avaliação e Melhoria de Qualidade | Felipe Hansen |
| `1.2` | 29/09/2025 | Revisão geral do documento | Yago Amin |
| `1.3` | 29/09/2025 | Adição das Especificação do Modelo de Qualidade | Yago Amin |
| `1.4` | 30/09/2025 | Correções sugeridas pela professora | Taynara Vitorino |
| `1.5` | 01/10/2025 | Descrição da votação da Tabela de Ênfase | Felipe Hansen |
