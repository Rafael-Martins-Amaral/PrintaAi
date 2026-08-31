# 👕 Product Requirements Document (PRD) — PrintaAI
## 1. Visão Geral e Objetivo

O *PrintaAI* é uma aplicação web para gerenciamento de pedidos de camisetas personalizadas. O sistema permite que clientes escolham características da camiseta, como modelo, cor, tamanho e estampa, e registrem seus pedidos de forma simples e organizada.

### 🎯 1.1 Objetivo do Produto

O objetivo do PrintaAI é facilitar o processo de criação e registro de pedidos de camisetas personalizadas, permitindo que o cliente escolha as características desejadas e consulte os pedidos realizados.

O sistema busca centralizar essas informações em uma interface simples, responsiva e intuitiva.

### 👤 1.2 Identificação
Aluno: [SEU NOME COMPLETO]
Projeto: PrintaAI
Tema: Sistema de pedidos de camisetas personalizadas
# 2. Atores do Sistema
Visitante: Usuário que acessa a aplicação para conhecer os modelos de camisetas disponíveis e realizar um pedido.
Cliente: Usuário que preenche os dados necessários e registra um pedido de camiseta personalizada.
Sistema: Responsável por armazenar, recuperar e apresentar os dados dos pedidos e das camisetas disponíveis.
# 3. Funcionalidades Principais

O PrintaAI terá como principais funcionalidades:

Visualização dos modelos de camisetas disponíveis;
Cadastro de pedidos de camisetas personalizadas;
Escolha de características da camiseta;
Informações de contato do cliente;
Visualização dos pedidos realizados;
Exclusão de pedidos cadastrados;
Consulta de endereço através do CEP informado pelo cliente.
# 📝 4. Histórias de Usuário e Escopo
## 👕 Épico 1: Catálogo de Camisetas
### US01 — Visualizar Camisetas

Como um Visitante, quero visualizar os modelos de camisetas disponíveis para conhecer as opções oferecidas pela PrintaAI.

Critérios de Aceitação:

Os modelos devem ser apresentados em cards;
Cada camiseta deve apresentar informações básicas, como nome, imagem e preço;
A listagem deve funcionar em dispositivos mobile e desktop.
### US02 — Selecionar Modelo

Como um Cliente, quero selecionar um modelo de camiseta para utilizá-lo no meu pedido.

Critérios de Aceitação:

O modelo escolhido deve ser identificado no formulário de pedido;
O cliente deve poder escolher entre os modelos disponíveis.
## 🛒 Épico 2: Cadastro de Pedidos
### US03 — Criar Pedido

Como um Cliente, quero preencher um formulário com meus dados e as características da camiseta para registrar um novo pedido.

Critérios de Aceitação:

Nome do cliente deve ser obrigatório;
E-mail deve ser obrigatório e possuir formato válido;
Modelo da camiseta deve ser selecionado;
Tamanho deve ser selecionado;
Cor deve ser selecionada;
Estampa deve ser selecionada;
Quantidade deve ser informada;
O sistema deve impedir o envio do formulário quando houver dados inválidos.
### US04 — Personalizar Camiseta

Como um Cliente, quero escolher características da camiseta, como cor, tamanho e estampa, para criar um pedido de acordo com minhas preferências.

Critérios de Aceitação:

O tamanho deve ser selecionado entre opções disponíveis;
A cor deve ser selecionada;
O cliente deve escolher uma estampa disponível;
A quantidade deve ser um valor positivo.
### US05 — Informar Endereço

Como um Cliente, quero informar meu CEP para preencher os dados básicos do endereço do pedido de forma mais rápida.

Critérios de Aceitação:

O CEP deve possuir formato válido;
O sistema deve consultar uma API de CEP;
Os dados retornados devem ser apresentados ao cliente;
O sistema deve informar o usuário caso o CEP não seja encontrado ou ocorra um erro na consulta.
### US06 — Confirmar Pedido

Como um Cliente, quero revisar as informações da minha camiseta antes de confirmar o pedido para evitar erros no cadastro.

Critérios de Aceitação:

O sistema deve apresentar um resumo das informações preenchidas;
O pedido somente deve ser registrado após a confirmação;
Após o cadastro, o usuário deve receber uma mensagem indicando que o pedido foi realizado.
## 📋 Épico 3: Visualização e Gerenciamento de Pedidos
### US07 — Visualizar Pedidos

Como um Cliente, quero visualizar os pedidos cadastrados para consultar as camisetas que solicitei.

Critérios de Aceitação:

Os pedidos devem ser apresentados em formato de cards ou tabela;
Cada pedido deve apresentar informações como cliente, modelo, tamanho, cor, quantidade e status;
Os dados devem ser carregados dinamicamente.
### US08 — Excluir Pedido

Como um Cliente, quero excluir um pedido cadastrado para remover pedidos que não desejo mais manter na lista.

Critérios de Aceitação:

O sistema deve solicitar confirmação antes da exclusão;
O pedido excluído não deve permanecer na listagem;
A listagem deve ser atualizada após a exclusão.
## 💾 Épico 4: Persistência dos Dados
### US09 — Armazenar Dados do Pedido

Como um Cliente, quero que os dados do meu pedido sejam armazenados para que possam ser consultados posteriormente.

Critérios de Aceitação:

Os pedidos devem ser enviados para a API utilizada pela aplicação;
Os dados devem ser armazenados em formato JSON;
A aplicação deve conseguir recuperar os pedidos armazenados.
###US10 — Manter Preferências Localmente

Como um Cliente, quero que algumas informações da minha utilização sejam armazenadas localmente para facilitar o uso da aplicação.

Critérios de Aceitação:

O sistema deve utilizar Web Storage;
Os dados armazenados devem poder ser recuperados em uma nova visita à aplicação;
O armazenamento local não deve impedir o funcionamento da aplicação caso esteja vazio.
