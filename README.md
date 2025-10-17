🎮 Atividade SQL – Banco de Dados da PixelPlay 🕹️
✨ Descrição

Esta atividade faz parte dos meus primeiros estudos em SQL. O objetivo é praticar a criação, manipulação e consulta de um banco de dados, simulando uma loja de jogos fictícia chamada PixelPlay.

Na PixelPlay, todo cliente pode registrar suas informações (nome, e-mail, telefone) e comprar jogos de diferentes plataformas. Cada venda precisa ser associada a um cliente e ao jogo adquirido, contendo data e valor da compra.

📋 Roteiro da Atividade
1️⃣ Criação das Tabelas

A equipe cria as estruturas do banco:

🎮 Game → Armazena títulos, plataformas e informações dos jogos

👤 Cliente → Guarda informações dos clientes

💰 Venda → Registra as compras, ligando cada cliente ao jogo adquirido

Exemplo de comando:

CREATE TABLE Cliente (
    id INT PRIMARY KEY,
    nome VARCHAR(100),
    email VARCHAR(100),
    telefone VARCHAR(15)
);

2️⃣ Inserção de Dados

Após criar as tabelas, adicionamos:

5 jogos distintos (vários gêneros e plataformas) 🎮

10 clientes fictícios 👥

5 vendas reais 💸

Exemplo de inserção:

INSERT INTO Cliente (id, nome, email, telefone)
VALUES (1, 'Ana Beatriz Santos', 'ana.santos@email.com', '(11) 98765-4321');

3️⃣ Consultas

O gerente da loja responde perguntas do dia a dia:

Quais games estão disponíveis? 🕹️

Quais clientes usam Gmail? 📧

Quais vendas ocorreram em outubro? 📅

Quais RPGs estão em estoque, e como se comparam por nome? 🎲

Exemplo:

SELECT * FROM Game WHERE genero = 'RPG' ORDER BY nome;

4️⃣ Atualização de Dados

O suporte corrige informações, como:

Telefone de cliente mal cadastrado 📞

Ano de lançamento de um game com erro 🗓️

Exemplo:

UPDATE Cliente
SET telefone = '(11) 99999-9999'
WHERE id = 3;

5️⃣ Exclusão de Dados

Para manter o banco limpo 🧹:

Remover um game retirado do catálogo ❌

Apagar vendas antigas (mais de 30 dias) 🗑️

Exemplo:

DELETE FROM Venda
WHERE data < '2025-09-01';

🌟 Moral da história

Com o banco de dados, a PixelPlay garante organização, controle de vendas e clientes, além de gerar relatórios detalhados a cada mês. Este exercício mostra como SQL e bancos de dados são essenciais para empresas de tecnologia, especialmente no mercado de games.

🚀 Objetivos da atividade

Iniciar os conhecimentos em SQL 💻

Praticar criação, inserção, consulta, atualização e exclusão de dados

Entender como bancos de dados ajudam a organizar informações e apoiar decisões
