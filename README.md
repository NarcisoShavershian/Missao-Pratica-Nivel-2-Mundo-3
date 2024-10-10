# Missao-Pratica-Nivel-2-Mundo-3
Projeto de Banco de Dados: Loja
Este projeto é um sistema de gerenciamento de uma loja que armazena dados de usuários , pessoas físicas , pessoas jurídicas , produtos e movimentações de entrada e saída .

O sistema foi projetado para registrar e controlar operações de compras e vendas, além de garantir a integridade dos dados por meio de chaves estrangeiras e validações.

O relatório de práticas foi elaborado em formato PDF e produzido em conjunto com o desenvolvimento do projeto.

Estrutura do Banco de Dados
Tabelas Principais:
usuário : Armazena os dados de login dos usuários que operam o sistema.
pessoa : Armazena dados comuns de pessoas físicas e jurídicas.
pessoa_física : Relacionada à tabela pessoa, com o CPF.
pessoa_jurídica : Relacionada à tabela pessoa, com o CNPJ.
produto : Armazena informações dos produtos da loja, como nome, quantidade em estoque e preço de venda.
movimento : Registra as movimentações de produtos (compras e vendas), relacionando usuário, pessoa e produto.
Chaves Primárias e Estrangeiras
Cada tabela possui uma chave primária que garante a unicidade de seus registros.
As tabelas de transferência utilizam chaves estrangeiras para relacionar usuários, pessoas e produtos, garantindo a consistência dos dados e a integridade referencial.
Consultas Importantes
Movimentações de entrada e saída : As consultas permitem visualizar os dados de compras e vendas, incluindo fornecedores, compradores, detalhes e valores.
Relatórios : É possível agrupar e somar os valores de movimentações por produto e operador, além de calcular médias ponderadas de vendas por produto.
Como Executar
Crie o banco de dados executando o comando:

CREATE DATABASE Loja;
Crie as tabelas executando os scripts SQL fornecidos no projeto.

Insira os dados iniciais de usuários, pessoas e produtos.

Utilize as consultas fornecidas para gerar relatórios e visualizar movimentações de entrada e saída.

Requisitos
SQL Server : O projeto foi desenvolvido utilizando o SQL Server.
Usuário e senha de acesso : Defina o login e senha para operar o banco de dados com:
CREATE LOGIN loja WITH PASSWORD = 'Loja2468';
Validações
O campo tipoda tabela movimentopossui uma restrição CHECK que garante que os tipos de movimentação só podem ser 'E' (Entrada) ou 'S' (Saída).
Os campos cpfe cnpjnas tabelas pessoa_fisicasão pessoa_juridicaúnicos para evitar duplicação de registros.
