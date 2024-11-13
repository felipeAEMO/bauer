# Bauer Collections - Website

Este repositório contém o código-fonte do site **Bauer Collections**, desenvolvido com HTML, CSS e JavaScript. O site inclui uma seção de contato com validação e armazenamento de mensagens, utilizando PHP e MySQL para gerenciar as interações com o banco de dados.

## Índice

- [Sobre o Projeto](#sobre-o-projeto)
- [Funcionalidades](#funcionalidades)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Pré-requisitos](#pré-requisitos)
- [Instalação e Configuração](#instalação-e-configuração)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Uso](#uso)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Sobre o Projeto

O site **Bauer Collections** é um projeto focado em oferecer uma experiência moderna e responsiva aos usuários, destacando a coleção de produtos e permitindo o contato direto através de um formulário que valida as informações fornecidas. Esta solução é ideal para quem busca um site básico com integração de back-end para coleta de contatos.

## Funcionalidades

- **Home:** Apresentação da coleção de produtos.
- **Sobre:** Informações sobre a Bauer Collections.
- **Produtos:** Lista e descrição dos produtos.
- **Contato:** Formulário de contato com validação em PHP e armazenamento das mensagens em um banco de dados MySQL.

## Tecnologias Utilizadas

- **Front-end:** HTML, CSS, JavaScript
- **Back-end:** PHP
- **Banco de Dados:** MySQL

## Pré-requisitos

Antes de iniciar, você precisará ter instalado em seu ambiente:

- [PHP](https://www.php.net/downloads) (versão 7.4 ou superior)
- [MySQL](https://dev.mysql.com/downloads/)
- [Apache](https://httpd.apache.org/download.cgi) (recomendado com XAMPP ou WAMP para facilitar o setup do ambiente)
- [Git](https://git-scm.com/downloads)

## Instalação e Configuração

1. **Clone este repositório:**

    ```bash
    git clone https://github.com/seu-usuario/bauer-collections.git
    cd bauer-collections
    ```

2. **Configure o Banco de Dados MySQL:**

   - Crie um banco de dados chamado `contatoDB` (ou outro nome à sua escolha).
   - No banco de dados, crie a tabela `contatos` com o seguinte comando SQL:

    ```sql
    CREATE TABLE contatos (
        id INT AUTO_INCREMENT PRIMARY KEY,
        nome VARCHAR(100),
        email VARCHAR(100),
        empresa VARCHAR(100),
        mensagem TEXT,
        data_envio TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    );
    ```

3. **Configuração do Arquivo PHP:**

   No arquivo `config.php`, configure os dados de acesso ao banco de dados:

    ```php
    <?php
    $servername = "localhost";
    $username = "seu_usuario";
    $password = "sua_senha";
    $dbname = "contatoDB";
    ?>
    ```

4. **Inicie o servidor:**

   Inicie o servidor Apache/MySQL (usando XAMPP, WAMP, ou via linha de comando) e verifique se o site está rodando em `http://localhost/bauer-collections`.


## Uso

1. Abra o site no navegador com `http://localhost/bauer-collections`.
2. Navegue pelas páginas do site para explorar as seções "Home", "Sobre" e "Produtos".
3. Acesse a seção de **Contato** e preencha o formulário com suas informações. O PHP validará e armazenará os dados no banco de dados MySQL.

## Contribuição

Contribuições são bem-vindas! Para contribuir:

1. Faça um fork do projeto.
2. Crie uma branch para sua feature: `git checkout -b minha-feature`.
3. Commit suas alterações: `git commit -m 'Adiciona nova feature'`.
4. Envie para a branch principal: `git push origin minha-feature`.
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo `LICENSE` para mais informações.

---

Esse modelo deve estar pronto para uso direto no arquivo `README.md`.


