# COMO ORGANIZO MINHAS IDEIAS E TAREFAS

Este documento descreve a estrutura de pastas e o fluxo de trabalho utilizados neste vault do Obsidian. O objetivo é combinar a organização orientada à ação do método **PARA** (Projetos, Áreas, Recursos, Arquivos) com o poder de construção de conhecimento do **Zettelkasten**. A numeração das pastas (`00`, `01`, etc.) garante uma ordem visual consistente no explorador de arquivos.

---

## A estrutura de pastas

### `00 - Maps of Content`

- **Propósito**: Esta pasta serve como o índice principal do seu conhecimento. Um "Map of Content" (MOC) é uma nota que funciona como um hub, agregando links para diversas outras notas sobre um tópico específico.
- **Método**: Conceito-chave do Zettelkasten.
- **Como usar**: Quando você percebe que várias notas permanentes (`04 - Permanent`) se conectam em torno de um grande tema (ex: "Inteligência Artificial", "Filosofia Estoica", "Compiladores"), você cria um MOC para estruturar e navegar por essas ideias. É o seu ponto de entrada para explorar um assunto.
- **Exemplos de notas**: `MOC - Sistemas Operacionais`, `MOC - Desenvolvimento de Carreira`.

### `01 - Projects`

- **Propósito**: Conter todas as notas e materiais relacionados a projetos específicos com um objetivo claro e um prazo definido.
- **Método**: **P**rojects do PARA.
- **Como usar**: Cada subpasta ou conjunto de notas aqui representa algo em que você está trabalhando ativamente.
- **Exemplos de notas**: `TCC - Compilador C++`, `Planejamento Viagem de Férias`, `Artigo Científico sobre Algoritmos de Deadlock`.

### `02 - Areas`

- **Propósito**: Gerenciar áreas de responsabilidade contínua na sua vida que não têm um fim definido, mas exigem um padrão de manutenção.
- **Método**: **A**reas do PARA.
- **Como usar**: São as grandes esferas da sua vida. As notas aqui servem como painéis de controle, listas de revisão e registros de progresso.
- **Exemplos de notas**: `Saúde e Fitness`, `Finanças Pessoais`, `Desenvolvimento Profissional`, `Relacionamentos`.

### `03 - Resources`

- **Propósito**: Armazenar informações de interesse geral e notas sobre conteúdos que você consome. É a sua biblioteca pessoal.
- **Método**: **R**esources do PARA e "Notas de Literatura" do Zettelkasten.
- **Como usar**: Quando você lê um livro, assiste a um vídeo ou encontra um artigo interessante, as notas que você tira sobre esse conteúdo vão para cá. Elas ainda não são suas próprias ideias, mas sim o material bruto que as alimentará.
- **Exemplos de notas**: `Notas do Livro - Clean Architecture`, `Resumo do Artigo sobre Telomerase`, `Clipping de Website - Tutorial de Rust`.

### `04 - Permanent`

- **Propósito**: O coração do seu Zettelkasten. Esta pasta contém as "Notas Permanentes" (ou "Zettels"). Cada nota é uma ideia única, atômica, escrita com suas próprias palavras e densamente conectada a outras notas.
- **Método**: "Notas Permanentes" do Zettelkasten.
- **Como usar**: Após processar as notas em `05 - Fleeting` e `03 - Resources`, você sintetiza os aprendizados em notas permanentes. O nome do arquivo idealmente contém um timestamp para garantir um ID único (ex: `202510162000`). O poder desta pasta vem da criação de links `[[outra nota]]` entre as ideias.
- **Exemplos de notas**: `[[202510162001]] A sobrecarga de operadores em C++ aumenta a expressividade do código`, `[[202510162005]] O Algoritmo do Avestruz ignora deadlocks por considerá-los eventos raros`.

### `05 - Fleeting`

- **Propósito**: A caixa de entrada do seu sistema. Aqui você captura pensamentos rápidos, ideias aleatórias e insights momentâneos que ocorrem ao longo do dia.
- **Método**: "Notas Passageiras" do Zettelkasten.
- **Como usar**: Use esta pasta para anotar rapidamente qualquer coisa que vier à mente. A regra é processar essas notas regularmente: transforme-as em notas permanentes, tarefas de projeto, ou simplesmente delete-as. A caixa de entrada deve ser esvaziada com frequência.
- **Exemplos de notas**: `Ideia para o TCC`, `Lembrar de pesquisar sobre Norbert Elias`, `Insight sobre a série que estou assistindo`.

### `06 - Daily`

- **Propósito**: Manter um registro temporal de atividades, planos e reflexões. É a sua seção de journaling e planejamento.
- **Método**: Prática comum de PKM (Personal Knowledge Management).
- **Subpastas**:
    - `06 - Daily/01 - Day`: Para notas diárias. Ideal para registrar o que você fez, aprendeu ou pensou em um dia específico.
    - `06 - Daily/02 - Week`: Para revisões semanais, planejamento da semana seguinte e acompanhamento de metas semanais.
    - `06 - Daily/03 - Month`: Para planejamento e revisão mensal, definindo objetivos maiores.

### `07 - Archives`

- **Propósito**: Armazenar itens inativos das outras categorias. É o seu "arquivo morto".
- **Método**: **A**rchives do PARA.
- **Como usar**: Quando um projeto de `01 - Projects` é concluído, uma área de `02 - Areas` se torna irrelevante ou um recurso de `03 - Resources` não é mais útil, você os move para cá. Isso mantém suas pastas ativas limpas e focadas.

### `99 - Meta`

- **Propósito**: Pasta de suporte para o funcionamento do vault. Não contém conteúdo principal, mas sim os bastidores do seu sistema.
- **Método**: Organização de sistema.
- **Subpastas**:
    - `99 - Meta/00 - Templates`: Contém modelos de notas (templates) para agilizar a criação de notas diárias, revisões semanais, notas de livros, etc.
    - `99 - Meta/Attachments`: Local padrão para onde o Obsidian salva imagens, PDFs e outros anexos, mantendo as outras pastas limpas.
    - `99 - Meta/Preloaded Classes`: Pode ser usada para configurações específicas de plugins, como classes CSS para estilização ou scripts para plugins como Dataview.

---

## Fluxo de trabalho integrado

1.  **Captura**: Uma ideia surge -> Crie uma nota em `05 - Fleeting`.
2.  **Consumo**: Você lê um artigo -> Crie uma nota de resumo em `03 - Resources`.
3.  **Processamento (Diário/Semanal)**: Revise o conteúdo de `05 - Fleeting` e `03 - Resources`.
4.  **Síntese**: Para cada ideia valiosa, crie uma **Nota Permanente** em `04 - Permanent`, escrita com suas palavras. O mais importante: **crie links** para outras notas permanentes relacionadas.
5.  **Estruturação**: Conforme sua rede de notas em `04 - Permanent` cresce, crie ou atualize um `00 - Map of Content` para organizar as ideias sobre um tópico.
6.  **Ação**: Se uma ideia gera uma tarefa ou projeto, crie as notas necessárias em `01 - Projects` ou `02 - Areas`, lincando de volta às notas permanentes que forneceram o conhecimento.
7.  **Arquivamento**: Quando um projeto em `01 - Projects` terminar, mova a pasta correspondente para `07 - Archives`.

Este sistema permite que você tenha um fluxo claro desde a captura de uma ideia até sua aplicação prática, ao mesmo tempo em que constrói uma base de conhecimento interconectada e duradoura.
