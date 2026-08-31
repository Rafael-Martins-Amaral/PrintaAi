# 👕 Product Requirements Document (PRD) — PrintaAI
## 1. Visão Geral e Objetivo

O **PrintaAI** é uma aplicação web para gerenciamento de pedidos de camisetas personalizadas. O sistema permite que clientes escolham características da camiseta, como modelo, cor, tamanho e estampa, e registrem seus pedidos de forma simples e organizada.

### 🎯 1.1 Objetivo do Produto

O objetivo do PrintaAI é facilitar o processo de criação e registro de pedidos de camisetas personalizadas, permitindo que o cliente escolha as características desejadas e consulte os pedidos realizados.

O sistema busca centralizar essas informações em uma interface simples, responsiva e intuitiva.

### 👤 1.2 Identificação
- **Aluno**: Rafael Martins Amaral
- **Projeto**: PrintaAI
- **Tema**: Sistema de pedidos de camisetas personalizadas

---

## 2. Atores do Sistema
- **Visitante**: Usuário que acessa a aplicação para conhecer os modelos de camisetas disponíveis e realizar um pedido.
- **Cliente**: Usuário que preenche os dados necessários e registra um pedido de camiseta personalizada.
- **Sistema**: Responsável por armazenar, recuperar e apresentar os dados dos pedidos e das camisetas disponíveis.

---

## 3. Funcionalidades Principais

 O PrintaAI terá como principais funcionalidades:

- Visualização dos modelos de camisetas disponíveis;
- Cadastro de pedidos de camisetas personalizadas;
- Escolha de características da camiseta;
- Informações de contato do cliente;
- Visualização dos pedidos realizados;
- Exclusão de pedidos cadastrados;
- Consulta de endereço através do CEP informado pelo cliente.

---

## 📝 4. Histórias de Usuário e Escopo

## 🔐 Épico 1: Autenticação e Conta

 ### US01 — Criar Conta

 Como um Visitante, quero criar uma conta informando meu nome, e-mail e senha para acessar as funcionalidades da PrintaAI.
 Critérios de Aceitação:

- Nome, e-mail e senha são obrigatórios;
- O e-mail deve possuir formato válido;
- A senha deve possuir um tamanho mínimo;
- Os dados da conta devem ser armazenados;
- Após o cadastro, o usuário deve poder acessar o sistema.

### US02 — Fazer Login

 Como um Cliente, quero informar meu e-mail e senha para acessar o catálogo e realizar pedidos.
 Critérios de Aceitação:

- E-mail e senha devem ser obrigatórios;
- O sistema deve verificar se os dados correspondem a uma conta cadastrada;
- Em caso de erro, deve ser apresentada uma mensagem;
- Após o login, o cliente deve ser direcionado ao catálogo.

## 👕 Épico 2: Catálogo de Camisetas

 ### US03 — Visualizar Camisetas

 Como um Visitante, quero visualizar os modelos de camisetas disponíveis para conhecer as opções oferecidas pela PrintaAI.
 Critérios de Aceitação:

- Os modelos devem ser apresentados em cards;
- Cada camiseta deve apresentar informações básicas, como nome, imagem e preço;
- A listagem deve funcionar em dispositivos mobile e desktop.

## 🛒 Épico 3 Cadastro de Pedidos

 ### US04 — Criar Pedido

 Como um Cliente, quero preencher um formulário com meus dados e as características da camiseta para registrar um novo pedido.
 Critérios de Aceitação:

- Nome do cliente deve ser obrigatório;
- E-mail deve ser obrigatório e possuir formato válido;
- O cliente deve poder escolher entre os modelos disponíveis.
- O modelo escolhido deve ser identificado no formulário de pedido;
- Tamanho deve ser selecionado;
- Cor deve ser selecionada;
- Estampa deve ser selecionada;
- Quantidade deve ser informada;
- O sistema deve impedir o envio do formulário quando houver dados inválidos.

 ### US05 — Personalizar Camiseta

 Como um Cliente, quero escolher características da camiseta, como cor, tamanho e estampa, para criar um pedido de acordo com minhas preferências.
 Critérios de Aceitação:

- O tamanho deve ser selecionado entre opções disponíveis;
- A cor deve ser selecionada;
- O cliente deve escolher uma estampa disponível;
- A quantidade deve ser um valor positivo.

 ### US06 — Informar Endereço

 Como um Cliente, quero informar meu CEP para preencher os dados básicos do endereço do pedido de forma mais rápida.
 Critérios de Aceitação:

- O CEP deve possuir formato válido;
- O sistema deve consultar uma API de CEP;
- Os dados retornados devem ser apresentados ao cliente;
- O sistema deve informar o usuário caso o CEP não seja encontrado ou ocorra um erro na consulta.

 ### US07 — Confirmar Pedido

 Como um Cliente, quero revisar as informações da minha camiseta antes de confirmar o pedido para evitar erros no cadastro.
 Critérios de Aceitação:

- O sistema deve apresentar um resumo das informações preenchidas;
- O pedido somente deve ser registrado após a confirmação;
- Após o cadastro, o usuário deve receber uma mensagem indicando que o pedido foi realizado.

## 📋 Épico 4: Visualização e Gerenciamento de Pedidos

 ### US08 — Visualizar Pedidos

 Como um Cliente, quero visualizar os pedidos cadastrados para consultar as camisetas que solicitei.
 Critérios de Aceitação:

- Os pedidos devem ser apresentados em formato de cards ou tabela;
- Cada pedido deve apresentar informações como cliente, modelo, tamanho, cor, quantidade e status;
- Os dados devem ser carregados dinamicamente.

 ### US09 — Excluir Pedido

 Como um Cliente, quero excluir um pedido cadastrado para remover pedidos que não desejo mais manter na lista.
 Critérios de Aceitação:

- O sistema deve solicitar confirmação antes da exclusão;
- O pedido excluído não deve permanecer na listagem;
- A listagem deve ser atualizada após a exclusão.

## 💾 Épico 5: Persistência dos Dados

 ### US10 — Armazenar Dados do Pedido

 Como um Cliente, quero que os dados do meu pedido sejam armazenados para que possam ser consultados posteriormente.
 Critérios de Aceitação:

- Os pedidos devem ser enviados para a API utilizada pela aplicação;
- Os dados devem ser armazenados em formato JSON;
- A aplicação deve conseguir recuperar os pedidos armazenados.

 ### US11 — Manter Preferências Localmente

 Como um Cliente, quero que meu nome e e-mail sejam armazenados localmente para não precisar preenchê-los novamente ao realizar outro pedido.
 Critérios de Aceitação:

- O sistema deve utilizar Web Storage;
- Os dados armazenados devem poder ser recuperados em uma nova visita à aplicação;
- O armazenamento local não deve impedir o funcionamento da aplicação caso esteja vazio.
