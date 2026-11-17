# Caderno de estudos — Pós-graduação em IA e Aprendizagem de Máquina (Uninove)

## Visão geral

A pós-graduação é da Uninove e tem 10 disciplinas de 36 h cada, total de 360 h em 12 meses. Gestão de TI na Era da Indústria 4.0 está em andamento (C); as outras 9 estão a cursar (AC).

As seções seguem uma ordem de estudo sugerida: primeiro a base (Python, dados e estatística), depois os modelos e, no fim, a aplicação em projetos. Cada seção traz os temas, um espaço de anotação ao lado de cada tema, os pontos-chave e perguntas de revisão para as avaliações.

O acompanhamento de notas e datas de avaliação está em [acompanhamento.md](acompanhamento.md).

## 1. Gestão de TI na Era da Indústria 4.0 (cursando)

| Tema | Minhas anotações |
| --- | --- |
| Pilares da Indústria 4.0 (IoT industrial, sistemas ciberfísicos, nuvem, big data, IA, robótica, manufatura aditiva) | |
| Gêmeo digital | |
| Governança de TI (COBIT) e gestão de serviços (ITIL) | |
| Alinhamento TI × negócio e transformação digital | |
| Segurança da informação e LGPD | |
| Integração TI/TO (ERP, MES, SCADA) | |

**Pontos-chave:**

- A Indústria 4.0 conecta o chão de fábrica (TO) aos sistemas de gestão (TI) em tempo real.
- Governança define o que a TI deve entregar; gestão (ITIL) define como entregar serviços.
- Gêmeo digital é a réplica virtual de um ativo, alimentada por sensores, para simular e prever falhas.
- Segurança passa a incluir máquinas e redes industriais, não só escritório.

**Perguntas de revisão:**

1. Quais são os pilares da Indústria 4.0 e como cada um gera valor na produção?
2. Diferencie governança de TI (COBIT) e gestão de serviços (ITIL).
3. Por que a integração TI/TO é um desafio de segurança?
4. Dê um exemplo de uso de gêmeo digital na manutenção preditiva.

## 2. Introdução ao Python

| Tema | Minhas anotações |
| --- | --- |
| Tipos e variáveis | |
| Listas, tuplas, dicionários e conjuntos | |
| Condicionais e laços | |
| Funções, módulos e pip | |
| Leitura de arquivos e tratamento de erros | |
| Noções de orientação a objetos | |
| Jupyter / Colab | |

**Pontos-chave:**

- Lista é mutável, tupla é imutável; dicionário guarda pares chave–valor.
- List comprehension: `[x*2 for x in dados if x > 0]`.
- `try/except` evita que o programa pare num erro previsível.
- Bibliotecas centrais do curso: NumPy, pandas, Matplotlib, scikit-learn.

**Perguntas de revisão:**

1. Qual a diferença entre lista e tupla, e quando usar cada uma?
2. Escreva uma função que receba uma lista de números e devolva a média.
3. O que faz `with open("arquivo.csv") as f:` e por que usar `with`?
4. Como instalar e importar uma biblioteca externa?

## 3. Análise e Processamento de Dados

| Tema | Minhas anotações |
| --- | --- |
| pandas: DataFrame, filtros, groupby, merge | |
| Limpeza: valores ausentes, duplicados, outliers | |
| Transformação: normalização e codificação de categorias | |
| Análise exploratória (EDA) | |
| Visualização de dados | |
| Pipeline ETL | |

**Pontos-chave:**

- Cerca de 80% do trabalho com IA é preparar dados.
- Ausentes: remover linhas, preencher com média/mediana ou criar uma categoria "desconhecido".
- Normalizar (0 a 1) ou padronizar (média 0, desvio 1) antes de modelos sensíveis à escala.
- Codificação one-hot transforma categorias em colunas 0/1.

**Perguntas de revisão:**

