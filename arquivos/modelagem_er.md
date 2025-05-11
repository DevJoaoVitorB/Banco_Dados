# 🧩 Modelagem Entidade-Relacionamento (ER)

> A modelagem ER (Entidade-Relacionamento) é uma técnica de modelagem conceitual utilizada para representar a estrutura lógica dos dados em um Banco de Dados, independentemente da forma como será implementado. Utiliza entidades, relacionamentos e atributos para descrever o mundo real, facilitando a comunicação entre os analistas e os usuários finais.

<br>

## 📐 Modelos de Dados

### 🔍 O que são Modelos de Dados?

> Um **modelo de dados** é um conjunto de conceitos usados para descrever a **estrutura**, os **relacionamentos** e as **restrições** de um Banco de Dados. Pode ser utilizado em diferentes níveis de abstração, servindo como base para o desenvolvimento e a manutenção de sistemas de informação.

<br>

### 🧭 Categorias de Modelos de Dados

#### 1. Modelo Conceitual (**Alto Nível**)

* Representa os dados do **mundo real** de forma independente da tecnologia e da implementação.
* Foca na **compreensão do problema**, na **estrutura lógica dos dados** e nos requisitos dos usuários.
* Utilizado por projetistas e analistas para discutir com usuários finais, garantindo que o sistema atenda às necessidades reais.
* Exemplo: **Modelo ER (Entidade-Relacionamento)**.

#### 2. Modelo Lógico (**Nível Intermediário**)

* Traduz o modelo conceitual para um modelo compatível com o SGBD (Sistema Gerenciador de Banco de Dados) escolhido.
* Ainda é **independente do hardware**, mas já **depende do tipo de banco de dados**, como relacional ou orientado a objetos.
* Serve como base para a implementação com comandos como SQL.
* Representado por estruturas como tabelas, colunas, tipos de dados, chaves primárias e estrangeiras.

#### 3. Modelo Físico (**Baixo Nível**)

* Descreve **como os dados serão armazenados fisicamente** no disco e acessados pelo SGBD.
* Leva em consideração aspectos como blocos de disco, buffers, índices e desempenho.
* Voltado para desenvolvedores de SGBDs e administradores de banco de dados (DBA’s).

<br>

## 🧠 Conceitos Fundamentais da Abordagem Relacional

### 🧩 Esquema, Instância e Estado

* **Esquema**: Descrição estática e estrutural do banco de dados, contendo os metadados. Define os elementos que compõem o banco, como tabelas e relacionamentos. Geralmente não muda com frequência.
* **Instância**: Conjunto de dados que estão armazenados no banco em um dado momento. Pode variar constantemente.
* **Estado**: É a forma como está preenchido o Banco de Dados, inicializando como estado vazio e através do sendo alterado a cada nova instância adicionada.

<br>

### 💬 Linguagens em um SGBD Relacional

> Linguagens utilizadas para **definir**, **manipular** e **consultar** os dados em um Banco de Dados Relacional. Cada uma delas tem uma finalidade específica no processo de desenvolvimento e manutenção.

#### 📘 DDL — Data Definition Language (Linguagem de Definição de Dados)

* Utilizada para criar e modificar estruturas do banco de dados, como tabelas, índices, esquemas e restrições.
* Inclui comandos como `CREATE`, `ALTER` e `DROP`.
* Também contempla o SDL (Storage Definition Language), voltado para a definição do armazenamento físico dos dados.

#### ✍️ DML — Data Manipulation Language (Linguagem de Manipulação de Dados)

* Permite inserir, atualizar, excluir e consultar os dados contidos no banco.
* Dois tipos principais:

  * **Alto Nível (Não Procedural)**: Permite manipular conjuntos de registros com uma única instrução (ex: SQL).
  * **Baixo Nível (Procedural)**: Permite manipular registros individualmente, com controle detalhado por meio de scripts ou linguagens de programação.
  * ⚠️ Podem ser implementados em uma linguagem de programação ou diretamente pelo terminal ou ferramentas gráficas SQL. 


#### 🔍 DQL — Data Query Language (Linguagem de Consulta de Dados)

* Utilizada exclusivamente para **realizar consultas** no banco de dados, sem alterar as informações armazenadas.
* Comando principal: `SELECT`.

#### 🔄 SQL — Structured Query Language

* Linguagem padrão usada para definir, manipular e consultar dados.
* **Combina comandos DDL, DML e DQL**, tornando-se a linguagem mais utilizada em SGBDs relacionais.

<br>

## 🧱 Modelagem ER — Entidade-Relacionamento

