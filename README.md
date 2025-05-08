<h1 align="center">🗄️ Banco de Dados</h1>

## 📌 Introdução

> **Banco de Dados** são conjuntos de dados relacionados, organizados e gerenciados por um sistema chamado **SGBD** (Sistema Gerenciador de Banco de Dados).

<br>

## 🔍 Características Principais

- 📌 Os dados refletem um **cenário de domínio** (contexto específico).
- 📌 A **ordem e organização dos dados são essenciais**; dados aleatórios não formam um verdadeiro Banco de Dados.
- 📌 A construção e implementação de um Banco de Dados está **atrelada ao domínio para o qual ele foi projetado**.

<br>

## 🛠️ Usabilidade dos Bancos de Dados

### 📦 Armazenamento Persistente

Utilizado em diversos tipos de sistemas:

- 🎓 Sistema Acadêmico  
- 🏦 Sistema Bancário  
- 🛒 Sistema de E-Commerce  
- 🏥 Sistema Hospitalar  
- 🧾 Sistemas de Gestão Empresarial (ERP)  
- 🚚 Sistemas Logísticos  

### 🔐 Gerenciamento de Acesso e Manipulação

- **Definição de Regras:** Regras comuns a diferentes sistemas (como unicidade de CPF, emails válidos, etc).
- **Modos de Acesso:**
  - 🔧 **Manual:** O usuário administra diretamente o banco.
  - 📲 **Por Aplicação:** Cada app interage de forma primitiva com os dados.
  - 🧠 **Via SGBD:** Gerenciado por um sistema especializado.

### 📊 Dados vs. Informações

| Conceito    | Definição                                                                 |
|-------------|---------------------------------------------------------------------------|
| **Dado**    | Fato isolado, sem contexto (ex: nome, CPF, idade).                        |
| **Informação** | Dados organizados com significado (ex: boletim escolar, nota fiscal).  |

<br>

## 🧠 Sistema Gerenciador de Banco de Dados (SGBD)

### 💡 Conceito

> Um SGBD é um conjunto de softwares que facilita a **definição, armazenamento, manipulação, compartilhamento, proteção e segurança** de um Banco de Dados.

<br>

### ⚙️ Funcionalidades Principais

- 📐 **Definição:** Estrutura, tipos e restrições dos dados.
- 📥 **Povoamento:** Inserção de dados nas estruturas.
- 🔄 **Manipulação:** Consultas, atualizações, exclusões e relatórios.
- 👥 **Compartilhamento:** Acesso simultâneo seguro e controlado.
- 🛡️ **Proteção:** Contra falhas, corrupção ou acessos indevidos.
- 🔒 **Segurança:** Contra ataques e acessos não autorizados.

<br>

### 🧬 Funcionamento do SGBD

```text
╭────────────────────╮
│     APLICAÇÃO      │  ← Interface do usuário ou sistema
╰────────┬───────────╯
         ↓
╭───────────────────────────────────╮
│  PROCESSAMENTO DE CONSULTAS SQL   │  ← Interpreta o comando da aplicação    
╰────────┬──────────────────────┬───╯
         ↓                      ↓
    ╭──────────────╮   ╭──────────────────────╮
    │  ACESSO AOS  │   │ DICIONÁRIO DE DADOS  │ ← Metadados (estruturas do banco)
    │    DADOS     │   │     (Metadados)      │
    ╰────────┬─────╯   ╰────────────┬─────────╯
             ↓                      ↓
    ╭─────────────────────────────────────╮
    │      BANCO DE DADOS (CONTEÚDO)      │ ← Dados reais (tabelas, índices)
    ╰──────────────────┬──────────────────╯
                       ↓
              ╭────────┴──────╮
              │  ACESSO AOS   │  ← Recupera os dados solicitados
              │     DADOS     │
              ╰────────┬──────╯
                       ↓
       ╭───────────────┴────────────────╮
       │   PROCESSAMENTO DE CONSULTAS   │  ← Organiza os dados p/ resposta
       ╰───────────────┬────────────────╯
                       ↓
               ╭───────┴───────╮
               │   APLICAÇÃO   │  ← Exibe os dados ao usuário
               ╰───────────────╯
```

