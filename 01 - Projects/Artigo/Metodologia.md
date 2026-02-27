# Metodologia

A presente investigação caracteriza-se como uma pesquisa de natureza aplicada estruturada segunda a abordagem de *Design Science Research* (DSR). O estudo combina procedimentos qualitativos e quantitativos, articulando inspeção por especialistas, coleta estruturada de percepção de usuários e técnicas de mineração de dados, no contexto da Interação Humano-Computador (IHC).

A articulação desses múltiplos procedimentos justifica-se pela necessidade de contornar as limitações recorrentes nos métodos tradicionais de avaliação. Na inspeção isolada por especialistas, por exemplo, destacam-se a subjetividade inerente ao processo e o** *expertise effect* — fenômeno documentado na literatura em que avaliadores menos experientes tendem a subnotificar problemas ou a aplicar diretrizes de forma puramente mecânica. A Avaliação Heurística (AH) ilustra bem esse desafio: embora seja vantajosa e popular sob o princípio de discount usability, o método carece de validação empírica sistemática. Portanto, a inclusão da percepção dos usuários e da mineração de dados surge para comprovar se as violações heurísticas identificadas pelos especialistas se traduzem, de fato, em barreiras reais na interação.

Diante desse cenário, o objetivo central deste estudo é conceber, desenvolver e demonstrar um artefato capaz de integrar diferentes fontes de evidência para apoiar a validação e a priorização de problemas de usabilidade. O artefato proposto consiste em um *framework* metodológico de triangulação que articula três dimensões: (i) inspeção heurística, visando o diagnóstico estrutural inicial das violações de interface; (ii) questionários estruturados *ad hoc*, derivados dos achados da inspeção, para capturar a percepção de uso empírica; e (iii) mineração de dados por regras de associação, empregando o algoritmo Apriori, para identificar padrões ocultos de co-ocorrência entre as dificuldades relatadas.

Alinhada ao ciclo da *Design Science Research* (DSR), a pesquisa compreende três fases interdependentes: (1) fundamentação teórica, (2) concepção e desenvolvimento do artefato e (3) demonstração e avaliação exploratória por meio de uma Prova de Conceito (*Proof of Concept* – PoC). A contribuição proposta situa-se no nível de método/artefato processual, ao oferecer um fluxo estruturado para triangulação sendo operacionalizada como o cruzamento sistemático entre os resultados da inspeção, as respostas dos questionários e as associações extraídas pela mineração de dados, com a finalidade de confirmar, priorizar ou complementar problemas de usabilidade identificados. A investigação foi orientada pela seguinte questão de pesquisa: **Em interfaces, de que modo a aplicação de regras de associação sobre dados de questionários *ad hoc* pode complementar a Avaliação Heurística na validação de violações previstas e na identificação de problemas emergentes?**

Ressalta-se que, por se tratar de uma PoC, o escopo metodológico concentra-se em propor e operacionalizar o *framework* em um contexto real, e não em produzir generalizações estatísticas irrestritas. Os resultados obtidos fornecem evidências preliminares de viabilidade técnica. Os procedimentos que compõem o delineamento desta investigação são detalhados a seguir.

## Fase 1 – Fundamentação Teórica (Revisão Sistemática da Literatura)

A fundamentação do artefato foi sustentada por uma Revisão Sistemática da Literatura conduzida para mapear o estado da arte na integração entre métodos de avaliação de usabilidade e técnicas de descoberta de padrões. O protocolo seguiu as recomendações do PRISMA, assegurando transparência e rastreabilidade ao processo de identificação, triagem e seleção dos estudos.

A estratégia de busca foi estruturada com base no modelo PICO, adaptada ao contexto metodológico da pesquisa. A população (P) foi definida como estudos relacionados à Interação Humano-Computador e avaliação de usabilidade em interfaces. A intervenção (I) correspondeu ao uso de técnicas de mineração de dados e análises estatísticas aplicadas à avaliação de usabilidade. O comparador (C), quando presente, envolveu métodos tradicionais de inspeção, como Avaliação Heurística ou revisão por especialistas. Os resultados (O) incluíram evidências de validação empírica, identificação de padrões, confiabilidade de instrumentos e integração metodológica entre abordagens qualitativas e quantitativas.

