# Fase 1 - Processo de Avaliação

---

## Contexto de Trabalho

Este trabalho foi desenvolvido na disciplina Qualidade de Software com o objetivo de aplicar, na prática, técnicas, normas e boas práticas que garantem a qualidade de produtos e processos ao longo do ciclo de vida do software. Como atividade central, realizamos uma análise crítica de uma aplicação real, avaliando critérios como usabilidade, confiabilidade, segurança, portabilidade e outros atributos de qualidade relevantes. O resultado esperado é identificar pontos fortes, não conformidades e oportunidades de melhoria, propondo recomendações objetivas para elevar o nível de qualidade do software analisado.

---

## Aplicação Escolhida

O software avaliado neste trabalho é o [Aprender 3](https://aprender3.unb.br/), o ambiente virtual de aprendizagem institucional da Universidade de Brasília, construído sobre a plataforma Moodle [3]. A ferramenta apoia disciplinas de modalidades presencial, híbrida e a distância, centralizando a publicação de conteúdos, a realização de atividades como tarefas e questionários, a comunicação por meio de fóruns e avisos, e o acompanhamento do desempenho dos estudantes. O Aprender 3 sucedeu a versão anterior, Aprender 2, consolidando a migração da UnB para uma base tecnológica mais moderna, estável e escalável.

Como uma instância do Moodle, o Aprender 3 herda uma arquitetura modular e extensível, com uma vasta biblioteca de plugins que incluem fóruns, rubricas, bancos de questões e o sistema de notas. Seus mecanismos de análise de uso apoiam tanto a docência quanto a gestão acadêmica. A filosofia de código aberto do Moodle permite a evolução contínua das funcionalidades sem dependência de fornecedores proprietários, além de favorecer análises de engajamento e usabilidade no contexto educacional [3].

A natureza aberta da plataforma Moodle alinha-se aos princípios da educação pública, como transparência, auditabilidade e colaboração, promovendo a melhoria contínua pela comunidade e garantindo a independência tecnológica da universidade. Para a UnB, isso se traduz em um ecossistema sustentável, que facilita a adaptação pedagógica, a acessibilidade e a interoperabilidade.

A avaliação do software considera critérios de qualidade essenciais como a portabilidade e a compatibilidade. A portabilidade é a capacidade de um software ser executado em diferentes ambientes computacionais com mínima modificação, como uma aplicação web que funciona em múltiplos navegadores e plataformas. Já a compatibilidade abrange tanto a habilidade de um software coexistir com outros sistemas sem gerar conflitos, a exemplo de uma aplicação que funciona dentro de um ecossistema maior como o Moodle, quanto a sua capacidade de interoperar, ou seja, de trocar informações com serviços externos para executar funções, como ao se integrar a um sistema de e-mail para enviar notificações.

---

## Classificação e Ênfase das Características de Qualidade

Nesta etapa inicial do processo de avaliação da plataforma Aprender3, foram definidas as características de qualidade a serem consideradas com base em seus objetivos estratégicos e no perfil de sua comunidade. A análise levou em conta as necessidades de integração da ferramenta ao ecossistema digital da instituição e a garantia de acesso amplo para todos os usuários.

O processo de definição dos pesos para cada característica de qualidade foi realizado em uma reunião com a participação de todos os membros da equipe. Durante a discussão, cada integrante apresentou sua perspectiva sobre a importância das características, considerando o público-alvo e os objetivos do Aprender3. Ao final, os pesos foram atribuídos por consenso, refletindo um entendimento coletivo sobre as prioridades estratégicas do projeto.

Foram priorizadas as características de portabilidade e compatibilidade. A portabilidade é fundamental para garantir que alunos e professores possam acessar a plataforma a partir de qualquer dispositivo. Já a compatibilidade é crucial para assegurar que o Aprender3 não funcione como um sistema isolado, mas sim como uma peça integrada à infraestrutura tecnológica e aos serviços já existentes na universidade.

A seguir, detalham-se as características priorizadas com exemplos concretos extraídos da análise do sistema, conforme os critérios da abordagem SQuaRE (ISO/IEC 25010) [1].

### Análise Detalhada das Características e Subcaracterísticas

* **Portabilidade:** mede o quão fácil é adaptar o sistema a diferentes ambientes.
    * **Adaptabilidade e Instalabilidade:** por ser um sistema web, o Aprender 3 funciona nos principais navegadores (Chrome, Firefox, Edge, Safari) e em sistemas operacionais variados (Windows, Linux, macOS, Android, iOS), exigindo apenas conexão e navegador atualizados. Em dispositivos móveis, pode ser acessado via navegador ou aplicativo oficial do ecossistema Moodle, o que facilita a instalação e o uso. O layout responsivo se ajusta a diferentes tamanhos de tela (smartphones, tablets, notebooks, monitores ultrawide), reduzindo a necessidade de configurações locais. Exemplos: acesso a tarefas e questionários pelo celular, visualização de notas no tablet e upload de arquivos a partir do desktop.
    * **Substituibilidade:** a evolução do Aprender 2 para o Aprender 3 demonstra a capacidade de substituir versões anteriores com migração de dados e continuidade de serviços. Essa característica permite atualizar a plataforma conforme novas demandas acadêmicas, atualizar plugins e temas, e descontinuar componentes obsoletos sem interromper o uso pelos cursos. Exemplos: troca de tema para melhorar acessibilidade, atualização de plugins de questionário, e migração de cursos arquivados para o novo ambiente.

* **Compatibilidade:** avalia a capacidade do Aprender 3 de coexistir e interagir com outros sistemas.
    * **Coexistência:** o Aprender 3 convive com o ecossistema Moodle e seus componentes, incluindo o aplicativo móvel e extensões de funcionalidade. Também opera de forma estável ao lado de serviços institucionais como repositórios de documentos, bibliotecas digitais e ferramentas de videoconferência adotadas pela universidade. Exemplos: abertura de PDFs hospedados em repositórios institucionais, incorporação de vídeos educacionais e utilização de salas virtuais de aula.
    * **Interoperabilidade:** o sistema integra-se a serviços institucionais para automatizar fluxos comuns, como envio de notificações por e-mail, publicação de avisos em massa e sincronização de prazos com calendários acadêmicos. Também permite troca de arquivos e referências com serviços de nuvem adotados pela instituição, bem como exportação de notas e relatórios para planilhas e sistemas administrativos quando habilitados. Exemplos: avisos de novas atividades enviados ao e-mail dos estudantes, eventos de prova aparecendo no calendário pessoal e exportação de notas para acompanhamento em relatórios acadêmicos.

### Tabela de Ênfase

A decisão sobre a prioridade das características de qualidade para o Aprender3 foi alcançada através de uma votação no canal do Discord da equipe.

O Método de Votação: Para garantir um foco claro e justo, cada membro da equipe recebeu o direito a apenas 2 votos no total, que deveriam ser atribuídos às características consideradas mais importantes. O resultado final da ênfase (escala de 1 a 5) foi uma representação do nível de consenso do grupo:

 - As características de Compatibilidade e Portabilidade foram as que receberam a maioria dos votos, sendo, por isso, categorizadas com a Ênfase 5 (Grande Interesse).

 - As características de Adequação Funcional, Eficiência e Confiabilidade receberam alguns votos, indicando um interesse secundário e aceitável para o lançamento inicial, o que as posicionou com a Ênfase 2 (Baixo Interesse).

 - Por fim, Segurança e Manutenibilidade foram as únicas a registrar zero votos, resultando na Ênfase 1 (Nenhum Interesse), após o consenso de que seriam otimizadas e priorizadas em fases subsequentes.

 - A Usabilidade foi a única característica que não foi incluída na votação, pois foi vetada pela professora, resultando na Ênfase 0.

| Característica | Ênfase (1-5) |
| --- | --- |
| Compatibilidade | 5 – grande interesse |
| Portabilidade | 5 – grande interesse |
| Adequação Funcional | 2 – baixo interesse |
| Confiabilidade | 2 – baixo interesse |
| Eficiência (Desempenho)| 2 – baixo interesse |
| Segurança | 1 – nenhum interesse |
| Manutenibilidade | 1 – nenhum interesse |
| Usabilidade | 0 – fora da votação |

Essa priorização servirá como base para a especificação das métricas e o planejamento da avaliação, garantindo foco na capacidade do Aprender3 de operar de forma integrada, flexível e acessível dentro do ambiente tecnológico da instituição.

---

## Proposta de Avaliação e Melhoria de Qualidade

A proposta busca elevar a qualidade da plataforma Aprender3 (Moodle da UnB), a partir do ponto de vista dos seus usuários (professores e estudantes) e também dos desenvolvedores e da equipe de suporte. O foco é garantir que o ambiente virtual de aprendizagem (AVA) seja acessível e confiável para apoiar o ensino e a pesquisa na Universidade de Brasília.

A avaliação será conduzida por meio de testes manuais e automatizados, focados em cenários de uso real. Serão utilizados checklists para verificar a consistência da interface em diferentes navegadores e dispositivos, além de scripts para testar a integração com APIs de serviços institucionais, como o sistema de e-mail. Adicionalmente, será aplicada uma pesquisa de satisfação com um grupo de estudantes para coletar feedback sobre a experiência de uso em dispositivos móveis e computadores.

### Público-alvo

Embora o público principal do Aprender3 seja composto por professores e estudantes da UnB, é fundamental reconhecer os diferentes perfis e níveis de familiaridade e acessibilidade dos usuários para com a plataforma Moodle. Em geral, a aplicação abrange a gestão de:

* Disciplinas de Graduação e Pós-Graduação: Servindo como espaço central para a disponibilização de conteúdo, comunicação, atividades avaliativas e interação.
* Cursos de Extensão, Treinamentos e Projetos Especiais: Apoiando diversas iniciativas da universidade.

### Foco da Avaliação

| Foco | Descrição |
| --- | --- |
| Portabilidade (Cross-Platform) | Analisar a capacidade do sistema de ser executado de forma consistente em diferentes ambientes computacionais, verificando sua funcionalidade e layout em diversos navegadores (Chrome, Firefox, Edge, Safari) e dispositivos (desktop, tablet, mobile), assegurando uma boa experiência em todos os dispositivos. |
| Compatibilidade e Interoperabilidade | Avaliar a coexistência do software dentro do ecossistema Moodle e a sua capacidade de interoperar e trocar dados com sucesso com sistemas externos da UnB (como o SIGAA para dados acadêmicos e o sistema de e-mail institucional para notificações), garantindo um fluxo de trabalho integrado e sem conflitos. |

## Especificação do Modelo de Qualidade

Para avaliar a qualidade da plataforma Aprender 3, adotaremos um modelo baseado na ISO/IEC 25010 (SQuaRE), com foco principal nas características de **Portabilidade** e **Compatibilidade** [1]. As métricas da ISO/IEC 25023 fornecerão diretrizes específicas para medir portabilidade e compatibilidade de forma padronizada e objetiva [2]. A combinação dessas metodologias assegurará uma avaliação abrangente, alinhando os critérios técnicos da ISO 25010 com as necessidades reais dos usuários (professores e estudantes) e stakeholders da UnB.

---

## Conexão com ODS (Objetivos de Desenvolvimento Sustentável) da ONU

O Aprender 3, como ambiente virtual de aprendizagem institucional da UnB construído sobre o Moodle, conecta-se aos [Objetivos de Desenvolvimento Sustentável (ODS)](https://brasil.un.org/pt-br/sdgs) da Agenda 2030 ao ampliar acesso, apoiar práticas pedagógicas inovadoras e facilitar colaboração acadêmica [4]. Abaixo, os ODS mais diretamente relacionados:

| ODS | Como o Aprender 3 contribui / pode contribuir |
| --- | --- |
| ODS 4 – Educação de Qualidade | Disponibiliza conteúdos e disciplinas on-line; flexibiliza o ensino entre presencial, híbrido e remoto; apoia docentes e estudantes no uso de tecnologia educacional, favorecendo aprendizagem contínua e avaliação formativa. |
| ODS 5 – Igualdade de Gênero | Oferece condições de acesso e permanência em igualdade para todas as pessoas; quando alinhado a políticas institucionais, contribui para ampliar participação feminina em cursos, projetos e atividades acadêmicas. |
| ODS 9 – Indústria, Inovação e Infraestrutura | Sustenta infraestrutura digital universitária estável; incentiva inovação pedagógica por meio de ferramentas e plugins; permite personalização do ambiente conforme a realidade da UnB, elevando eficiência e qualidade do ecossistema acadêmico. |
| ODS 10 – Redução das Desigualdades | Possibilita acesso a estudantes geograficamente distantes ou com restrições de deslocamento; pode incorporar recursos de acessibilidade (legendas, leitores de tela, design responsivo) para inclusão de diferentes perfis de usuários. |
| ODS 17 – Parcerias e Meios de Implementação | Facilita colaboração entre universidades e órgãos públicos, compartilhamento de recursos digitais, oferta de cursos e eventos on-line, e intercâmbio de boas práticas, fortalecendo redes de cooperação. |

## Tabela de Contribuição

Na Tabela 1, apresenta-se a contribuição dos membros da equipe na construção do artefato.

<font size="3"><p style="text-align: center">Tabela 1 - Tabela de contribuição</p></font>

<div align="center">
  <table border="1">
    <thead>
      <tr>
        <th>Matrícula</th>
        <th>Nome completo</th>
        <th>Contribuição (%)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>222032810</td>
        <td><a href="https://github.com/Fhansen98">Felipe Aguiar Hansen</a></td>
        <td>16,66</td>
      </tr>
      <tr>
        <td>211030620</td>
        <td><a href="https://github.com/patrickacs">Patrick Anderson Carvalho dos Santos</a></td>
        <td>16,66</td>
      </tr>
      <tr>
        <td>211043745</td>
        <td><a href="https://github.com/PedroSampaioDias">Pedro Sampaio Dias Rocha</a></td>
        <td>16,66</td>
      </tr>
      <tr>
        <td>211030264</td>
        <td><a href="https://github.com/taybalau">Taynara Gabrielle Vitorino</a></td>
        <td>16,66</td>
      </tr>
      <tr>
        <td>202017147</td>
        <td><a href="https://github.com/thalesgvl">Thales Germano Vargas Lima</a></td>
        <td>16,66</td>
      </tr>
      <tr>
        <td>190101091</td>
        <td><a href="https://github.com/yagoas">Yago Amin Santos</a></td>
        <td>16,66</td>
      </tr>
    </tbody>
  </table>
</div>

<font size="3"><p style="text-align: center"><b>Autores: Grupo Irmã Mary Keller, 2025</p></font>

## Referências Bibliográficas

> [1] ISO/IEC 25010. Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards/iso-25010>. Acesso em: 28 de setembro de 2025.

> [2] ISO/IEC 25023:2016. Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — Measurement of system and software product quality. Disponível em: <https://www.iso.org/standard/35747.html>. Acesso em: 29 de setembro de 2025.

> [3] Moodle. Moodle - Open-source learning platform. Disponível em: <https://moodle.org/>. Acesso em: 28 de setembro de 2025.

> [4] ONU Brasil. Objetivos de Desenvolvimento Sustentável. Disponível em: <https://brasil.un.org/pt-br/sdgs>. Acesso em: 28 de setembro de 2025.

## Histórico de Versões

|Versão|Data|Descrição|Autor|
|:---:|---|---|---|
|`1.0`|28/09/2025|Criação do documento| [Pedro Sampaio](https://github.com/PedroSampaioDias)|
|`1.1`|29/09/2025|Adição da Proposta de Avaliação e Melhoria de Qualidade| [Felipe Hansen](https://github.com/Fhansen98)|
|`1.2`|29/09/2025|Revisão geral do documento| [Yago Amin](https://github.com/yagoas)|
|`1.3`|29/09/2025|Adição das Especificação do Modelo de Qualidade| [Yago Amin](https://github.com/yagoas)|
|`1.4`|30/09/2025|Correçoes sugeridas pela professora| [Taynara Vitorino](https://github.com/taybalau)|
|`1.5`|01/10/2025|Descrição da votação da Tabela de Ênfase| [Felipe Hansen](https://github.com/Fhansen98)|