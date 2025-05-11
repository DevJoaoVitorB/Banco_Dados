# 🧱 Construção do Modelo ER

> A construção de um modelo ER (Entidade-Relacionamento) é uma etapa fundamental na modelagem conceitual de bancos de dados. Envolve decisões importantes sobre a representação dos dados, escolha dos elementos e validações necessárias para garantir consistência e clareza.

<br>

## 📋 Propriedades do Modelo ER

### ⚙️ Formalidade

> O modelo ER é um **modelo formal**, com notação padronizada e base teórica sólida.

- Pode ser processado por **ferramentas CASE** (*Computer-Aided Software Engineering*) que geram **modelos relacionais** automaticamente a partir dos diagramas ER.
- Deve ser claro e compreendido por **todos os envolvidos** no projeto, incluindo analistas, desenvolvedores e usuários.

<br>

### 🚫 Limitações

> Apesar de poderoso, o modelo ER possui **limitações**.

- Representa **apenas os aspectos conceituais essenciais** dos dados.
- **Nem todas as restrições de integridade** podem ser representadas diretamente.
- ❗ *Exemplo de limitação:*  
  Uma **restrição de integridade recursiva** como:  
  > “Um empregado pode ser supervisionado por outro que, por sua vez, também é supervisionado por outro”  
  é difícil de representar apenas com relacionamentos no modelo ER.

<br>

### 🔄 Equivalência

> Modelos ER diferentes podem ser **equivalentes** entre si.

- Dois modelos ER distintos podem gerar **o mesmo modelo relacional** ao serem convertidos.
- Isso é possível desde que **sigam corretamente as regras de transformação** do modelo conceitual para o lógico.

<br>

## 🎯 Critérios para Escolha dos Elementos

> Decisões importantes devem ser tomadas ao definir **o que será modelado como entidade, atributo ou relacionamento**.

<br>

### 🔎 Identificação dos Elementos

- Perguntas como:  
  **“Quando algo deve ser uma entidade e não um atributo?”**  
  ajudam a direcionar a modelagem.
- O **contexto da aplicação** e a **lógica de negócio** são essenciais para essa decisão.
- O objeto isoladamente **não define sua representação** — é preciso considerar seu papel no sistema.

<br>

### 🧱 Entidade vs. Atributo

- Uma **entidade** deve ser usada quando o item:
  - Pode possuir **relacionamentos próprios**;
  - Possui **várias propriedades** (atributos).

- 💡 *Exemplo de análise:*  
  Vale a pena modelar a **cor** de um automóvel como atributo ou como entidade?  
  > Como atributo: simples e direto.  
  > Como entidade: caso tenha relacionamentos ou propriedades próprias (ex: código da cor, tipo, fabricante).

<br>

### 🧬 Atributo vs. Generalização/Especialização

- Utilize **generalização/especialização** quando as **subentidades possuem propriedades específicas**.
- Evita o uso excessivo de **atributos opcionais**, que podem ocultar diferenças importantes.

- 💡 *Exemplo de análise:*  
  Se **empregados de diferentes categorias funcionais** (ex: técnico, gerente) possuem **atributos distintos**, o ideal é usar generalização/especialização.

<br>

### 📎 Atributo Multivalorado vs. Entidade

- **Atributos multivalorados** (como telefones ou e-mails) **não são diretamente representáveis** no modelo relacional.
- Devem ser transformados em **entidades relacionadas**.

- 💡 *Exemplo de análise:*  
  O atributo "telefone" da entidade **Pessoa** pode ser modelado como uma **nova entidade Telefone**, com relacionamento com Pessoa.

<br>

## ✅ Verificação do Modelo

> Após construído, o modelo ER deve ser **verificado** e **validado**.

### 🧪 Requisitos de Validação

- **✔️ Correto**: Sem erros de sintaxe ou significado.
- **🧩 Completo**: Todos os requisitos do cliente foram modelados.
- **♻️ Livre de Redundâncias**: Evitar repetição de dados ou entidades.
- **⏳ Temporalidade**: Considere a evolução dos dados no tempo (atributos que mudam).
- **⚠️ Entidades sem atributos ou isoladas**: Só devem ser usadas em casos muito específicos e justificados.

<br>

## 🛠️ Estratégias de Modelagem

> O processo de construção do modelo ER é **incremental e iterativo**.