> Técnica padrão de modelagem **conceitual**, usada para representar de forma clara e abstrata os dados relevantes de um sistema. Utiliza os elementos principais do modelo ER: **entidades**, **relacionamentos** e **atributos**, facilitando a comunicação com os usuários e a transição para o modelo relacional.

### 🔹 Elementos da Modelagem ER

* **Entidade**: Representa objetos ou conceitos (reais ou abstratos) com existência independente no contexto do sistema.

  * Exemplo: Pessoa, Produto, Curso.

* **Relacionamento**: Representa uma associação lógica entre duas ou mais entidades.

  * Exemplo: "MATRICULA" entre "Aluno" e "Disciplina".

* **Atributo**: Propriedade ou característica associada a uma entidade ou relacionamento.

  * **Atributo Simples**: Apresenta apenas um valor. Ex: nome, idade.
  * **Atributo Composto**: Pode ser subdividido em partes menores. Ex: endereço → rua, número, bairro.
  * **Atributo Identificador**: Permite identificar unicamente uma ocorrência da entidade. Ex: CPF.
  * **Atributos Identificadores Compostos**: quando há a necessidade de mais de um atributo para identificar uma ocorrência de entidade. Ex: cep + Nº casa
  * **Atributo Multivalorado**: Pode conter múltiplos valores. Ex: telefones, e-mails.

<br>

### 🔗 Tipos de Relacionamento

* **Auto-relacionamento (Unário)**

  * Uma entidade se relaciona consigo mesma.
  * É definido o papel de cada ocorrência no relacionamento.
  * Exemplo: Funcionário supervisiona Funcionário.

* **Relacionamento Binário**

  * Envolve exatamente duas entidades.
  * Exemplo: Aluno estuda Disciplina.

* **Relacionamento Ternário**

  * Envolve três entidades simultaneamente.
  * Exemplo: Médico prescreve Remédio para Paciente.

<br>

### 📏 Propriedades dos Relacionamentos

* **Cardinalidade**: Define quantas ocorrências de uma entidade estão associadas a ocorrências de outra.

  * **1:1** — Um para um — no **mínimo** 1 associação e no **máximo** 1 associação. (ex: pessoa e RG).
  * **1\:N** — Um para muitos — no **mínimo** 1 associação e no **máximo** n associações. (ex: professor ministra várias disciplinas).
  * **N\:N** — Muitos para muitos — no **mínimo** n associações e no **máximo** n associações. (ex: alunos e disciplinas).

* **Atributos do Relacionamento**: Informações adicionais sobre a associação.

  * Exemplo: Data da matrícula entre Aluno e Disciplina.

* **Relacionamento Identificador**:
 
  * Ocorre entre uma **Entidade Forte** e uma **Entidade Fraca**.
  * É obrigatório quando existir uma **Entidade Fraca**, pois possibilita identificar os registros dessa entidade.  
  * A **Entidade Fraca** depende da forte para existir, pois não possui identificador próprio.
  * Exemplo: Dependente (fraca) depende de Funcionário (forte).

* **Entidade Associativa**:

  * Um relacionamento transformado em entidade, geralmente por possuir atributos próprios.
  * ❗ **Problema** - Inviável de implementar no Modelo Relacional.
  * 💡 **Solução** - Modelo ER equivalente sem **Entidades Associativas**.
  * ✅ **Resolução** - Construir relacionamentos intermediários entre as entidades e a entidade associativa, sendo convertida para uma entidade simples. Método usado em relacionamentos ternários.

<br>

### 🌳 Herança em ER (Generalização/Especialização)

> Associa **entidades específicas** a uma **entidade genérica** por meio de propriedades pertinentes a ambas ocorrências (**especializadas**). Essas ocorrências possuem propriedades particulares que diferenciam as especificidades de cada uma.

#### Tipos de Herança:

* **Total**: Todas as instâncias da entidade genérica pertencem obrigatoriamente a uma entidade especializada.
* **Parcial**: Algumas instâncias da entidade genérica não pertencem a nenhuma entidade especializada.
* **Disjunta**: Cada instância da genérica pertence a no máximo uma especializada.
* **Sobreposta**: Uma instância pode pertencer a mais de uma entidade especializada ao mesmo tempo.

<br>

### 📝 Observações Finais

* A modelagem ER é essencial para um projeto de banco de dados sólido, organizado e de fácil manutenção.
* Os diagramas ER auxiliam a visualizar e validar a estrutura dos dados junto aos usuários finais.
* Ao converter o modelo ER para o modelo relacional, é fundamental respeitar as estruturas definidas e adaptar corretamente atributos e relacionamentos.
