# Notas CSS

## Introducción
### Tipos de selectores 
  * Universal
  * Tipo o etiqueta
  * Clase
  *  ID
  * Atributo
  * Descendiente
  * Pseudaclases
###  Rangos de Especificidad
   La especifidad vino para resolver un problemas muy común en css. El problema radicaba en como se seleccionaban ciertos elemento del DOM, y como seleccionar algunos elementos podia ocasionar comportamientos inesperados en otros. Lo que se busca con la especifidad es poder brindar caracteristicas inmutables o con mayor importancia ante otras, de manera que independientemente de los cambios en otros lugares, su estilo inicial se conserve.
   Los rangos de especifidad son:
  * Important
  * Estilos en linea: Aquellos usados en el HTML.
  * Identificadores
  *
    * Clases
    * Pseudoclase
    * clases  
  *
    * Elementos
    * Pseudoelementos
  
NOTA: Cuando hay dos selectores que entran en conflicto debido a que tienen un mismo rango de especifidad, el atributo definitivo se define por cascada, es decir, en el mismo orden que son declarados los atributos en el CSS.

### Metodologia BEM
La metodologia Bem(Block, Element, Modifier) es una metodologia basada o dirigida en la modularización o entendimiento de la jerarquia y especificación de nuestro componentes CSS. Consiste en nombrar las clases basados en un sistema estandar y siguiendo ciertos patrones conocidos, brindando así: 
* Orden
* Escalabilidad
* Entendimiento
* Mantenibilidad

### Unideades de Medida

En CSS podemos encontrar 2 tipos de medida **relativas y fijas**, las cuales se pueden ver reflejadas en la siguiente lista: 

#### Medidas Absolutas:

Medida | Valor
-|-
 Pixeles | px
Centimetros| cm
 Milimetros|mm
 Inches| in(1in = 96px = 2.54cm)
 Puntos| pt(1pt = 1/72 of 1in)
 Picas| pc (1 pc = 12pt)

#### Medidas Relativas 

Medida|Valor
-|-
em | Se refiere al tamaño actual o longitud del elemento, 2em significa(2  veces el tamaño del elemento). Inicialmente el navegador asigna un valor de 16px a 1em.
rem  | Hace referencia al tamaño o longitud del elemento raiz o elemento padre.
vw | Hace referencia al ancho total del dispositivo.
vh | Relativo a la altura del dispositivo.
% | Hace enfasis en el valor que tiene o medida que tiene su padre. De tal manera, que 50% es la mitad del valor de su padre.

### Propiedades de Texto
 Todos las fuentes tienen caracteristicas importantes que deberiamos tener en cuenta, o por lo menos conoce:

 Atributo|valor
 -   |-
 font-size   |Define el tamaño de la fuente 
font-family   | Define el tipo de fuente (Calibri, arial, etc).
line-height   | Especifica la altura de una linea, o la altura que ocupa. El valor por defecto es 1.
font-weight| Sirve para aplicar negrilla en determinadas proporciones a una fuente.

Se pueden agregar fuentes de internet, puede buscar en [Google fonts](https://fonts.google.com/) para ver varias opciones gratuitas.