As buscas foram realizadas nas bases IEEE Xplore, Springer, Science Direct, Google Scholar e Periódicos Capes, a partir de *strings* elaboradas por meio de combinações de descritores relacionados a IHC, avaliação heurística, confiabilidade de questionários, correlação estatística e mineração de dados por regras de associação. As *strings* foram formuladas com operadores booleanos e aplicadas de forma padronizada entre as bases.

Foram incluídos estudos que abordassem avaliação de usabilidade por métodos qualitativos, quantitativos ou mistos; que empregassem inspeção por especialistas ou instrumentos estruturados; que aplicassem técnicas estatísticas ou de mineração de dados com detalhamento analítico; ou que apresentassem contribuições metodológicas transferíveis ao contexto da IHC. Foram excluídos trabalhos sem avaliação empírica, sem detalhamento metodológico suficiente, restritos a aspectos exclusivamente técnicos sem análise de uso ou indisponíveis em texto completo revisado por pares. Estudos de áreas externas à IHC foram considerados apenas quando ofereciam contribuições metodológicas comparáveis.

O processo de seleção seguiu as etapas de identificação, triagem, elegibilidade e inclusão, conforme o fluxo PRISMA. O quantitativo de estudos recuperados por eixo temático foi registrado na fase de identificação, seguido de remoção de duplicatas, leitura de títulos e resumos e análise integral dos textos elegíveis. A síntese dos estudos incluídos permitiu identificar lacunas relacionadas à validação cruzada de inspeções heurísticas com dados empíricos de usuários e ao uso sistemático de mineração de dados para apoiar a interpretação de problemas de usabilidade.

A partir dessa síntese, foram derivados os seguintes requisitos para o artefato: (i) integrar avaliação especializada e percepção do usuário; (ii) permitir análise estruturada de co-ocorrência de dificuldades; (iii) oferecer critérios objetivos para priorização de problemas; e (iv) manter aplicabilidade em contextos de amostras reduzidas. Esses requisitos orientaram a fase de concepção do *framework*.

## 3.3 Fase 2: Concepção e Desenvolvimento do Artefato

### Avaliação Heurística

A operacionalização do *framework* teve início com a aplicação da Avaliação Heurística, baseada nas dez heurísticas de usabilidade propostas por Nielsen. O procedimento contou com seis avaliadores independentes, que registraram e classificaram individualmente as violações de interface e seus respectivos níveis de severidade. Em seguida, as discrepâncias inter-avaliadores foram submetidas a uma sessão de consolidação. Essa etapa foi mediada por um avaliador sênior e conduzida até a obtenção de consenso, visando reduzir a variabilidade diagnóstica entre os especialistas.

### Questionário *ad hoc*

Os resultados obtidos na AH serviram como base para a construção de um questionário *ad hoc*. O instrumento foi concebido com o propósito específico de validar os achados da inspeção, assumindo, portanto, uma natureza confirmatória/complementar, sem a pretensão de mapear exaustivamente todo o espectro de problemas de usabilidade do sistema.

O questionário foi composto por itens binários (presença ou ausência de dificuldade na execução das tarefas) e itens estruturados em escala Likert de cinco pontos. A consistência interna do instrumento foi atestada mediante o cálculo do Alfa de Cronbach (α = 0,81). Como evidência adicional de coerência entre os itens conceitualmente relacionados foi examinada mediante correlações de Pearson.

### Pré-processamento dos dados

Para viabilizar a aplicação do algoritmo Apriori, as respostas coletadas foram convertidas para um formato transacional binário. Os itens originalmente binários foram mantidos em sua forma bruta, enquanto os itens baseados na escala Likert passaram por um processo de discretização, pautado em limiares semânticos previamente estabelecidos (valores ≤ 2 ou ≤ 3 indicando ausência de dificuldade; valores superiores indicando presença de dificuldade). Registros que apresentavam dados faltantes essenciais foram excluídos da base.

### Extração de Regras de Associação (Apriori) e Análise de Sensibilidade

