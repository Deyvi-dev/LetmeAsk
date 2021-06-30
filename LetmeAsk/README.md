## 🧐 Sobre o projeto

A aplicação consite ajudar os criadores de conteúdo a colocarem dúvidas com um sistema de classificação baseado em likes e highlights. <br>
<a align="center" target="blank" href="https://letmeask-c1f7a.web.app/">
    <img alt="Site LetMeAsk" src="https://img.shields.io/static/v1?label=site&message=LetMeAsk&color=4953B8&style=flat&logo=vercel">
</a>

## 🎨 Layout

### Telas Mobile

<div align="center">
  <img width="100%" src="./img/mobile.png"/>
</div>

### Telas Desktop-light

<div align="center">
  <img width="100%" src="./img/desktop-light.png"/>
</div>

### Telas Desktop-dark

<div align="center">
  <img width="100%" src="./img/desktop-dark.png"/>
</div>

## ⚙️ Funcionalidades 

- [x] Autenticação com google;
- [x] Criação de sala;
- [x] Input para inserção novas perguntas;
- [x] Sistema de likes para perguntas;
- [x] Destaque para pergunta que esta sendo respondida (Highlighted);
- [x] Destaque para perguntas que já foram respondidas (Answered);
- [x] Exclusão de perguntas;
- [x] Encerramento de sala;
## ⚙️ Milha Extra
- [x] Responsividade;
- [x] Dark mode;
- [x] Modal para remoçao de perguntas ou encerramento de sala;
- [x] Rankeamento de perguntas por highlights e número de likes;
- [x] Perguntas respondidas são enviadas para o fim da lista; 

## Como executar o projeto
### Pré-requisitos
- git 
- Node.js
- NPM ou Yarn
### Variáveis de Ambiente
Além das ferramentas anteriores é necessário criar o arquivo .env.local na raiz do projeto e adicionar as seguintes variáveis

```
REACT_APP_API_KEY="AIzaSyB1DYALyajve7WWoRpyb1FytC9CsUggRcg"
REACT_APP_AUTH_DOMAIN="letmeask-c1f7a.firebaseapp.com"
REACT_APP_DATABASE_URL="https://letmeask-c1f7a-default-rtdb.firebaseio.com"
REACT_APP_PROJECT_ID="letmeask-c1f7a"
```

Caso você deseje alterar as variáveis ambientes você só precisa usar um banco de dados em tempo real com estas regras:
```
{
  "rules": {
    "rooms": {
      ".read": false,
      ".write": "auth != null",
      "$roomId": {
        ".read": true,
        ".write": "auth != null && (!data.exists() || data.child('authorId').val() == auth.id)",
        "questions": {
          ".read": true,
          ".write": "auth != null && (!data.exists() || data.parent().child('authorId').val() == auth.id)",
          "likes": {
            ".read": true,
            ".write": "auth != null && (!data.exists() || data.child('authorId').val() == auth.id)"
          }
        }
      }
    }
  }
}
```
### Instalação
```
# Abra o terminal e copie este repositório com o comando
$ git clone https://github.com/Deyvi-dev/LetmeAsk.git

# Acesse a pasta do projeto no prompt de comando 
$ cd LetmeAsk

# Instale as dependências
yarn install
ou
$ npm install

# Execute a aplicação
$ yarn start
ou
$ npm run start

# Acesse http://localhost:3000 no seu navagador.

```
## 🚀 Tecnologias 
Tecnologias utilizadas para desenvolver o projeto:
- react.js
- typescript
- firebase
- context
- sass
## 🦸‍♂️ **Autor**

<p>
 <sub><strong>🌟 Deyvi_dev🌟</strong></sub>
</p>
.
