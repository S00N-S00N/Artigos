<h1 align="center"> XSS - Stored </h1>

### Introdução:

Opa! Estou aqui com mais um artigo, desculpa pela demora de soltar esse aqui mas provavelmente o próximo vai demorar para sair também. Então dito isso irei começar!

### O que é XSS **Stored**?

Dentro de alguns sites existe campos de comentários, campos de postagens e etc… esse tipo de campos de texto são geralmente armazenados dentro de um banco de dados do lado do servidor, e assim quando alguém carrega uma página que contém essas postagens/comentários, serão exibidos para eles o que outro usuário digitaram.

Sabendo que a maioria dessas postagens contém textos, podemos aplicar "xss" lá! E assim o código será executado em todos os “browsers” de todas as pessoas que acessaram aquela página. Isso é “xss - stored” um xss armazenado dentro do banco de dados de um servidor.

### Exemplo:

Dentro do **DVWA** temos uma página onde podemos fazer algumas postagens.

<img src="Imagens/XSS - Stored/ex-01.png"></img>

Sabendo disso, podemos testar alguns payloads ou comandos que achamos que possam funcionar nessa página. E como você pode ver ele necessita que coloquemos um nome para a postagem, mas tem um porém, o número de caracteres máximo que é possivel colocar está igual a 10.

<img src="Imagens/XSS - Stored/ex-02.png"></img>

Para resolver esse problema podemos alterar o código fonte da página ao nosso favor para burlar isso.

<img src="Imagens/XSS - Stored/ex-03.png"></img>

Agora feito isso tudo, podemos colocar nosso payload dentro do site e ter o seguinte resultado:

<img src="Imagens/XSS - Stored/ex-04.png"></img>

### Tente você mesmo:

Você pode treinar esse tipo de **XSS** nesse laboratório da portswigger:

- [https://portswigger.net/web-security/cross-site-scripting/stored/lab-html-context-nothing-encoded](https://portswigger.net/web-security/cross-site-scripting/stored/lab-html-context-nothing-encoded)

### Finalização:

Espero que você tenha gostado e tenha entendido qual é o conceito desse **XSS** e que possa aplicar ele na prática a partir daqui! Lembre-se de ter 20% de teoria 70% nos estudos.

Obs: É sempre importante dizer que o conteúdo colocado nesse artigo é feito meramente para fins educativos e didáticos e não me responsabilizo por qualquer ato ilegal feito a partir do conhecimento desse artigo por mais simples que ele seja!

<p align="right">Soon - (10/08/24)</p>
