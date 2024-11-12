<h1 align="center">XSS - Refletido</h1>

### Introdução

Opa, queria dizer antes tudo, que esse vai ser o meu primeiro artigo escrito! E portanto, não imagino que tenha uma qualidade tão boa, mas ainda sim espero que dê para entender mais ou menos o conceito da vulnerabilidade. Então prazer! Me chamo Soon e falarei um pouco sobre XSS.


### Sobre oque é XSS?

XSS em sua tradução bruta significa "script em sites",  e isso se refere em executar scripts dentro de um site. Um site normalmente é composto por 2 tipos de linguagem, sendo uma de Hipertexto e outra de Back-End! Sendo as mais comuns utilizadas:

- HTML
- CSS
- JavaScript
- PHP

E XSS pode entrar no contexto de todas! Já que XSS se trata de uma execução de código não proposta pelo código fonte do site.

### O que é o XSS refletido?

Existem 3 tipos de XSS, que são os: "Refletidos", "Storage" e " Dom". Nesse artigo falaremos sobre o permanente mas você pode ver meus outros artigos falando sobre os outros dois tipos no meu GitHub!

Nós encontramos XSS em pontos de entrada dentro de um site! Como uma barra de procura, um parâmetro ou em postagens. Então em um exemplo onde usamos o JS para realizar tal vulnerabilidade e passarmos o link da página em que testamos para o nosso alvo ele receberá o mesmo resultado que a gente! Isso é um xss refletido! Uma execução de código de uma url contaminada e refletida no navegador do nosso alvo!

### Exemplo

Então abrindo o metasploitable e indo para a aba de "xss", podemos ver esse campo de inserção perguntando o nosso nome. Se a gente colocar o nome "Carlos" e dar o "Submit" ele exibirá "Carlos", dentro da página. Então sabendo disso a gente coloca um script simples em JS. E executado esse processo. Temos o seguinte resultado:

<img src="Imagens/XSS - Refletido/ex-01.png"></img>

Aqui podemos ver que na url existe o parâmetro "name" que executa o nome/código que passamos dentro dela! Sendo assim fizemos um XSS funcionar, e se copiarmos a url e esconder dentro de um outro link para o nosso alvo, vai ter o mesmo resultado que o nosso! E em uma situação real poderia ser um script malicioso e assim roubando cookies, sessões, ou até colocando um key-logger dentro do navegador do alvo. Por isso é uma vulnerabilidade tão séria.

Então se você pretende ir testando XSS em um site manualmente, visualize sempre o código fonte da página que carregou o payload e verifique a filtragem que ocorreu.

<img src="Imagens/XSS - Refletido/ex-02.png"></img>

### Tente você mesmo:

Você pode treinar esse tipo de **XSS** nesse laboratório da portswigger:

- [https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded](https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded)

### Finalização:

Se algum dia alguém ler isso, muito obrigado por ler! Espero que você tenha entendido e espero que tenha ficado claro. Futuramente postarei mais artigos de diferentes falhas, explicações do que são diferentes coisas e assim por diante, sempre focando na parte de hacking!

Obs: É sempre importante dizer que o conteúdo colocado nesse artigo é feito meramente para fins educativos e didáticos e não me responsabilizo por qualquer ato ilegal feito a partir do conhecimento desse artigo por mais simples que ele seja!

<p align="right">Soon - (24/08/24)</p>
