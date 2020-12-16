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

| Medida      | Valor                   |
| ----------- | ----------------------- |
| Pixeles     | px                      |
| Centimetros | cm                      |
| Milimetros  | mm                      |
| Inches      | in(1in = 96px = 2.54cm) |
| Puntos      | pt(1pt = 1/72 of 1in)   |
| Picas       | pc (1 pc = 12pt)        |

#### Medidas Relativas 

| Medida | Valor                                                                                                                                                         |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| em     | Se refiere al tamaño actual o longitud del elemento, 2em significa(2  veces el tamaño del elemento). Inicialmente el navegador asigna un valor de 16px a 1em. |
| rem    | Hace referencia al tamaño o longitud del elemento raiz o elemento padre.                                                                                      |
| vw     | Hace referencia al ancho total del dispositivo.                                                                                                               |
| vh     | Relativo a la altura del dispositivo.                                                                                                                         |
| %      | Hace enfasis en el valor que tiene o medida que tiene su padre. De tal manera, que 50% es la mitad del valor de su padre.                                     |

### Propiedades de Texto
 Todos las fuentes tienen caracteristicas importantes que deberiamos tener en cuenta, o por lo menos conoce:

  Propiedad|valor   
  -|-                   
 | font-size   | Define el tamaño de la fuente                                                        |
 | font-family | Define el tipo de fuente (Calibri, arial, etc).                                      |
 | line-height | Especifica la altura de una linea, o la altura que ocupa. El valor por defecto es 1. |
 | font-weight | Sirve para aplicar negrilla en determinadas proporciones a una fuente.               |

Se pueden agregar fuentes de internet, puede buscar en [Google fonts](https://fonts.google.com/) para ver varias opciones gratuitas.

### Normalize
Todos los navegadores dan valores por defecto a cada etiqueta HTML, es decir, dan un (padding, margin) que varia entre cada navegador web. Esto puede ocasionar ciertos dolores de cabeza, y es que esto puede ocasionar que nuestra pagina web se vea diferente en cada navegador web, sujeto a decisiones que deberiamos poder controlar. La solucion para esta problematica se conoce como Normalize, es codigo CSS que viene especializado en dar un formato estandar en todos los navegadores, de modo que podamos empezar a trabajar sin preocupaciones de las variaciones que se puedan producir en el diseño de nuestra pagina.
*Nota*: Es recomendable aplicar en el archivo Normalize.css, con el operador universal la propiedad universal la propiedad:
 ``` 
 box-sizing: border-box; 
 ```
 Con esta propiedad nos aseguramos de darle el ancho y alto correcto a cada elemento. Tambien recomendable aplicar margin y padding con valor de cero. Y al elemento *img* del archivo normalize darle un: ```max-width: 100%;``` para que en los dispositivos moviles las imagenes se ajusten al ancho sin sobrepasarse.

 ### El Modelo de Caja

 En HTML todo son cajas, sin embargo, no todas se comportan de la misma manera. Encontramos dos tipos de caja que podran ser adaptadas con CSS pero que tambien traen un valor por defecto con HTML. Los dos tipos de caja existentes son: *cajas en bloque y cajas en linea*. 


 El comportamiento caracteristico de una caja en bloque es:
 * Fuerza a realizar un salto de linea respecto a los otros componentes.
 * La caja adquiere un ancho del 100% del valor disponible.
 * Las propiedades **height** y **width** se respetan.

El comportamiento que refleja una caja en linea es el siguiente:
* No fuerza a ningun salto de linea, eso quiere decir que puede compartir una mismo linea con otra caja en linea.
* Las propiedades **height** y **width** no se aplican ni se tienen en cuenta.

Para cambiar el comportamiento de nuestras cajas podemos usar la propiedad *display*.



### Propiedades de las Cajas

En HTML todas las etiquetas son cajas o estan envuelta en una por lo tanto, todas las siguiente propiedades aplican para todas las etiquetas:
Atributo|Función
-|-
_padding_ | Es la distancia que hay entre la caja y su contenido (shorthand property).
_margin_ | Es la distancia entre diferentes cajas, tambien se entiende como la distancia que una caja tiene hacia afuera (shothand property).
_border_| Define las caracteristicas que tiene el borde(shorthand property).
_content_| Se refiere al contenido mismo de la caja(line-height).

### Propiedades Intersantes

Propiedad | Uso
-|-
_border-radius_| Le da bordes redondeados a una caja.
_box-shadow_| Se usa para darle el efecto de sombreado a una caja (material design).

### Position

La propiedad _position_ es muy importante, es una propiedad que nos brindad diferentes modos de acomodar nuestros elementos respecto a los otros. Cuando usamos la caracteristica _position_ adquirimos 5 nuevas propiedas que son: _left_ , _right_ ,_top_ ,_bottom_, _z-index_.

Hay 5 diferentes tipos de valores que puede tomar la propiedad _position_:
* _relative_
* _absolute_
* _fixed_
* _sticky_
 * _static_