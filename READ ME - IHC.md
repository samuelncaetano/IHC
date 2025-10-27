# 📘 Guia Completo de Leitura, Notas e Relatórios no Obsidian

**Método Integrado: Leitura Ativa + Cornell + Zettelkasten + Síntese de Relatório**

---

## 🧭 Objetivo do Guia

Este documento ensina como ler, anotar e produzir relatórios a partir de livros usando o **Obsidian**.

O método combina estratégias clássicas de estudo com uma estrutura de templates em Markdown para organizar o conhecimento.

Ele se baseia em quatro pilares:

1. **Leitura Ativa (SQ3R)** → compreender profundamente o conteúdo
2. **Cornell Notes** → organizar visualmente as anotações
3. **Zettelkasten** → construir conexões entre ideias
4. **Síntese Final** → gerar relatórios bem estruturados e rastreáveis

---

## 🗂️ Estrutura Recomendada no Obsidian

Crie a seguinte estrutura no seu vault:

```bash
01 - Projects
├── IHC
│    ├── 01 - Leitura/
│    ├── 02 - Conceitos/
│    ├── 03 - Citações/
│    └── Relatório Final.md
└── 99 - Meta
     └── 00 - Templates
	      ├── (TEMPLATE) Chapter
	      ├── (TEMPLATE) Concept
	      ├── (TEMPLATE) Quote
	      └── (TEMPLATE) Final Summary
```

Cada pasta representa uma etapa do processo:

- **Leitura:** notas por capítulo
- **Conceitos:** ideias atômicas
- **Citações:** trechos relevantes
- **Relatório Final:** documento consolidado

---

## 📖 Etapas do Método

### 1. Leitura Ativa (SQ3R)

Método de leitura em cinco etapas:

| Etapa                     | Ação                                       |
| ------------------------- | ------------------------------------------ |
| **Survey (Explorar)**     | Ler sumário e entender o panorama do livro |
| **Question (Questionar)** | Criar perguntas antes de ler               |
| **Read (Ler)**            | Fazer anotações ativas                     |
| **Recite (Relembrar)**    | Escrever com suas palavras                 |
| **Review (Revisar)**      | Releitura e conexão entre ideias           |

---

### 2. Tomada de Notas com Cornell

O **template de capítulo** usa o formato Cornell para te ajudar a organizar as ideias.

| Ideias e exemplos               | Palavras-chave / Dúvidas           |
| ------------------------------- | ---------------------------------- |
| Explicações e exemplos práticos | Conceitos e perguntas a investigar |

Use a primeira coluna para **explicar** e a segunda para **questionar**.

No final, resuma em suas palavras — isso reforça a retenção do conteúdo.

---

### 3. Construção do Conhecimento com Zettelkasten

Cada ideia importante deve virar uma **nota atômica** com o template **Conceito.md**.

Essas notas são curtas, focadas e interconectadas.

**Regras básicas:**

- 1 conceito = 1 nota
- Nomeie claramente (ex: _Responsabilidade Única_)
- Use links (`[[Link]]`) para conectar ideias
- Relacione capítulos -> conceitos -> citações

Com o tempo, você terá uma **rede de conhecimento** navegável, formando o “mapa mental” do livro.

---

### 4. Registro de Citações

Citações são blocos de evidência e reflexão.

Use o template **Citação.md** para cada trecho que queira preservar.

- Inclua o texto original (entre aspas)
- Escreva um comentário pessoal
- Conecte a citação com o capítulo e conceito relacionado

---

### 5. Relatório Final

Por fim, use o **template Resumo Final.md** para escrever o relatório completo.

Ele será a síntese das notas e conexões criadas durante todo o processo.

**Estrutura do relatório:**

1. Introdução
2. Objetivo do estudo
3. Metodologia de leitura
4. Análise dos capítulos
5. Conceitos-chave
6. Interpretação crítica
7. Conclusão
8. Referências

Use links internos para conectar os capítulos e conceitos estudados.

O relatório será, na prática, **um documento vivo**, sustentado pelas suas notas.

---

## 🧠 Fluxo de Uso dos Templates

| Etapa             | Ação                | Template        |
| ----------------- | ------------------- | --------------- |
| Ler o capítulo    | Criar nota e anotar | Capítulo.md     |
| Extrair conceito  | Criar nota atômica  | Conceito.md     |
| Registrar citação | Guardar e comentar  | Citação.md      |
| Concluir o livro  | Escrever relatório  | Resumo Final.md |

---

## 📘 Exemplo Prático de Uso dos Templates

A seguir, um exemplo completo de como aplicar as técnicas e templates no estudo do livro

**_“Arquitetura Limpa”_ de Robert C. Martin**, focando no conceito de **Responsabilidade Única (SRP)**.

---

### 🔹 1. Etapa: Capítulo (Template `Capítulo.md`)

**Nota:** `01 - Leitura/Capítulo 7 - SRP.md`

