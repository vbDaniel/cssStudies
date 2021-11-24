# CSS Studies Plural Sight Curses and Guanabara


## O que é CSS?
CSS é um mecanismo que possibilita adcionar um estilo ao documento, pode esta dentro de um documento css separado ou dentro deum tag <style> a escolha é definida de acordo com a necessidade  do programador. 

## Syles Rules:

|     **Selectors**    |
| :------------------: | 
|  1   body {...}.     |  
|  2   #menu{...}.     |
|  3 .bookTitle{...}.  |
  
 
Selector são as formas que se usar para comunicar com o browser oque desejamos estilizar.
  
  1. No local de body pode-se inserir qualquer elemento e o estilo sera aplicado a todos os elementos daquela categoria.
  2. Encontrara um elemento com uma ID fornecida "id" -> #id
  3. Vai editar todos os elementos que estão dentro da classe informada "classename" -> .classename
  
 Outros Selectors são por exemplos:
  - Selector Descendente: div p{...} (apenas os elementos dentro do primeiro elemento seram editados)
  - Selector Child: div > p{...} (apenas os elementos dentro porém logo abaixo do primeiro elemento)
  - Selector Attribute: combina elementos baseado no valor de um atributo dado.
  - Selector Child: div > p{...} (apenas os elementos dentro porém logo abaixo do primeiro elemento)
  - Psuedo Class: a : visited {...}, sempre que o link é visitado algo é editado.
  
------------------------------------------  
```CSS   
propertyname:value => backgound-color:#cccc99
```  
Existem centenas de propertyname, que devem ser estudados, para buscar a melhor opção para uso em seu website.
 
  
## Specifying CSS Property Values:

- Keywords
  - thin, thick, larger
- Medidas:
  - incher(in), points(pt), picas(pc)
- Medidas de tela:
  - pixels(px)
- Medidas relativas:
  - %, em
- Codigo de cores:
  - #rrggbb, rgb(r,g,b)
- Fonts:
  - Helvetica, sans-serif
- Notação de função:
  - rgb(r,g,b), url
 
CSS -> Cascading Style Sheets
  
Cascading: O efeito cascata consi ste em setar prioridades, no caso css setar um pesso para cada regra de estilo, e o com maior peso terá prioridade, por exemplo o estilos do usuário  tem prioridade emcima dos estilos default.
  
  `!important` tem maior importância.
   
- **Regras conflitantes** vindos de uma mesma fonte 
são resolvidos de uma forma simples onde o browser usa a ultima regra listada. Da mesma forma as importações e referências com conteúdo  conflitados o ultimo tem prioridade.
  
------------------------------------------ 
  
- **CSS Reset** substitui o padrao fornecidos pelo browser, assim o programador sempre saber de onde começar suas regras sem depender  do padrão  que varia de cada browser, e começa definitivamente  do 0 com todas as regras.
  
------------------------------------------    
  
 - **Specificity** é o valor do peso, quanto mai s specificity mais importante é o estilo.
  
  | A | Count  of ID selectors.     |
  | B | Count of class and attribute|
  | C | Count of type selectors     |

  if { A = 1 , B = 0, C = 0} 
Specificity = 100 -> 1(A)0(B)0(C)

  style aplicado diretamente dentro da tag é o mais especifico de todas as regras style. 
  
------------------------------------------    
  
Inheritance (Herança) é data por uma árvore, em codigo CSS é dado por `div > p`, nesse caso p é filho de div, assim ao aplicar qualquer estilo em `div > p{...}` o `p {...}` sera diferente de apenas um p. Esse modelo pode ser trabalhado com outros elementos. 
  
  - Para acessar uma certa filha de um elemento: elemento :nth-child(3){...} 
  ex: 
 ```CSS 
  ul li:nth-child(3){...}
 ```
------------------------------------------ ## CSS-The box model
  
**DICA** = usa Background-color pra visualizar  as boxs
  
Todo elemento tem como base um caixa, nem sempre se pode ver notar as caixas, porém elas estão  e deve-se organiza-las. 
  
A caixa é formada pelo conteúdo a parte mais interna, o Padding, o Border e a Margin.
  
  
### Display and Visibility:
  
   - Display é o geral, ou seja quando se diz `display: none;` em alguma tag, ira retirar tudo desde o elemento ao bloco. 
   - Visibility apenas ira esconder o elemento, ou seja o bloco continua lá mantendo seu espaço intacto.
  
  
------------------------------------------ 
 
# **Algumas ferramentas uteis de Styles**
  
```CSS  
  .menu li:hover{
    Background-color: green
  }
```  
  ->  Sempre que o usuário  passa com o cursor sobre o bloco o bloco trocara o fundo pra verde.
  

 
  
  
  
  
   
------------------------------------------ 
  
## Styling Text:
  
  Font é algo que deve ser pensado, visto que nem todo equipamento utiliza certas fontes. Além que deve-se usar fontes que possa simplificar a leitura, uma fonte limpa.
  
  
```CSS
body{
     font-family: sans-serif
}
```
  Existe diversas fontes e deve-se escolher a que mais se adapta ao projeto. Porém para resolver o problema de um aparelho nao possuir algumas fonte:
  
```CSS
body{
     font-family: Arial, Helvetica, sans-serif
}
```
O Browser irá  percorrer por Arial, Helvetica e Sans-serif a primeira fonte que ele possuir será a usada.
  
  - Sobre o tamanho a fonte, também  nos leva a uma escolha o tamanho Absolute(pixel - px) que não se altera ou Variável relativo(% ou 'em') que se altera de acordo com o tamanho da tela ou da linha.
  
