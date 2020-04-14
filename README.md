<img alt="GoStack" src="https://raw.githubusercontent.com/gabriel-fz/FastFeet/master/assets/header-desafio.png" />

<h2 align="center">
  Minha resolução do desafio FastFeet do Bootcamp GoStack
</h2>

<p align="center">
  <a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#rocket-tecnologias-utilizadas">Tecnologias utilizadas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#rocket-instalação-e-execução">Instalação e execução</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#rocket-detalhes-extras">Detalhes Extras</a>
</p>

<p align="center">
  Feito com :purple_heart: by <a href="https://github.com/gabriel-fz" target="_blank">gabriel-fz</a>
</p>

## :rocket: Sobre o desafio

Nos links abaixo estão os repositórios das 4 etapas que compõem o desafio:

- [Etapa 1](https://github.com/Rocketseat/bootcamp-gostack-desafio-02/blob/master/README.md#desafio-02-iniciando-aplica%C3%A7%C3%A3o)
- [Etapa 2](https://github.com/Rocketseat/bootcamp-gostack-desafio-03/blob/master/README.md#desafio-03-continuando-aplica%C3%A7%C3%A3o)
- [Etapa 3](https://github.com/Rocketseat/bootcamp-gostack-desafio-09#desafio-09-front-end-do-meetapp)
- [Etapa 4](https://github.com/Rocketseat/bootcamp-gostack-desafio-10#desafio-10-mobile-do-meetapp)

## :rocket: Tecnologias utilizadas

Para a resolução do desafio final, foram utilizadas as seguintes tecnologias:

- [Node](https://nodejs.org/en/)
- [Docker](https://www.docker.com/)
- [PostgreSQL](https://www.postgresql.org/)
- [Express](https://github.com/expressjs/express)
- [Redis](https://redis.io/)
- [Bee-Queue](https://github.com/bee-queue/bee-queue)
- [Nodemailer](https://nodemailer.com/about/)
- [Sequelize](https://sequelize.org/)
- [Jest](https://jestjs.io/)
- [React](https://reactjs.org/)
- [React-Native](https://reactnative.dev/)
- [Redux](https://redux.js.org/)
- [Styled-Components](https://styled-components.com/)
- [Date-Fns](https://date-fns.org/)
- [Unform](https://unform.dev/) (1.0)
- [React Select](https://react-select.com/home)
- [React-Navigation](https://reactnavigation.org/docs/4.x/getting-started) (4.x)
- [Bcryptjs](https://github.com/dcodeIO/bcrypt.js)
- [Reactotron](https://github.com/infinitered/reactotron)
- [Insomnia](https://insomnia.rest/)

## :rocket: Instalação e execução

A seguir, estão descritos todos os passos para a instalação e execução

### :memo: Pré-requisitos

- [Node](https://nodejs.org/en/)
- [Yarn](https://classic.yarnpkg.com/pt-BR/docs/install#debian-stable)
- [Git](https://git-scm.com/downloads)
- [Insomnia](https://insomnia.rest/) (Opcional)
- [Reactotron](https://github.com/infinitered/reactotron) (Opcional)

### :octocat: Clonando o repositório

Abra em sua máquina uma pasta de sua preferência. Em seguida, abra o terminar de sua máquina na respectiva pasta e rode o seguinte comando:

```
$ git clone https://github.com/gabriel-fz/FastFeet.git
```

Ou então, baixe este repositório zipado.

### :bar_chart: Instalação e execução do Back-end

Inicialmente, vá até a pasta api e execute o comando `yarn` para instalar as dependências do projeto.

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

1. Abra a pasta api
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

Caso queira testar as rotas, vá até a pasta api e importe o arquivo `Insomnia.json` no insomnia.

Terminadas todas as configurações, basta executar o seguinte comando na pasta api para iniciar o servidor:

```
yarn dev
```

### :computer: Instalação e execução do Front-end

Inicialmente, vá até a pasta web e execute o comando `yarn` para instalar as dependências do projeto.

Ainda dentro da pasta web, basta executar o seguinte comando para iniciar o client web:

```
yarn start
```

**Observação 1:** Para que o client web funcione corretamente, é necessário que o back-end também esteja rodando. Para isso, utilize o comando `yarn dev` na pasta api como citado anteriormente.

**Observação 2:** Após iniciar o client web, use os seguintes dados para fazer o login:

```
Email: admin@fastfeet.com
Senha: 123456
```

### :iphone: Instalação e execução do Mobile

Inicialmente, vá até a pasta mobile e execute o comando `yarn` para instalar as dependências do projeto.

Para poder testar o aplicativo mobile, pode-se utilizar simuladores virtuais (como o Genymotion) ou celulares físicos via USB ou Wi-Fi. Para cada tipo de ambiente há uma descrição detalhada com os passos a serem seguidos nesta documenteção da RocketSeat: [Ambiente React Native](http://react-native.rocketseat.dev/)

**Observação 1:** O aplicativo mobile foi desenvolvido para **Android** utilizando com base para testes um celular Motorola One Zoom com Android 9.

**Observação 2:** Com base no ambiente onde o aplicativo mobile for testado, é necessário fazer umas configurações de links.

Com o ambiente configurado corretamente, basta rodar o seguinte comando dentro da pasta mobile para instalar o aplicativo:

```
react-native run-android
```

Ainda dentro da pasta mobile, basta rodar o seguinte comando para iniciar o aplicativo:

```
react-native start
```

**Observação 3:** Para que o aplicativo mobile funcione corretamente, é necessário que o back-end também esteja rodando. Para isso, utilize o comando `yarn dev` na pasta api como citado anteriormente.

**Observação 4:** Após iniciar o aplicativo mobile, use um ID de um entregador presente no banco de dados para poder fazer login.

## :rocket: Detalhes extras

Os layouts propostos dos ambientes web e mobile estão presentes nos seguintes links:

- [Layout Web](https://xd.adobe.com/view/62e829fc-4f10-4ac8-70d2-d39b429d43ee-14d9/grid/)
- [Layout Mobile](https://xd.adobe.com/view/a5d56d7d-c1d4-48a8-70ce-8b77f5f417a5-d3e4/grid/)

Os repositórios particulares da api, da web e do mobile (que contém todas as branchs e históricos de commits) estão presentes nos seguintes links:

- [Repositório da api](https://github.com/gabriel-fz/FastFeet-back-end)
- [Repositório da web](https://github.com/gabriel-fz/FastFeet-front-end)
- [Repositório do mobile](https://github.com/gabriel-fz/FastFeet-mobile)
