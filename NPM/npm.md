# NPM
O NPM é uma ferramenta de trabalho extremamente importante nas aplicações Node. O NPM é usado para buscar qualquer pacote (biblioteca JavaScript) que uma aplicação precisa para ser desenvolvida, testada ou produzida, além de ser adotado para rodar testes ao longo de todo o processo de desenvolvimento.
## Instalação:
1. NPM é instalado com o Node.js
### Exemplo de comando NPM
1. Primeiro passo é criar um diretório para sua aplicação. No prompt, insira os comandos a seguir.
**mkdir myapp**  
**cd myapp**  
2. Use o comando npm init para criar o arquivo package.json da sua aplicação. Esse comando registra para você uma série de informações, como o nome e a versão do seu aplicativo, além do nome do seu "entry point" (index.js por padrão). Por hora, vamos manter a configuração padrão.  
**npm init**  
Se você acessar o arquivo package.json (**cat packge.json**), você verá toda a configuração padrão e, ao final, o tipo de licença que o app está utilizando.  
{  
  "name": "myapp",  
  "version": "1.0.0",  
  "description": "",  
  "main": "index.js",  
  "scripts": {  
    "test": "echo \"Error: no test specified\" && exit 1"  
  },  
  "author": "",  
  "license": "ISC"  
}  
3. Agora, instale o Express dentro do diretório myapp. O pacote será salvo automaticamente na lista de dependências do seu package.json.  
**npm install express**  
A lista de dependências do package.json agora mostra também a versão do Express que estamos usando. Está grifada no final do arquivo.  
{  
  "name": "myapp",  
  "version": "1.0.0",  
  "description": "",  
  "main": "index.js",  
  "scripts": {  
    "test": "echo \"Error: no test specified\" && exit 1"  
  },  
  "author": "",  
  "license": "ISC",  
  "dependencies": {  
    "express": "^4.16.2"  
  }  
}  
4. Para usar o Express, é preciso incluir a função require() no arquivo index.js dentro da sua aplicação. Crie esse arquivo agora mesmo na pasta raiz "myapp" e inclua o código a seguir.  
var express = require('express')  
var app = express()  
app.get('/', function (req, res) {  
  res.send('Hello World!')  
})  
app.listen(8000, function () {  
  console.log('Example app listening on port 8000!')  
})  
O código mostra uma aplicação web bem simples cujo objetivo único é imprimir a mensagem "HelloWorld". Em linhas gerais, esse arquivo importa o módulo do express e o utiliza para criar um servidor (app) que escuta as requisições HTTP pela porta 8000 e imprime a mensagem no console, além de definir qual URL usada para testar o servidor. A função app.get() responde apenas às requisições HTTP feitas com o método GET, desde que especificadas com o path ('/'). Nesse caso, chamando a função para enviar a mensagem Hello World!  
5. Rode a linha de comando abaixo para iniciar o servidor.  
**node index.js**  
**Example app listening on port 8000**  
6. Vá para a seguinte URL (http://127.0.0.1:8000/). Se tudo estiver funcionando corretamente, o browser vai mostrar a mensagem "Hello World!".
