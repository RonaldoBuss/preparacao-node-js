# Node.js
## Instalação:
Existem várias versões do Node disponíveis, normalmente as mais recentes possuem melhorias e correções de bugs. Sempre estã disponíveis a versã mais recente LTS e verão corrente.
A orientação é utilizar a versão mais recente LTS, pois é a versã mais estável. A versão corrente contém as últimas funções, mas não tão validadas, então deve utilizar ela apenas se precisar de algumas destas funções.

### Windows
1. Baixar o instalador LTS em [https://nodejs.org/en/](https://nodejs.org/en/)
2. Instalar o Node clicando duas vezes no arquivo de download. Siga a instalação a partir das janelas que vão aparecer na sua tela.

Para validar se a instalação foi realizada com sucesso, basta acessar o proompt de comando do windows e digitar:

**node -v**

Será exibido a versão do Node instalado no computador. O mesmo pode ser feito para o NPM:

**npm -v**

Será exibido a versão do NPM instalada no computador.

Outra forma de testar é criar um servidor web em "puro node" e imprimir a tradicional frase "Hello World" no browser quando visitarmos uma determinada URL.
1. Crie um arquivo chamado hellonode.js e cole dentro dele o código abaixo.

//Chame o módulo HTTP

var http = require("http");

//Crie um servidor HTTP para ouvir as requisições na porta 8000

http.createServer(function (request, response) {

   // Configure o resposta HTTP header com o HTTP status e Content type

   response.writeHead(200, {'Content-Type': 'text/plain'});

   // Envie a resposta do body "Hello World"

   response.end('Hello World\n');

}).listen(8000);

// Imprima URL para acessar o servidor

console.log('Server running at http://127.0.0.1:8000/')

2. No prompt de comando do windows, navegue até o diretório onde o arquivo está salvo e digite o comando abaixo: 

**node hellonode.js**

Será exibido a mensagem abaixo:

**Server running at http://127.0.0.1:8000/** 

3. Acesso no navegador [http://127.0.0.1:8000/](http://127.0.0.1:8000/). Se tudo estiver funcionando bem, o browser vai apresentar a frase "Hello World".
