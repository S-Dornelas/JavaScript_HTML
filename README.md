# JavaScript_HTML

Projetos realizados no curso de JAVASCRIPT E HTML: DESENVOLVA UM JOGO E PRATIQUE LÓGICA DE PROGRAMAÇÃO, da Alura em parceriua com a Oracle no projeto ONE - Oracle Next Education.

Neste curso puter ter a experiencia de aprender a lógiva de programação utilizando o JavaScript e HTML, no qual foi colocado em prática: concatenação e os seus comandos como alert(""), <script> </script>, <h1> </h1>, <br>, <a>, <meta charset="UTF-8">, document.write():

<meta charset="UTF-8">

<h1>Meu primeiro teste!</h1>
<br>
  Seria isso um programa? Descubra visitando a Alura <a href="http://www.alura.com.br">aqui</a>!
</br>
<script>
    var ano = 2023;

    document.write("Flávio tem " + (ano - 1977) + " anos");
    document.write("<br>");
    document.write("Joaquim tem " + (ano - 1996) + " anos");
    document.write("<br>");
    document.write("Barney tem " + (ano - 1976) + " anos");
    document.write("<br>");

</script>


*Funções:

<meta charset="UTF-8">

<script>

    function pulaLinha() {
        alert("oi");
        document.write("<br>");
        document.write("<br>");

}

	var ano = 2016;

	document.write("Flávio tem " + (ano - 1977) + " anos");

	pulaLinha();

	document.write("Joaquim tem " + (ano - 1996) + " anos");

	pulaLinha();

	ano = 2017;

	document.write("Barney tem " + (ano - 1976) + " anos");

</script>

*Funções com parâmetros:

<script>
    function pulaLinha() {

        document.write("<br>");
    }

    function mostra(frase){

		    document.write(frase);
    }

    mostra("Olá pessoal!");

    var ano = 2016;

    mostra("Flávio tem " + (ano - 1977) + " anos");

    pulaLinha();

    mostra("Joaquim tem " + (ano - 1996) + " anos");

    pulaLinha();

    ano = 2017;

    mostra("Barney tem " + (ano - 1976) + " anos");

</script>

*Retorno de funções:

function calculaImc(altura, peso) {

    var imc = peso / (altura * altura);
    return imc;

}

var imcFlavio = calculaImc(1.71, 73);
var imcAmigo = calculaImc(1.72, 68);

mostra(imcFlavio);
mostra(imcAmigo);

Interagindo com usuário:

<meta charset="UTF-8">

<script>
functionpulaLinha() {

        document.write("<br>");
}

functionmostra(frase) {
        document.write(frase);
				pulaLinha();
}

var numero1 =prompt("Digite o primeiro número");
var numero2 =prompt("Digite o segundo número");

mostra("O valor de " + numero1 + " vezes " + numero2 + " é: " + (numero1 * numero2));

</script>

Convertendo texto em números:

<meta charset="UTF-8">

<script>
functionpulaLinha() {
        document.write("<br>");
    }

functionmostra(frase) {
        document.write(frase);
pulaLinha();
    }

var convidados = parseInt(prompt("Número de convidados"));
var vips = parseInt(prompt("Número de convidados VIP's"));

var total = convidados + vips;

mostra("O total de convidados é " + total);

</script>

*Condições:

<meta charset="UTF-8">

<script>

functionpulaLinha() {

        document.write("<br>");
        document.write("<br>");
}

functionmostra(frase) {

        document.write(frase);
				pulaLinha();
}

functioncalculaImc(altura, peso) {

return peso / (altura * altura);
}

var nome  =prompt("Informe o seu nome");
var alturaInformada = prompt(nome + ", informe sua altura");
var pesoInformado = prompt(nome + ", informe seu peso");

var imc = calculaImc(alturaInformada, pesoInformado);

document.write(nome + ", o seu IMC é " + imc);

if(imc < 18.5) {

    mostra("Você está abaixo do recomendado");

}

if(imc > 35) {

    mostra("Você está acima do recomendado");
}

if(imc >= 18.5 && imc <= 35) {

    mostra("Seu IMC está excelente!");
}
</script>

*De WHILE para FOR!

var contador = 1;
while(contador <= 10) {
    alert("Contador atual: " + contador);
    contador = contador + 1;
}

*Do FOR para o WHILE!

for(var i = 0; i < 10; i++ ) {
alert( "O resultado é " + (2 * i) );
}


<script>
var i = 0;

Campo de texto e botão:

<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
var segredo = 5;

var input = document.querySelector("input");

function verifica() {

	if(input.value == segredo) {
			alert("Você ACERTOU!");
	}else {
			alert("Você ERROU!!!!!!!!");
	}
input.value = ""; //deixará o imput em branco
input.focus(); //a caixa de texto ganhe foco sempre que recarregarmos a página
}

var button = document.querySelector("button");

button.onclick = verifica; //button.onclick = clicar no butão e acionar a função "verificar()".

</script>

*Array:

<meta charset="UTF-8">

<input/>
<button>Compare com o meu segredo</button>

<script>
	function sorteia() {
	
		returnMath.round(Math.random() * 10);
	
	}
	
	function sorteiaNumeros(quantidade) {
	
		var segredos = [];
		
		var numero = 1;
		
			while(numero <= quantidade) {
			
			var numeroAleatorio =sorteia();
			var achou =false;
			
					if (numeroAleatorio !== 0) {
							for(var posicao = 0; posicao < segredos.length; posicao++) {
							
									 if(segredos[posicao] == numeroAleatorio){
									     achou =true;
									     break;
									 }
							}
									
							 if (achou ==false) {
									segredos.push(numeroAleatorio);
									numero++;
							 }
					   }
					}
			
			   return segredos;
	
      }

		var segredos = sorteiaNumeros(3);

    console.log(segredos);

    var input = document.querySelector("input");
    input.focus();

function verifica() {

var achou =false;

for(var posicao = 0; posicao < segredos.length; posicao++) {

		if(input.value == segredos[posicao]) {
		
		    alert("Você ACERTOU!");
		    achou =true;
		    break;
		}
}

	if(achou ==false) {
	
			alert("Você ERROU!");
	}

input.value = "";
input.focus();
}

var button = document.querySelector("button");

button.onclick = verifica;

</script>



while( i < 10) {
    alert( "O resultado é " + (2 * i) );
    i++;    
}
</script>
