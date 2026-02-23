# Texto v5

## 3.1 Classificação e Delineamento da Pesquisa

A presente investigação caracteriza-se como uma pesquisa de **natureza aplicada**, conduzida sob a estratégia metodológica de **Design Science Research (DSR)**. O estudo adota **abordagem de métodos mistos (_mixed methods_)**, integrando procedimentos qualitativos de inspeção por especialistas e análises quantitativas de dados empíricos no contexto de **Interação Humano-Computador (IHC)**.

A natureza aplicada decorre da finalidade prática de mitigar desafios persistentes na avaliação de sistemas interativos, notadamente a **subjetividade inerente aos métodos de inspeção** e o denominado **expertise effect**, no qual avaliadores menos experientes tendem a identificar menos problemas ou a aplicar heurísticas de forma mecânica. Embora a **Avaliação Heurística (AH)** seja amplamente reconhecida pela eficiência diagnóstica, ela carece de validação empírica sistemática acerca de como as violações previstas impactam a experiência real do usuário.

Nesse contexto, a pesquisa assume **caráter exploratório e avaliativo**, investigando a viabilidade de uma **triangulação metodológica** entre inspeção especializada, percepção do usuário e técnicas algorítmicas de descoberta de padrões.

Sob a perspectiva da DSR, a investigação orientou-se à **concepção, desenvolvimento e avaliação de um artefato**, materializado em um _framework_ que integra três fontes complementares de evidência:

1. **Inspeção Heurística**, para diagnóstico inicial de violações de usabilidade;
2. **Questionários estruturados _ad hoc_**, para capturar a percepção subjetiva dos usuários;
3. **Mineração de dados por regras de associação (Algoritmo Apriori)**, para identificar padrões de co-ocorrência entre dificuldades relatadas.

Neste estudo, **triangulação metodológica** é definida operacionalmente como o **cruzamento sistemático entre achados da inspeção, respostas do questionário e associações extraídas por mineração de dados**, com a finalidade de **confirmar, priorizar ou complementar** problemas de usabilidade.

A investigação foi guiada pela seguinte questão de pesquisa:

> **RQ:** Em interfaces móveis, de que maneira a aplicação de regras de associação (Algoritmo Apriori) sobre dados de questionários _ad hoc_ pode complementar a Avaliação Heurística para validar violações previstas e identificar problemas emergentes?

Ressalta-se explicitamente que o estudo constitui uma **Prova de Conceito (Proof of Concept – PoC)**. Assim, o objetivo central é **propor e operacionalizar o framework**, e não validá-lo de forma confirmatória ou produzir generalizações estatísticas. Os resultados devem ser interpretados como **evidências preliminares de viabilidade técnica**.

O delineamento foi organizado em três fases progressivas e complementares.

---

## 3.2 Fase 1 – Fundamentação Teórica (Revisão Sistemática da Literatura)

Realizou-se uma **Revisão Sistemática da Literatura**, conduzida conforme diretrizes estruturadas de busca, seleção e síntese, com o objetivo de mapear o estado da arte na integração entre métodos de inspeção de usabilidade e técnicas de descoberta de padrões.

Os achados dessa etapa subsidiaram:

- a definição dos componentes do artefato;
- a seleção do algoritmo de mineração de dados;
- a construção do protocolo experimental;
- a identificação de lacunas metodológicas relacionadas à validação cruzada de inspeções heurísticas.

---

## 3.3 Fase 2 – Proposição do Framework

### Avaliação Heurística

Inicialmente, aplicou-se a **Avaliação Heurística** com base nas **dez heurísticas de Nielsen**. Sete avaliadores independentes registraram violações e níveis de severidade individualmente. Posteriormente, as discrepâncias foram discutidas em sessão de consolidação mediada por avaliador sênior até consenso, reduzindo variabilidade interavaliador.

### Questionário _ad hoc_

Os resultados da AH fundamentaram a construção de um **questionário _ad hoc_**.

Destaca-se que o instrumento foi concebido **explicitamente para validar e triangular empiricamente os achados da AH**, não tendo como objetivo mapear exaustivamente todo o espectro de problemas de usabilidade. Seução, portanto, confirmatória-complementar.

O questionário incluiu:

- itens binários (presença/ausência de dificuldade);
- itens em escala Likert de cinco pontos.

A consistência interna foi verificada por **Alfa de Cronbach (α = 0,81)**. **Correlações de Pearson** foram empregadas como evidência adicional de coerência entre itens conceitualmente relacionados.