<br>

### 🧩 Características de um SGBD

- 🧾 **Natureza Autodescritiva:** Descrição de suas estruturas armazenados dentro do próprio BD (Metadados).
- 🧭 **Isolamento de Programas e Dados:** As aplicações não precisam conhecer como os dados são organizados, apenas acessa-los por comando.
- 🎭 **Abstração de Dados:** Usuários interagem com níveis diferentes de como os dados são vistos e manipulados (externo, lógico, interno).
- 🔍 **Múltiplas Visões dos Dados:** Visualização adaptada ao tipo de usuário.
- 👥 **Compartilhamento Seguro:** Acesso simultâneo com controle de concorrência.
- 🔁 **Transações Multiusuário:** Suporte a transações seguras e consistentes.
- 🧼 **Controle de Redundância:** Evita duplicações desnecessárias.
- 🔐 **Restrição de Acesso:** Controle de permissões por usuário.
- 🚀 **Eficiência em Consultas:** Uso de índices e outras estruturas de desempenho.
- 💾 **Backup e Restauração:** Segurança em caso de falhas.
- 💻 **Interfaces Diversificadas:** Acesso via SQL, APIs, interfaces gráficas etc.
- 📏 **Restrições de Integridade:** Regras para manter consistência e validade dos dados.

<br>

### 💽 Principais SGBDs e Descrições

| Nome              | Descrição                                                                 |
|-------------------|---------------------------------------------------------------------------|
| **Oracle**        | Robusto, usado em grandes empresas, com forte suporte a transações.       |
| **SQL Server**    | Da Microsoft, integração com Windows e ferramentas BI.                    |
| **IBM DB2**       | Voltado a ambientes corporativos de alta performance.                     |
| **SAP HANA**      | Processamento em memória, ideal para big data e análise em tempo real.    |
| **Snowflake**     | Baseado na nuvem, altamente escalável e utilizado para data warehousing.  |
| **Teradata**      | Projetado para análises massivas e armazenamento distribuído.             |
| **MySQL**         | Open source, amplamente utilizado em web e apps com PHP.                  |
| **PostgreSQL**    | Avançado e gratuito, ideal para aplicações complexas e personalizáveis.   |

<br>

### 👨‍💼 Atores de um Sistema de Banco de Dados

#### 🛠️ Administrador de Banco de Dados (DBA)

- Define permissões e autorizações.
- Monitora e coordena o uso do BD.
- Responsável por hardware, software e manutenção.

#### 🧱 Projetista do Banco

- Define a estrutura ideal para os dados.
- Realiza levantamento de requisitos com stakeholders.

#### 👤 Usuários Finais

- **Casuais:** Acessos esporádicos (consultas ou relatórios).
- **Parametrizáveis:** Usam interfaces gráficas para manipular os dados.
- **Sofisticados:** Usam SQL diretamente, conhecem a fundo os recursos do sistema.

#### 👨‍💻 Desenvolvedores

- **Projetista e Implementador do SGBD:** Desenvolvem o próprio SGBD.
- **Ferramentas de Apoio:** Criam ferramentas auxiliares para o gerenciamento do sistema.
- **Operação e Manutenção:** Responsáveis pelo funcionamento contínuo do banco.

<br>

### 🧮 Considerações sobre o Uso de SGBDs

- 💰 **Custo:** Investimento em hardware, software e capacitação.
- 📋 **Adequação:** Ideal para aplicações com grande volume de dados ou multiusuário.
- ⏱️ **Tempo Real:** Alguns SGBDs não são ideais para sistemas com requisitos críticos de tempo.
- 👥 **Multiusuário:** Possibilidade de acesso simultâneo com consistência.
