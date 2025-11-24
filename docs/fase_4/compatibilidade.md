# Resultados dos Testes de Compatibilidade

Esta seção descreve os testes realizados e resultados obtidos com base nos **Casos de Teste (CTs)** projetados para avaliar a característica de **Compatibilidade** do Aprender 3, conforme planejamento realizado na Fase 3.

---

# CT-COMP-01: Sincronia de Status de Conclusão

## Informações do Teste
- **Questão GQM:** Q1 – Sincronia de Dados  
- **Métrica:** 1.1 – Percentual de Discrepância  
- **Hipótese:** H1.1 – Possível inconsistência Web × App  
- **Perfil:** Discente  

## Ambiente
- **Web:** Aprender 3 (Linux Ubuntu 24.04)  
- **App:** Moodle 5.0.0 – S24 (Android 16)  
- **Conexão:** Dados móveis (emulado)

## Execução
Foram avaliadas **atividades** com rastreamento de conclusão.  
Passos: marcar na Web → sincronizar App → comparar status.

## Resultados

| Atividades | Discrepâncias | Percentual |
|------------|---------------|------------|
| 10         | 0             | **0%**     |

### Fórmula

Discrepância = (0 / 10) × 100 = 0%


### Classificação (Métrica 1.1)
**EXCELENTE** (0% a 5%)

---

# CT-COMP-02: Sincronização Bidirecional de Arquivos

## Informações do Teste
- **Questão GQM:** Q1 – Sincronia de Dados  
- **Métrica:** 1.2 – Taxa de Sucesso de Sincronização  
- **Hipótese:** H1.2 – Possíveis falhas na sincronização Web ↔ App  
- **Perfil:** Discente  

## Ambiente
- Mesmo do CT-COMP-01  
- Arquivos: PDF, MD

## Execução

### Web → App
- **1 arquivo enviados via Web**
- Resultado: **1/1 sincronizados**

### App → Web
- **1 arquivo enviados via App**
- Resultado: **1/1 sincronizados**

## Resultados Consolidados

| Direção     | Sucesso | Total | Taxa  |
|-------------|---------|-------|-------|
| Web → App   | 1       | 1     | 100%  |
| App → Web   | 1       | 1     | 100%  |

### Fórmula

Taxa de Sucesso = (2/2) × 100 = 100%


### Classificação (Métrica 1.2)
**EXCELENTE** (> 90%)


O video da execução do teste está disponível a seguir:

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
        src="https://www.youtube.com/embed/IcZVN-WvuPE"
        style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
        allowfullscreen>
    </iframe>
</div>


## Resumo dos Resultados

### Métricas Avaliadas

| Métrica       | Descrição                                       | Resultado          | Classificação |
| ------------- | ----------------------------------------------- | ------------------ | ------------- |
| **CT-COMP-01**| Sincronia de Status de Conclusão                | 0% discrepâncias   | **Excelente** |
| **CT-COMP-02**| Sincronização Bidirecional de Arquivos          | 100% sincronização | **Excelente** |

---

## Histórico de Versões

| Versão | Data       | Descrição                               | Autor                                  |
| :----: | ---------- | --------------------------------------- | -------------------------------------- |
| `1.0`  | 24/11/2025 | Criação da página | [Felipe Hansen](https://github.com/FHansen98) |
| `1.1`  | 23/11/2025 | Adição do CT-COM-01 e CT-COM-02 | [Thales Germano](https://github.com/thalesgvl) |

