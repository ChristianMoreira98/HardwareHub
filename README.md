# 🖥️ HardwareHub - Banco de Dados MySQL

Projeto de banco de dados desenvolvido em **MySQL** simulando o funcionamento de uma loja de informática chamada **HardwareHub**.

O objetivo do projeto é praticar **operações CRUD**, **modelagem de banco de dados** e **relacionamentos entre tabelas**.

---

## 📦 Estrutura do Banco

O banco de dados possui 4 tabelas principais:

### 👤 clientes
Armazena as informações dos clientes.

Campos principais:
- id_cliente (Primary Key)
- nome
- email
- telefone

---

### 💻 produtos
Armazena os produtos disponíveis na loja.

Campos principais:
- id_produto (Primary Key)
- nome
- descricao
- preco
- estoque

---

### 🧾 vendas
Registra as vendas realizadas pelos clientes.

Campos principais:
- id_venda (Primary Key)
- data_venda
- fk_cliente (Foreign Key)

Relaciona cada venda a um cliente.

---

### 📋 itens_venda
Tabela responsável por relacionar **produtos com vendas**.

Campos principais:
- id_item (Primary Key)
- fk_venda (Foreign Key)
- fk_produto (Foreign Key)
- quantidade

Essa estrutura permite que **uma venda tenha vários produtos**.

---

## 🔑 Conceitos Utilizados

### 🆔 Primary Key
Identifica **cada registro de forma única** dentro da tabela.

Exemplos no projeto:
- `id_cliente`
- `id_produto`
- `id_venda`
- `id_item`

---

### 🔗 Foreign Key
Cria **relacionamentos entre tabelas**, garantindo integridade dos dados.

Relacionamentos no projeto:

- `vendas.fk_cliente → clientes.id_cliente`
- `itens_venda.fk_venda → vendas.id_venda`
- `itens_venda.fk_produto → produtos.id_produto`

---

## 🛠 Tecnologias Utilizadas

- MySQL
- SQL
- MySQL Workbench

---

## 🎯 Objetivo do Projeto

Este projeto foi criado para praticar:

- criação de tabelas
- inserção de dados
- relacionamentos entre tabelas
- estruturação de banco de dados para sistemas reais

---

💡 Projeto desenvolvido para fins de **estudo e prática de SQL e banco de dados**.