```CSS
body{
  font-family: Arial, Helvetica, sans-serif
  font-size: 0.9em;
  font-size: 20px;
  font-size: 
  font: italic 0.9em Arial;
}
```  

------------------------------------------ 
  
# LAYOUT with CSS 
  
  ### Position 
Propriedade de layout da página que permite posicionar qualquer elemento (de bloco) com um dos quatro valores: top, right , bottom e left. O position ignora o PADDING  e o MARGIN do elemento, por isso é recomendado. Não se importa de sobrepor elementos.

O tipo de position padrão do CSS é o posistion: static.
Tipos de positions: 
- Static
Posiciona os elementos em pilha, um seguindo o outro, seguindo o fluxo da página para baixo.
- Relative
Posiciona o elemento de forma relativa ao posicionamento anterior, geralmente o estático por ser default.
- Absolute
Remove um elemento do fluxo do documento, move o elemento para uma posição específica  em relação ao Body.
- Fixed
Muito parecido com o Absoluto, exceto que o posicionamento é relativo à própria janela, então se eu quiser uma posição fixa, ela permanecerá nessa posição mesmo se o usuário rolar a página para baixo. Usado geralmente para elementos de toolbar, que tem que ficar fixo na tela de qualquer forma, mesmo que o conteúdo da página desça.
  
  Exemplos de uso in code:
```CSS 
#buttons inpiut:last-child{
  position: relative; //absolute or fixed
  top: 100px;
  left: 300px;
}
```
  - Deve-se usar o position relative com cuidado pois pode sobrepor outros elementos, sempre tenha em mente se há espaço  ou não.
---------------------------------------------------
## Floating and Cleanring
 
### Float elements
Permite que o elemento se mova para esquerda ou para a direita e que outro conteúdo flutue ao lado dele em um fluxo normal. (estático).  O clear remove essa flutuação e impede que um elemento seja flutuante.
  
```CSS  
#figure{
  float: left; // A figura é jogada para esquerda 
  margin-right: 5px;
}
  
<p style= "clear:both"> // Vai impedir o texto de ter algo nas laterais, pode ser usado no local de 'both' -> 'left' or 'right'
```  
---------------------------------------------------   
 # GUANABARA  

 ## Conceitos de Cores e suas importâncias:
---------------------------------------------------
  
  As cores influenciam também o nosso humor. O amarelo, por exemplo, desperta alegria, otimismo. Já a cor cinza, quando em excesso, pode causar um efeito contrário, gerando um estado deprimido. Mas não  necessariamente  me proibe utilizar as cores, apenas é necessário  tomar cuidado com o uso. Pois um site harmonico sobre as cores e organização do mesmo, ganham de outros site que não levam isso em consideração. 
  Importância por exemplo o azul tem a a maior taxa de aprovação  e a menor de rejeição. Segue outros  exemplos:
  
  ![image](https://user-images.githubusercontent.com/87997848/142464927-cf0f137e-e099-4cdd-927e-693e55705b72.png)

  O constraste de letras de fundo, pode causar alto índice  de cansaço, exemplo de fundo preto com letras brancos. 
  
  ## Cores representadas no CSS:
  ---------------------------------------------------
 É possível   representar as cores de 4 formas diferente, como:
  - o nome das cores, porém  é limitado(ex: []blue};
  - Hexadecimal (ex: #0000ff);
  - RGB (ex: rgb(0,0,25);
  - HSL (ex: hsl(240,100%,50%));
 ** Todos é possível  inserir a transparência  no final de todos.**  
 
  
  ## Cores e suas hamonias:
  ---------------------------------------------------
  Cores primárias:
  
  ![Screen Shot 2021-11-24 at 10 38 40](https://user-images.githubusercontent.com/87997848/143248793-b1391537-7449-457c-a310-a1a73fa69d37.png)

  
  Cores secundárias:
  
  ![Screen Shot 2021-11-24 at 10 40 51](https://user-images.githubusercontent.com/87997848/143249149-efaf28f3-950a-4cdb-b30e-92cf01261263.png)

  Atençao ao fazer um site, uma paleta tem que ser focada entre 3 à 5 cores, sem contar o preto e branco que já consta. Uma ferramenta interessante de se fazer uma peleta é o Adobe Colorque se criar uma paleta apartir de um circulo cromático. Outra ferramenta é o Paletton que trabalha de forma parecida, pórem podesse aplicar a paleta com testes em sites, e modelos pre-prontos(Pag-Layout). 
  
  
  ## Tipografia 
  ---------------------------------------------------
  TipoGrafia é um tipo de estudo de como escrever de forma mais inteligente  para passar mais sensações  ou apenas facilitar a leitura, hoje esse estudo é muito importante para a criação  dos sites. 
  
  A anatomia de uma fonte é de suma importância, visto que a o tamanho de uma fonte é dada pelo tamanho do corpo da fonte, que é: 
  
  ![Screen Shot 2021-11-24 at 12 22 03](https://user-images.githubusercontent.com/87997848/143266078-cbf04da8-cbad-43b7-b7b7-8561c91c920f.png)

  Fique esperto com a família  das fontes visto que nem todos os browers possuem as todas fontes, então montar um família é importante  visto que caso não  há uma certa fonte o browser busca outras dentro da família. Também  é possível  usa uma genérica  para um caso de não existir  nenhuma ele buscara por exemplo "serif", buscará qualquer fonte com serif.
  

  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