A etapa de mineração empregou o algoritmo Apriori, executado por meio da biblioteca *mlxtend* da linguagem Python. A técnica foi aplicada com caráter exclusivamente exploratório e descritivo, com foco na identificação de associações e co-ocorrências entre os dados, sem inferência de relações causais.

Os parâmetros iniciais de extração foram definidos em: suporte mínimo de 10%, confiança mínima de 60%, *lift* > 1 e *conviction* > 1. A avaliação das regras geradas baseou-se nessas quatro métricas (*support*, *confidence*, *lift* e *conviction*), sendo retidas apenas as associações que demonstraram dependência positiva.

==Para garantir a robustez dos achados, conduziu-se uma análise de sensibilidade sistemática, variando-se as métricas de suporte (entre 10% e 20%) e confiança (entre 60% e 70%). Priorizou-se a seleção de regras que se mantiveram estáveis em múltiplas configurações paramétricas.== <- Procurar referências bibliotecas para validar a afirmação.

==Essa prática mitigou a dependência estrita dos parâmetros iniciais, um procedimento metodologicamente recomendado para cenários analíticos caracterizados por amostras reduzidas (*small data*).== <- Procurar referências bibliotecas para validar a afirmação, se existir, caso contrário excluir a frase.

Essa fase corresponde ao núcleo construtivo da DSR, no qual o artefato foi concebido, implementado e preparado para demonstração em contexto real.

## 3.4 Fase 3: Demonstração e Avaliação do Artefato (Prova de Conceito)

### Participantes

A execução do estudo de caso envolveu dois grupos distintos. O grupo de avaliadores foi composto por sete especialistas em IHC (seis estudantes pesquisadores e um docente sênior). O grupo de usuários finais contou com 18 estudantes de graduação, com média de idade de 22,4 anos.

O recrutamento dos participantes foi pautado em critérios de disponibilidade e familiaridade prévia com o domínio da aplicação avaliada, realizado em um contexto acadêmico e sem a oferta de incentivos financeiros. Embora tais fatores tenham delimitado a dimensão da amostra, o caráter exploratório e de Prova de Conceito da pesquisa dispensa a necessidade de representatividade estatística.

### Protocolo Experimental

==Durante o experimento, os participantes responderam ao questionário *ad hoc* estruturado na fase anterior com base em capturas de tela representativas do sistema avaliado. O instrumento permaneceu aberto por um período de um mês, sem acompanhamento síncrono dos pesquisadores, razão pela qual não houve execução controlada de tarefas no momento da coleta de dados; para assegurar a validade das respostas, foram selecionados exclusivamente usuários com experiência prévia de uso do sistema.==

Cada item do instrumento de coleta foi composto por três elementos integrados:

1. **Estímulo visual:** uma captura de tela (*screenshot*) do estado do sistema correspondente à funcionalidade analisada;
2. **Pergunta contextualizada:** uma formulação que exigia do participante a interpretação da interface ou a identificação da ação correta a ser tomada;
3. **Resposta:** categorizada de forma binária ou em escala Likert de cinco pontos, conforme a natureza da variável investigada.

O questionário não impôs limite de tempo imediato, permanecendo aberto por um período predefinido. Isso permitiu que os usuários respondessem de forma reflexiva com base em sua experiência prévia de interação, garantindo o registro de dados completos e consistentes. O protocolo possibilitou capturar a percepção empírica do usuário frente a estados específicos da interface, assegurando o alinhamento com os apontamentos da inspeção heurística e a viabilidade da análise transacional pelo algoritmo Apriori.

### Critérios de Utilidade do Artefato

Em conformidade com os preceitos da DSR, a avaliação do *framework* baseou-se em critérios de utilidade preestabelecidos, voltados à verificação de sua viabilidade e capacidade diagnóstica exploratória: (i) execução completa do fluxo metodológico proposto; (ii) interpretabilidade das regras de associação geradas; (iii) convergência parcial entre violações identificadas na Avaliação Heurística e dificuldades relatadas pelos usuários; e (iv) identificação de associações adicionais não previstas explicitamente pelos especialistas. Esses critérios foram analisados de forma exploratória, coerente com o escopo de Prova de Conceito.
