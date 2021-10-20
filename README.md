# CSS Studies


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
```bash    
**propertyname:value => backgound-color:#cccc99
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
  
  `!important`tem maior importância.
   
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
  ex: ul li:nth-child(3)
 
------------------------------------------ ## CSS-The box model

Todo elemento tem como base um caixa, nem sempre se pode ver notar as caixas, porém elas estão  e deve-se organiza-las. 
  
A caixa é formada pelo conteúdo a parte mais interna, o Padding, o Border e a Margin.
  
  
### Display and Visibility:
  
   - Display é o geral, ou seja quando se diz `display: none;` em alguma tag, ira retirar tudo desde o elemento ao bloco. 
   - Visibility apenas ira esconder o elemento, ou seja o bloco continua lá mantendo seu espaço intacto.
  
  
------------------------------------------ 
 
Algumas ferramentas uteis de Styles
```CSS  
  .menu li:hover{
    Background-color: green
  }
```  
  ->  Sempre que o usuário  passa com o cursor sobre o bloco o bloco trocara o fundo pra verde.
  

 
  
  