1. Quais etapas compõem um pipeline ETL?
2. Como tratar valores ausentes numa coluna numérica e numa categórica?
3. Qual a diferença entre normalização e padronização?
4. O que um `df.groupby("setor")["custo"].mean()` retorna?

## 4. Estatística para IA e Aprendizagem de Máquina

| Tema | Minhas anotações |
| --- | --- |
| Estatística descritiva: média, mediana, desvio-padrão, quartis | |
| Probabilidade e teorema de Bayes | |
| Distribuições: normal e binomial | |
| Correlação × causalidade | |
| Amostragem | |
| Testes de hipótese e p-valor | |
| Regressão linear | |

**Pontos-chave:**

- Mediana resiste a outliers; média não.
- Correlação (r de −1 a 1) mede relação linear, não prova causa.
- Bayes: P(A|B) = P(B|A) · P(A) / P(B), base de classificadores como o Naive Bayes.
- p-valor < 0,05 costuma levar a rejeitar a hipótese nula.

**Perguntas de revisão:**

1. Quando a mediana descreve melhor os dados que a média?
2. Explique o teorema de Bayes com um exemplo de diagnóstico de falha.
3. O que significa um p-valor de 0,03?
4. Por que dividir os dados em treino e teste é uma questão estatística?

## 5. Arquitetura e Governança de Dados

| Tema | Minhas anotações |
| --- | --- |
| Bancos relacionais e SQL | |
| NoSQL | |
| Data warehouse, data lake e lakehouse | |
| Modelagem dimensional: fato e dimensão | |
| Qualidade, linhagem, catálogo e metadados | |
| Governança de dados (DAMA-DMBOK) | |
| LGPD e privacidade | |

**Pontos-chave:**

- Data warehouse guarda dados estruturados e tratados para relatórios; data lake guarda dados brutos de qualquer tipo.
- Governança define donos, regras e responsabilidades sobre os dados.
- Qualidade: completude, exatidão, consistência, atualidade.
- LGPD exige base legal, finalidade e segurança para dados pessoais.

**Perguntas de revisão:**

1. Compare data warehouse, data lake e lakehouse.
2. O que são tabelas fato e dimensão num modelo estrela?
3. Cite quatro dimensões da qualidade de dados.
4. Como a LGPD afeta um projeto de IA que usa dados de clientes?

## 6. Aprendizagem de Máquina e Visão Computacional

| Tema | Minhas anotações |
| --- | --- |
| Aprendizado supervisionado, não supervisionado e por reforço | |
| Regressão, árvores, random forest, SVM, k-means | |
| Overfitting e validação cruzada | |
| Métricas: acurácia, precisão, recall, F1 | |
| Redes neurais e CNNs | |
| Classificação, detecção e segmentação de imagens | |
| OpenCV e transfer learning | |

**Pontos-chave:**

- Overfitting: o modelo decora o treino e erra em dados novos. Combate: mais dados, regularização, validação cruzada.
- Em classes desbalanceadas, acurácia engana: olhe precisão, recall e F1.
- CNNs extraem padrões da imagem com filtros convolucionais.
- Transfer learning reaproveita um modelo pré-treinado e exige poucos dados.

**Perguntas de revisão:**

1. Diferencie aprendizado supervisionado e não supervisionado com exemplos.
2. O que é overfitting e como detectá-lo?
3. Num detector de defeitos com 1% de peças ruins, por que a acurácia não basta?
4. Diferencie classificação, detecção e segmentação de imagens.

## 7. Fundamentos de Modelagem, Simulação e Blockchain

| Tema | Minhas anotações |
| --- | --- |
| Modelagem de sistemas | |
| Simulação de eventos discretos | |
| Simulação de Monte Carlo | |
| Teoria das filas | |
| Validação de modelos | |
| Blockchain: blocos, hash, consenso | |
| Contratos inteligentes e rastreabilidade | |

**Pontos-chave:**