```markdown
# 📘 Capítulo: O Princípio da Responsabilidade Única (SRP)

## Objetivo

> Entender o significado de “responsabilidade única” e sua importância no design de classes e módulos.

## Principais Conceitos

- [[Responsabilidade Única]]
- [[Coesão]]
- [[Acoplamento]]

## Anotações (Método Cornell)

| Ideias e exemplos                                | Palavras-chave / Dúvidas                |
| ------------------------------------------------ | --------------------------------------- |
| Uma classe deve ter apenas um motivo para mudar. | O que é considerado “motivo”?           |
| SRP melhora a manutenção e reduz dependências.   | Coesão e SRP são a mesma coisa?         |
| Exemplo: separar lógica de negócios e interface. | É possível violar SRP em microserviços? |

## Resumo

> O SRP defende que cada módulo tenha uma única responsabilidade.  
> Isso melhora o design, reduz o acoplamento e facilita a evolução do software.  
> O autor destaca que responsabilidade está ligada a **motivos de mudança**, não apenas a número de funções.

## Relações

- [[Capítulo 5 - Coesão]]
- [[Capítulo 8 - Acoplamento Baixo]]
```

---

### 🔹 2. Etapa: Conceito (Template `Conceito.md`)

**Nota:** `02 - Conceitos/Responsabilidade Única.md`

```markdown
# Conceito: Responsabilidade Única (SRP)

## Definição

Uma classe deve ter **apenas um motivo para mudar**, ou seja, representar uma **única responsabilidade**.

## Citação do autor

> “Um módulo deve ser responsável por uma, e apenas uma, parte da funcionalidade do sistema.”  
> — Robert C. Martin, _Arquitetura Limpa_, Cap. 7

## Interpretação

O SRP não fala apenas de funções, mas de **propósito e contexto**.  
Seguir esse princípio garante clareza e manutenção mais fácil.  
Aplicar SRP reduz o risco de alterações em cadeia no código.

## Relações

- Relacionado a: [[Coesão]], [[Acoplamento Baixo]]
- Citado em: [[Capítulo 7 - SRP]], [[Capítulo 8 - DIP]]

## Palavras-chave

#conceito #design #arquitetura #responsabilidade
```

---

### 🔹 3. Etapa: Citação (Template `Citação.md`)

**Nota:** `03 - Citações/Arquitetura é sobre intenções.md`

```markdown
# Citação

> “Arquitetura não é sobre frameworks, é sobre intenções.”  
> — Robert C. Martin, _Arquitetura Limpa_, Cap. 7

## Comentário

Essa frase reforça que princípios como SRP são ferramentas conceituais, não técnicas.  
Arquitetura é sobre **clareza de intenção**, não sobre ferramentas ou frameworks.

## Relações

[[Responsabilidade Única]]
[[Capítulo 7 - SRP]]
```

---

### 🔹 4. Etapa: Relatório Final (Template `Resumo Final.md`)

**Nota:** `Relatório Final.md`

```markdown
# Relatório Final — Arquitetura Limpa

## 1. Introdução

Este relatório apresenta os principais conceitos do livro _Arquitetura Limpa_ de Robert C. Martin, com foco nos princípios que sustentam a qualidade estrutural do software.

## 2. Objetivo

Compreender como princípios de design como SRP e DIP ajudam a construir sistemas flexíveis e de fácil manutenção.

## 3. Metodologia

Foi aplicada a leitura ativa (SQ3R), o método Cornell para anotações e o modelo Zettelkasten para conexões entre ideias no Obsidian.

## 4. Análise dos Capítulos

- [[Capítulo 7 - SRP]]
- [[Capítulo 8 - DIP]]
- [[Capítulo 9 - ISP]]

## 5. Conceitos-Chave

- [[Responsabilidade Única]]
- [[Coesão]]
- [[Acoplamento Baixo]]

## 6. Interpretação Crítica

Martin destaca que princípios arquiteturais são decisões sobre intenções e limites.  
O SRP se mostrou fundamental para compreender como a estrutura do software reflete responsabilidades humanas dentro do time.

## 7. Conclusão

O estudo demonstrou que a aplicação disciplinada dos princípios SOLID, especialmente o SRP, é essencial para criar sistemas duráveis e compreensíveis.

## 8. Referências

Martin, R. C. (2019). _Arquitetura Limpa_. Alta Books.
```

---

## 🧩 Resultado Final no Obsidian

Após aplicar as etapas, seu vault conterá:

```
Relatório - Arquitetura Limpa/
├── 01 - Leitura/
│   └── Capítulo 7 - SRP.md
├── 02 - Conceitos/
│   ├── Responsabilidade Única.md
│   ├── Coesão.md
│   └── Acoplamento.md
├── 03 - Citações/
│   └── Arquitetura é sobre intenções.md
├── 04 - Revisões/
│   └── Revisão Semana 2.md
└── Relatório Final.md
```

No **gráfico do Obsidian**, você verá:

- O capítulo conectado aos conceitos e citações.
- Conceitos conectados entre si.
- O relatório final como **nó central** da rede.
