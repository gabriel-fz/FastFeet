<img alt="GoStack" src="https://raw.githubusercontent.com/gabriel-fz/FastFeet/master/assets/header-desafio.png" />

<h2 align="center">
  Minha resolução do desafio FastFeet do Bootcamp GoStack
</h2>

<p align="center">
  <a href="#sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#tecnologias-utilizadas">Tecnologias utilizadas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#instalação-e-execução">Instalação e execução</a>
</p>

## Sobre o desafio

Nos links abaixo estão os repositórios das 4 etapas que compõem o desafio:

- [Etapa 1](https://github.com/Rocketseat/bootcamp-gostack-desafio-02/blob/master/README.md#desafio-02-iniciando-aplica%C3%A7%C3%A3o)
- [Etapa 2](https://github.com/Rocketseat/bootcamp-gostack-desafio-03/blob/master/README.md#desafio-03-continuando-aplica%C3%A7%C3%A3o)
- [Etapa 3](https://github.com/Rocketseat/bootcamp-gostack-desafio-09#desafio-09-front-end-do-meetapp)
- [Etapa 4](https://github.com/Rocketseat/bootcamp-gostack-desafio-10#desafio-10-mobile-do-meetapp)

## Tecnologias utilizadas

Para a resolução do desafio final, foram utilizadas as seguintes tecnologias:

- [Node](https://nodejs.org/en/)
- [Docker](https://www.docker.com/)
- [PostgreSQL](https://www.postgresql.org/)
- [Express](https://github.com/expressjs/express)
- [Redis](https://redis.io/)
- [Bee-Queue](https://github.com/bee-queue/bee-queue)
- [Nodemailer](https://nodemailer.com/about/)
- [Jest](https://jestjs.io/)
- [React](https://reactjs.org/)
- [React-Native](https://reactnative.dev/)
- [Redux](https://redux.js.org/)
- [Styled-Components](https://styled-components.com/)
- [Date-Fns](https://date-fns.org/)
- [Unform](https://unform.dev/)
- [Reactotron](https://github.com/infinitered/reactotron)
- [Insomnia](https://insomnia.rest/)
- [React Select](https://react-select.com/home)
- [Bcryptjs](https://github.com/dcodeIO/bcrypt.js)

## Instalação e execução

A seguir, estão descritos todos os passos para a instalação e execução

### Pré-requisitos

- [Node](https://nodejs.org/en/)
- [Yarn](https://classic.yarnpkg.com/pt-BR/docs/install#debian-stable)
- [Git](https://git-scm.com/downloads)
- [Insomnia](https://insomnia.rest/)(Opcional)
- [Reactotron](https://github.com/infinitered/reactotron)

### Clonando o repositório

Abra em sua máquina uma pasta de sua preferência. Em seguida, abra o terminar de sua máquina na respectiva pasta e rode o seguinte comando:

```
$ git clone https://github.com/gabriel-fz/FastFeet.git
```

Ou então, baixe este repositório zipado.

### Instalação e execução da API

Inicialmente, vá até a pasta da api e execute o comando `yarn` para instalar as dependências do projeto.

Para que a api funcione, é necessário ter em sua máquina o PostgreSQL. Para ser mais fiel ao modo como foi desenvolvido, recomenda-se que instale o PostgreSQL via Docker com o seguinte comando:

```
$ docker run
```

Em seguida, é necessário também instalar o Redis. Recomenda-se que instale o Redis via Docker com o seguinte comando:

```
$ docker run
```

Com o PostgreSQL rodando, crie um banco de dados com o nome `fastfeet`.

Para testar o envio de emails, crie uma conta no [Mailtrap](http://mailtrap.io/) e guarde os dados para preencher a configuração da api.

Para receber notificações de erros, crie uma conta no [Sentry](http://sentry.io/). Crie um projeto novo e guarde os dados para preencher a configuração da api.

Para configurar a api, siga os seguintes passos:

1. Abra a pasta da api
2. Copie todo o conteúdo do arquivo `.env.example`
3. Crie um arquivo na raiz da pasta api com o nome `.env`
4. Cole todo o conteúdo copiado do arquivo `.env.example` no arquivo `.env`
5. Preencha todo o conteúdo do arquivo `.env` com os dados do banco de dados, do redis, do mailtrap e do sentry.

Com toda configuração feita, execute o seguinte comando para criar as tabelas no banco de dados:

```
yarn sequelize db:migrate:all
```

Com as tabelas criadas no banco de dados, execute o seguinte comando para inserir os dados do admin no banco:

```
yarn sequelize db:seed:all
```

Caso queira testar as rotas, vá até a pasta da api e importe o arquivo `Insomnia.json` no insomnia.

Terminadas todas as configurações, basta executar o seguinte comando na pasta da api para iniciar o servidor:

```
yarn dev
```