- Simulação testa cenários sem mexer no sistema real, como gargalos de uma linha de produção.
- Monte Carlo repete o modelo milhares de vezes com valores aleatórios para estimar riscos.
- Blockchain é um registro distribuído; cada bloco guarda o hash do anterior, o que torna alterações detectáveis.
- Contrato inteligente executa regras automaticamente quando as condições são cumpridas.

**Perguntas de revisão:**

1. Quando usar simulação em vez de um modelo analítico?
2. Como o método de Monte Carlo estima a probabilidade de atraso num projeto?
3. Por que o encadeamento por hash torna o blockchain resistente a fraude?
4. Dê um exemplo de blockchain na rastreabilidade de peças industriais.

## 8. Inteligência Artificial Generativa: Conceitos e Aplicações

| Tema | Minhas anotações |
| --- | --- |
| Modelos de linguagem (LLMs) e arquitetura transformer | |
| Tokens e janela de contexto | |
| Engenharia de prompt | |
| RAG: geração aumentada por recuperação | |
| Ajuste fino (fine-tuning) | |
| Modelos de imagem (difusão) | |
| Alucinação, viés, ética e direitos autorais | |

**Pontos-chave:**

- LLMs preveem o próximo token a partir do contexto; não "consultam" fatos, por isso podem alucinar.
- Bom prompt: contexto, tarefa clara, formato esperado e exemplos.
- RAG busca documentos da empresa e os entrega ao modelo, reduzindo alucinação.
- Ajuste fino muda o comportamento do modelo; RAG muda o conhecimento disponível.

**Perguntas de revisão:**

1. O que é alucinação e como reduzi-la num assistente corporativo?
2. Compare RAG e ajuste fino: quando usar cada um?
3. Monte um prompt para resumir relatórios de manutenção em 5 tópicos.
4. Cite dois riscos éticos da IA generativa e como mitigá-los.

## 9. Resolução de Problemas com IA e Aprendizagem de Máquina

| Tema | Minhas anotações |
| --- | --- |
| Do problema de negócio ao problema de ML | |
| Escolha do tipo de modelo | |
| Engenharia de atributos | |
| Ajuste de hiperparâmetros | |
| Interpretação de modelos (importância de variáveis, SHAP) | |
| Estudos de caso: demanda, manutenção preditiva, qualidade | |

**Pontos-chave:**

- Comece pela pergunta: "o que exatamente quero prever ou decidir?".
- Defina a métrica de sucesso de negócio antes da métrica do modelo.
- Um modelo simples que funciona bate um complexo que ninguém entende.
- Bons atributos (variáveis) costumam valer mais que um algoritmo melhor.

**Perguntas de revisão:**

1. Como transformar "reduzir paradas de máquina" num problema de ML?
2. Classificação ou regressão: prever falha em 7 dias e prever horas até a falha.
3. O que é engenharia de atributos? Dê dois exemplos com dados de sensores.
4. Por que a interpretabilidade importa num ambiente industrial?

## 10. Projetos de IA e Aprendizagem de Máquina

| Tema | Minhas anotações |
| --- | --- |
| Ciclo de vida de um projeto de IA (CRISP-DM) | |
| Escopo e KPIs | |
| Coleta e rotulagem de dados | |
| MLOps: versionamento, deploy, monitoramento | |
| Drift de dados | |
| Documentação e apresentação de resultados | |
| Projeto final | |

**Pontos-chave:**

- CRISP-DM: entendimento do negócio → dos dados → preparação → modelagem → avaliação → implantação.
- Um modelo em produção precisa de monitoramento: os dados mudam (drift) e a precisão cai.
- Mostre o resultado em linguagem de negócio: horas economizadas, custo evitado, defeitos reduzidos.
- Ideia de projeto final ligada ao trabalho: manutenção preditiva ou inspeção visual de produção.

**Perguntas de revisão:**

1. Descreva as 6 fases do CRISP-DM.
2. O que é drift de dados e como monitorá-lo?
3. Quais KPIs você usaria para provar o valor de um modelo de manutenção preditiva?
4. O que precisa estar documentado para outra pessoa reproduzir seu modelo?
