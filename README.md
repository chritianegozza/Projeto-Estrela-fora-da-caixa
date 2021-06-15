# Projeto-Estrela-fora-da-caixa
A elaboração de um site consumido uma API
<!DOCTYPE html>
<html>
  <head>
         <meta charset="utf-8">
         <meta http-equiv="X-UA-Compatible" content="IE=edge">
         <meta name="viewport" content="width=device-width">
         <title>Rick e Morty</title>
         <link href="style.css" rel="stylesheet" type="text/css" />
        <script src="script.js" defer></script>

  </head>
    
    <body>
      
           
            <!-- titulo da pagina -->
           <h1>Conheça os personagens de Rick e Morty</h1>

            <!-- div container -->
        <div class="container">
             
               <!-- div com tag da imagens e nome do personagem -->

            <div class="vermelho" id="b1"><img><p></p></div>
            <div class="vermelho" id="b2"><img><p></p></div>
            <div class="vermelho" id="b3"><img><p></p></div>
            <div class="vermelho" id="b4"><img><p></p></div>

            

        </div>
      
    </body>
</html>





body {
 background-image: url('http://pavbca.com/walldb/original/0/1/0/5430.jpg');
 background-repeat: no-repeat;
 background-position: center top;
 background-size: cover;
 margin: 0;
 min-height: 320px;
 width: 100%;
   
}

.container {
 display: grid;
 grid-template-columns: 1fr 1fr;
 margin: 50px;
 padding: 30px;
    
}
       
h1 {
 color: white;
 font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
 font-size: 40px;
 text-align: center;
 text-shadow: 0 0 0.2em #8F7
   
}       
   
.nome-personagem1 {
 align-items: center;
 font-family: EuclidBold;
 font-size: 12px;
 font-weight: 700;
 letter-spacing: -0.6px;
 line-height: 15px;
 padding: 9px 23px;
 text-transform: uppercase;
           
}
   
.vermelho img {
 max-width: 100%;
   
}
   
.vermelho {
 background-color: #D0E4D3;
 box-shadow: 0px 0px 6px #393F35;   
 background-color: whitesmoke;   
 margin: 50px auto;
 padding:10px;
 text-align: center;
   
}
   
   
   
   const nomePersonagem1 =  document.querySelector('#nome-personagem1');
const botao = document.querySelector('button');

function adicionaInfo(el,json){
    el.querySelector("img").src = json.image
    el.querySelector("p").innerHTML = json.name
}

gerarValorAleatorio = () => {
    return Math.floor(Math.random() * 671);
}

var r1 = gerarValorAleatorio()
var r2 = gerarValorAleatorio()
var r3 = gerarValorAleatorio()
var r4 = gerarValorAleatorio()


async function personagem(numero){
    const r = await fetch(`https://rickandmortyapi.com/api/character/${numero}`)
    const j = await r.json()
    return j
}



personagem(r1).then(e=> adicionaInfo(b1,e) )
personagem(r2).then(e=> adicionaInfo(b2,e) )
personagem(r3).then(e=> adicionaInfo(b3,e) )
personagem(r4).then(e=> adicionaInfo(b4,e) )








![image](https://user-images.githubusercontent.com/72118415/122115414-d8ef1f80-cdfa-11eb-99bc-743f3787ef6b.png)



![image](https://user-images.githubusercontent.com/72118415/122115325-bc52e780-cdfa-11eb-8787-8ee58a4b5cbe.png)