### Pré-processamento dos dados

Para aplicação do Apriori, as respostas foram convertidas para formato transacional binário.

- itens binários: mantidos conforme resposta;
- itens Likert: discretizados segundo limiares semânticos previamente definidos (tipicamente ≤ 2 ou ≤ 3 = ausência; valores superiores = presença).

Registros com dados faltantes essenciais foram removidos. Análises de sensibilidade verificaram que tal exclusão não alterou substancialmente os padrões observados.

### Regras de associação (Apriori)

Aplicou-se o **algoritmo Apriori (biblioteca _mlxtend_, Python)** com **caráter exclusivamente exploratório e descritivo**, buscando identificar **associações e co-ocorrências**, não relações causais.

Parâmetros iniciais:

- suporte mínimo = 10%
- confiança mínima = 60%
- lift > 1
- conviction > 1

As regras foram avaliadas por **support, confidence, lift e conviction**, mantendo-se apenas associações com dependência positiva.

### Análise de sensibilidade

Realizou-se **análise de sensibilidade sistemática**, variando suporte (10–20%) e confiança (60–70%). Regras estáveis em múltiplas configurações foram priorizadas, reduzindo dependência paramétrica — prática recomendada para cenários de _small data_.

---

## 3.4 Fase 3 – Estudo de Caso (Prova de Conceito)

### Participantes

O estudo envolveu dois grupos.

**Avaliadores:** sete especialistas (seis estudantes pesquisadores e um docente sênior).  
**Usuários finais:** 18 estudantes de graduação (idade média = 22,4 anos).

O recrutamento foi condicionado à disponibilidade e aos critérios de familiaridade com o domínio do sistema, em contexto acadêmico sem incentivos financeiros, limitando a dimensão amostral.

Entretanto, considerando o **caráter exploratório/PoC**, não se buscou representatividade estatística, sendo amostras reduzidas adequadas para avaliações formativas de usabilidade.

Os resultados são válidos especificamente para esse perfil, não generalizáveis à população ampla. Estudos futuros devem incluir usuários leigos e amostras maiores.

### Protocolo Experimental

Os participantes realizaram **tarefas representativas** no sistema avaliado e, ao término de cada tarefa, responderam a um **questionário _ad hoc_** estruturado para validar os achados da Avaliação Heurística (AH).

Cada item do questionário foi composto por:

1. **Estímulo visual:** uma captura de tela do sistema relacionada à tarefa executada;
2. **Pergunta contextualizada:** exigindo que o participante interpretasse a interface ou identificasse a ação correta;
3. **Resposta:** podendo ser **binária** (presença/ausência de dificuldade) ou em **escala Likert de cinco pontos**, dependendo da natureza da pergunta.

O questionário permaneceu **aberto por um período pré-definido**, permitindo que os participantes respondessem após a execução da tarefa, sem imposição de tempo imediato de resposta. Após esse intervalo, o questionário foi fechado, garantindo o registro de respostas completas e consistentes.

Essa abordagem permitiu capturar **a percepção do usuário em relação a cada estado da interface**, mantendo coerência com os achados da inspeção heurística e compatibilidade com a análise de regras de associação (Apriori).

### Critérios de utilidade do artefato

Os critérios de utilidade do artefato foram estabelecidos para **avaliar a viabilidade e a capacidade diagnóstica exploratória** do framework:

1. **Exequibilidade do fluxo metodológico:** avaliação de se todos os passos planejados puderam ser executados conforme o protocolo;
2. **Interpretabilidade das regras:** análise da clareza e compreensão das regras de associação geradas (considerando suporte, confiança, lift e conviction);
3. **Grau de concordância entre AH e respostas dos usuários:** observação de convergência parcial, sugerindo consistência entre avaliação de especialistas e percepção dos usuários;
4. **Identificação de associações adicionais:** detecção de padrões emergentes não explicitamente previstos pelos avaliadores, indicando complementaridade potencial na interpretação de problemas de usabilidade.

Ressalta-se que todos os critérios **foram avaliados de forma exploratória**, gerando **evidências preliminares de viabilidade técnica** e não constituindo validação definitiva do framework.

---

## 3.6 Considerações Finais do Método

O método proposto foi implementado integralmente e produziu **evidências preliminares de viabilidade técnica**. Os resultados **sugerem complementaridade** entre inspeção heurística, percepção do usuário e mineração de dados. Todavia, tais achados **não configuram validação definitiva do framework**, exigindo estudos adicionais para confirmação externa.
