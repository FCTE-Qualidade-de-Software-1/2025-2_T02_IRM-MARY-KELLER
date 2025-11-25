**A Metodologia GQM (Goal-Question-Metric) na Avaliação de Software: Fortalecendo a Medição com Estrutura Hierárquica**

A metodologia **GQM (Goal-Question-Metric)** é um paradigma de medição amplamente reconhecido na engenharia de *software*, desenvolvido por Victor Basili e sua equipe. Ela tem como premissa fundamental a **ligação direta e hierárquica** entre os objetivos de negócio, as questões de avaliação e as métricas coletadas [1], garantindo que a medição seja relevante e estratégica. O GQM é visto como uma técnica para definir e apoiar a medição no contexto de objetivos específicos de projeto e qualidade [3].

A abordagem GQM garante que as métricas coletadas estejam diretamente alinhadas aos objetivos da avaliação, transformando um problema de negócio (por exemplo, baixa confiabilidade percebida) em um **plano de medição concreto e orientado a dados**. A essência do GQM reside em um processo de definição de objetivos que, por sua vez, determinam as questões e as métricas necessárias para a coleta de dados [4].

A estrutura hierárquica do GQM pode ser visualizada da seguinte forma, ilustrando a cascata de abstração, onde o **Goal** é o mais abstrato e as **Metrics** são o nível mais concreto [3]:

* **Objetivo (Goal):** Define o que se deseja alcançar, considerando o propósito, o objeto de estudo, o ponto de vista e o contexto. O *goal* é a espinha dorsal do GQM, fornecendo a motivação para toda a estrutura de medição [1].
* **Perguntas (Questions):** Identificam os aspectos específicos que precisam ser avaliados para atingir o objetivo. As perguntas detalham o *goal* em termos mensuráveis, funcionando como uma ponte entre o objetivo estratégico e a coleta de dados [1]. O conjunto de perguntas busca caracterizar o objeto de estudo e avaliar a realização do objetivo [3].
* **Métricas (Metrics):** Fornecem os dados necessários para responder às perguntas, permitindo uma análise quantitativa ou qualitativa. As métricas são os dados brutos ou processados que dão subsídio às respostas [1]. Elas são definidas de forma a coletar a informação necessária para responder a cada pergunta [4].

Essa metodologia é especialmente útil em projetos complexos, onde a medição de características como confiabilidade, manutenibilidade e segurança é essencial para garantir o sucesso do sistema [2]. A clareza e a estrutura hierárquica do GQM asseguram que cada esforço de medição contribua diretamente para o entendimento e a melhoria do sistema em relação aos seus objetivos predefinidos.

---

**Estrutura GQM (Diagrama)**

<div align="center">
  <img src="https://fga-eps-mds.github.io/2019.1-Aix/assets/img/GQM.png"
       alt="Estrutura Goal-Question-Metric">
</div>

**Explicação do Diagrama:**

O diagrama ilustra a estrutura em três níveis e o fluxo de trabalho da metodologia **GQM (Goal-Question-Metric)**, que estabelece uma ligação clara entre os objetivos de medição e as métricas de software.

| Nível | Nome |
| :--- | :--- |
| **1** | **Nível Conceitual** (Goals/Metas) |
| **2** | **Nível Operacional** (Questions/Perguntas) |
| **3** | **Nível Quantitativo** (Metrics/Métricas) |

**Conexões:**
As setas indicam a relação hierárquica: uma única **Meta** pode ser desdobrada em várias **Perguntas (Q)**, e cada **Pergunta (Q)** pode exigir a coleta de uma ou mais **Métricas (M)**.

**Fluxo de Trabalho:**

* Definição: Ocorre de cima para baixo (do Goal para a Metric).
* **Análise e Interpretação:** Ocorre de baixo para cima (a partir da Metric para responder ao Goal).

---

### **Referências Bibliográficas sobre o GQM**

> [1] Basili, V. R., Caldiera, G., & Rombach, H. D. (1994). **The Goal Question Metric Approach**. Em *Encyclopedia of Software Engineering*. John Wiley & Sons.

> [2] ISO/IEC 25010. (2011). **Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models**. International Organization for Standardization.

> [3] Universidade Federal de Pernambuco (UFPE) - Centro de Informática. **GQM: Goal-Question-Metric** (Texto de Seminário). Disponível em: https://www.cin.ufpe.br/~scbs/metricas/seminarios/GQM_texto.pdf

> [4] Universidade de Brasília (UnB) - Faculdade do Gama (FGA). **Gerência: Goal Question Metric (GQM)**. (2019). Disponível em: https://fga-eps-mds.github.io/2019.1-Aix/gerencia/2019/04/19/gqm/