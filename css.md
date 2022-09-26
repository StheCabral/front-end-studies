# Especificidade
### Ranking por seletor 
(Mais específico => mais prioridade na estilização) 
1. Id
2. Classe/Atributo/Pseudo-classe
3. Elementos

* Para tornar um seletor ainda mais específico vamos aumentando a quantidade de seletores associados, por exemplo
`#footer.class-footer` é mais específico que `#footer`, e se eu quiser tornar ainda mais espefíco posso ir 
adicionando elementos ou ainda mais classes

* Porém isso não depende apenas da quantidade, se eu criar um estilo de css referenciando 4 elementos ex.: `section div p` o meu if ainda será mais espefífico `#text` 
pois os parametros são o ranking de especificidade e depois a quantidade

### Comportamento de Cascata
O local do código em que o estilo é aplicado afeta a sua especificidade!
* CSS embutido vs Externo: o que vem por último tem prioridade, se eu linkar o css em cima e embaixo passar
 um `<style> p {color: white} </style>` o embutido terá preferência em caso de conflito.
 * CSS inline: tem menos prioridade que todos `<p color="white">Hello World</p>`
 * Herança: ap atribuir estilo para um elemento pai em alguns casos o elemento filho herda a propriedade

### !important
Evitar! Torna aquela estilização a mais prioritária, a única coisa que sobrescreve um !important é outro

### Dicas
1. Aderir a uma metodologia CSS (BEM, OOCSS, SMACSS, DRY CSS)
2. Utilizar calculadoras de especificidade
