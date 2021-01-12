# Notas CSS

## Introducción
   1. [Tipos de selectores](#selectores)
   2. [Especificidad](#especifidad)
   3. [Metodologia Bem](#bem)
   4. [Medidas](#medidas)
   5. [Propiedades de texto](#textProperty)
   6. [Normalize](#normalize)
   7. [Modelo de Cajas](#caja)
   8. [Position](#position)
   9. [Overflow](#overflow)
   10. [Float](#float)
   11. [Pseudoelementos](#pseudoelementos)
   12. [Pseudoclases](#pseudoclases)
   13. [Objet Fit](#objet-fit)
   14. [Cursor](#cursor)
   15. [Responsive Design](#responsive)
   16. [Flex Box](#flexbox)

### <a name="selectores">Tipos de selectores </a>
Los selectores (como su nombre lo dice), nos ayudan a identificar y seleccionar los elementos dentro del DOM, una vez seleccionado e identificado el elemento que deseamos procedemos a darle estilo aplicando diversas propiedas.
  * Universal
  * Tipo o etiqueta
  * Clase
  *  ID
  * Atributo
  * Descendiente
  * Pseudaclases
###  <a name="especifidad">Rangos de Especificidad</a>
   La especifidad vino para resolver un problemas muy común en css. El problema radicaba en como se seleccionaban ciertos elemento del DOM, y como seleccionar algunos elementos podia ocasionar comportamientos inesperados en otros. Lo que se busca con la especifidad es poder brindar caracteristicas inmutables o con mayor importancia ante otras, de manera que independientemente de los cambios en otros lugares, su estilo inicial se conserve.
   Los rangos de especifidad son:
  * Important
  * Estilos en linea: Aquellos usados en el HTML.
  * Identificadores
  *
    * Atributos
    * Pseudoclase
    * clases  
  *
    * Elementos
    * Pseudoelementos
  
NOTA: Cuando hay dos selectores que entran en conflicto debido a que tienen un mismo rango de especifidad, el atributo definitivo se define por cascada, es decir, en el mismo orden que son declarados los atributos en el CSS.

### <a name="bem">Metodologia BEM</a>
La metodologia Bem(Block, Element, Modifier) es una metodologia basada o dirigida en la modularización o entendimiento de la jerarquia y especificación de nuestro componentes CSS. Consiste en nombrar las clases basados en un sistema estandar y siguiendo ciertos patrones conocidos, brindando así: 
* Orden
* Escalabilidad
* Entendimiento
* Mantenibilidad

### <a name="medidas"> Unidades de Medida</a>

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

### <a name="textProperty"> Propiedades de Texto</a>
 Todos las fuentes tienen caracteristicas importantes que deberiamos tener en cuenta, o por lo menos conoce:

  | Propiedad   | valor                                                                                |
  | ----------- | ------------------------------------------------------------------------------------ |
  | font-size   | Define el tamaño de la fuente                                                        |
  | font-family | Define el tipo de fuente (Calibri, arial, etc).                                      |
  | line-height | Especifica la altura de una linea, o la altura que ocupa. El valor por defecto es 1. |
  | font-weight | Sirve para aplicar negrilla en determinadas proporciones a una fuente.               |

Se pueden agregar fuentes de internet, puede buscar en [Google fonts](https://fonts.google.com/) para ver varias opciones gratuitas.

### <a name="normalize">Normalize</a>
Todos los navegadores dan valores por defecto a cada etiqueta HTML, es decir, dan un (padding, margin) que varia entre cada navegador web. Esto puede ocasionar ciertos dolores de cabeza, y es que esto puede ocasionar que nuestra pagina web se vea diferente en cada navegador web, sujeto a decisiones que deberiamos poder controlar. La solucion para esta problematica se conoce como Normalize, es codigo CSS que viene especializado en dar un formato estandar en todos los navegadores, de modo que podamos empezar a trabajar sin preocupaciones de las variaciones que se puedan producir en el diseño de nuestra pagina.
*Nota*: Es recomendable aplicar en el archivo Normalize.css, con el operador universal la propiedad universal la propiedad:
 ``` 
 box-sizing: border-box; 
 ```
 Con esta propiedad nos aseguramos de darle el ancho y alto correcto a cada elemento. Tambien recomendable aplicar margin y padding con valor de cero. Y al elemento *img* del archivo normalize darle un: ```max-width: 100%;``` para que en los dispositivos moviles las imagenes se ajusten al ancho sin sobrepasarse.

 ### <a name="caja"> El Modelo de Caja</A>

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
| Atributo  | Función                                                                                                                            |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| _padding_ | Es la distancia que hay entre la caja y su contenido (shorthand property).                                                         |
| _margin_  | Es la distancia entre diferentes cajas, tambien se entiende como la distancia que una caja tiene hacia afuera (shothand property). |
| _border_  | Define las caracteristicas que tiene el borde(shorthand property).                                                                 |
| _content_ | Se refiere al contenido mismo de la caja(line-height).                                                                             |

### Propiedades Intersantes

| Propiedad       | Uso                                                                    |
| --------------- | ---------------------------------------------------------------------- |
| _border-radius_ | Le da bordes redondeados a una caja.                                   |
| _box-shadow_    | Se usa para darle el efecto de sombreado a una caja (material design). |

### <a name="position">Position</a>

La propiedad _position_ es muy importante, es una propiedad que nos brindad diferentes modos de acomodar nuestros elementos respecto a los otros. Cuando usamos la caracteristica _position_ adquirimos 5 nuevas propiedas que son: _left_ , _right_ ,_top_ ,_bottom_, _z-index_.

Hay 5 diferentes tipos de valores que puede tomar la propiedad _position_:
* _relative_
* _absolute_
* _fixed_
* _sticky_
* _static_
  
### <a name="overflow">Overflow</a>

La propiedad overflow hacer referencia al contenido que sobre o no se ajusta correcta a nuestra caja, con overflow podemos decidir que pasa con este contenido y como manejarlo. La propiedad _overflow_ es un shorthand de _overflow-x_ y _overflow-y_.

Posible valores:
* _Visible_:  Es el valor por defecto que tiene la caja.
* _Auto_: Si mi texto o contenido se desborda, automaticamente me cree una barra deslizable.
*  _Scroll_: Genera una barra deslizable independientemente de que sea necesario o no.
*  _Hidden_: Oculta la barra deslizable y tambien su contenido.

### <a name="float">Float</a>

Esta propiedad actualmente es usada para envolver imagenes o elementos en texto, esto le da un efecto muy bueno y formateado a la estructura del texto y el desarrollo.

Puede adquirir 3 propiedades:
* _Left_: La imagen o el elemento pasa a estar en el lado izquierdo del texto.
* _Right_: La imagen o el elemento pasa a estar en el lado derecho del texto.
* _None_: Es como si la propiedad _float_ no se aplicara (default).

 ### <a name="pseudoelementos">Pseudelementos</A>
Un pseudoelemento no hace referencia a un elemento HTML del todo, hace referencia a una parte del elemento que puede variar dinamicamente, ejemplo: la primera linea de un texto. Es importante que la existencia de un pseudelemento depende de un elemento de HTML.

A continuación, mostraremos los diferentes pseudelemento que hay:

| Pseudelemento  | Referencia                                                                                                                                                                                                                                                                    |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _first-line_   | Hace referencia a la primer linea de un texto. No función con elementos _inline_.                                                                                                                                                                                             |
| _first-letter_ | Hace referencia a la primer letra de un texto. No función con elementos _inline_.                                                                                                                                                                                             |
| _placeholder_  | Texto que se encuentra incialmente en un campo de texto y desaparece al empezar a escribir.                                                                                                                                                                                   |
| _selection_    | Cuando seleccionamos texto con el cursor normalmente obtenemos un fondo azul, bueno, con el pseudelemento _selection_ podremos manejar este fondo a nuestro antojo. Tiene sus propiedades un poco limitadas ya que tiene caracteristicas de un elemento en linea ( _inline_). |
| _before_       | Crea contenido "antes" del contenido, sin embargo, no genera contenido real en el DOM, es visible, sin embargo no se puede seleccionar. Requiere propiedad _content_ para su funcionamiento.                                                                                  |
| _after_        | Crea contenido "despúes" del contenido, sin embargo, no genera contenido real en el DOM, es visible, sin embargo no se puede seleccionar. Requiere propiedad _content_ para su funcionamiento.                                                                                |

### <a name="pseudoclases">Pseudoclases</a>

Las pseudoclases son listeners, reaccionan a determinados eventos e interacciones que el usuario va desarrollando a lo largo del desarrollo de la aplicación, volviendo el programa y su diseño mas dinamicos.

Algunas pseudoclases que podremos ver son las siguientes:
| Pseudoclase | Evento                                                                                                                                                                                                                                                                       |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _hover_     | Esta pseudoclase tiene su momento cuando ponemos el mouse encima o sobre el elemento, permitiendonos brindarle propiedades. Se recomiendo usar la pseudoclase _hover_ en conjunto con la propiedad _transition_, ya que ayuda a realizar cambios graduales y no tan bruscos. |
| _link_      | Hace referencia a todos los enlaces o link de la pagina que __NO__ han sido visitados.                                                                                                                                                                                       |
| _visited_   | Hace referencia a todos los enlaces o link de la pagina que __SI__ han sido visitados.                                                                                                                                                                                       |
| _focus_     | Se usa comunmente para los input. Cuando seleccionamos el input para empezar a escribir es cuando pasa de estado desenfocado a enfocado, es entonces cuando tomar lugar la pseudoclase _focus_.                                                                              |
| _active_    | Eesponde al __click__, es decir, cuando clickeamos o seleccionamos un elemento esta pseudoclase actua, permitiendonos modifical el elemento mientras este siendo presionado. Tambien se recomienda el uso de la propiedad _transition_.                                      |
| _lang_      | Recibe un argumento, el cual es el tipo de lenguaje. Para que esto funcione debemos definir en HTML el atributo _lang_ con su respectivo lenguaje. Funciona similar a la selección por atributo.                                                                             |

### <a name="objetFit">Objet Fit</a>

Esta propiedad nos indica como un imagen o video sera desplejado o ajustado en un contenerdor. Si nosotros definimos un contenedor para la imagen con propiedades que no concuerdan con las originales la imagen va a perder su proporción, es por eso que la propiedad _objet-fit_ puede usar alguna de las siguientes propiedades:
Valor|Significado
-|-
_fill_| Estira la imagen hasta lograr ocupar totalmente el elemento, comunmente hace que la imagen pierda sus proporciones logicas (_default value_).
_cover_ | Se escala la imagen para llenar el contenedor, sin embargo no pierde las proporciones logicas de la imagen, lo cual puede dar como resultado que la imagen sea cortada.
_contain_ | Escala la imagen al maximo tamaño posible para poder encajar sin tener que cortar la imagen.
_none_ | Mantinene las medidas iguales de la imagen sin importarle el tamaño de su contenedor. La imagen puede llegar a ser cortada si el tamaño de su contenedor es menor al de la imagen.
_scale-down_| Es una combinación entre el valor _contain_ y _none_. Da como resultado que no se adapta al tamaño de su contenedor a menos que el tamaño del contenedor sea menor al de la misma imagen.
  
### <a name="cursor"> Cursor</a>

Esta propiedad indica que forma y caracteristicas tendra nuestro puntero cuando este sobre determinado elemento, ya que existen demasiados valores se recomienda ver la siguiente pagina donde estan bien explicado: <a href="https://www.w3schools.com/cssref/pr_class_cursor.asp" target ="_blank">Click Aqui para ir al enlace</a>

### <a name="responsive">Responsive Design</a>

Actualmente todas la web se trabajaba sobre computadores de escritorio, lo cual hacia muy sencillo definir la interfaz grafica ya que tanto la figura rectangular de la pantalla como las resoluciones eran muy similares, pero cuando se introdujo al mundo los celulares toda la web tuvo un gran problema de diseño ya que se enfrenta con que los tamaños de las pantallas eran diferentes y podian variar drasticamente. _Responsive Design_ es el nombre que se le dio al concepto de adaptar una interfaz de usuario a diferentes resoluciones y formas vistos en diferentes dispositivos.
Existe un concepto llamado __mobile first__, el cual nos dice que debemos definir el diseñ del celular antes que el de un computador, de manera que el diseño del movil se adapte al del computador y no al reves.

### <a name="flexbox">Flex Box</a>

Antes las paginas web se estructuraban con tablas, lo cual ocasionaba codigo HTML muy extenso y enredado, que si se le daba un mal manejo podia ocasionar desastres en la parte visual, dañando por completo nuestros "estilos". Con la llegada de CSS se soluciono este problema, separando el estilo de la estructura de la pagina. 

Como conté en puntos anteriores la llegada de los dispositivos moviles y las diferentes resoluciones fue otro de los grandes retos que enfrentarón las paginas web. Para solucionar este reto que es el responsive design, podemos usar la propiedad ´´´display: flex;´´´, lo cual es usado para definir un flex container.  Lo cual habilita algunas propiedades propias del __display flex__.  Es importante que tengamos conocimiento de que cuando los hijos directos que tenga el __flex container__ pasan a ser flex items, que tienen un importante rol en este display ya que son los directamente afectados.

Veamos algunas de las propiedades y valores que pueden tomar los flex container y sus hijos.

__order__: Normalmente tenemos los flex items ubicados de una manera acorde a como lo hemos definido en el HTML, sin embargo, este orden puede ser cambiado según nuestra necesidad aplicando la propiedad _order_ a los flex items. El flex item con menor valor en su propiedad _order_ sera el primero en mostrarse.(recibe numeros).

__flex-direction__: Esta propieda se aplica al flex container y puede recibir 4 valores, que son: _row_, _row-reverse_, _column_ y _column-reverse_. Por defecto su valor es _row_, el cual le indica al contenedor que posicione sus items en una fila. El valor_row-reverse_ ubica los items en fila, pero su orden va a ser inverso. Ahora, faltan por describir dos valores que son _column_ y _column-reverse_, según la explicación dada con _row_ se puede decir que es igual a diferencia que los flex items se ubicaran en columnas.

__flex-flow__: Es un shorthand el cual nos abrevia tanto el _flex-wrap_ como el _flex-direction_. Recibe como primer argumento el flex direction(column,row, column-reverse, row-reverse) y como segundo argumento el flex wrap(wrap, wrap-reverse).

__justify-content__: Esta propiedad nos ayuda a indicar como van a estar distribuidos nuestros flex items en nuestro flex container. Es analogo al _text-align_ en textos. Puede tomar cuatro valores diferentes que son: _space-evenly_ ,_space-between_ ,_space-around_ ,_center_.

__align-items__ & __align-content__: Estas propiedades se usan para alinear los flex items en el eje __Y__, sin embargo, _align-items_ se usa cuando se espera una sola linea de cajas, mientas que _align-content_ la podemos usar aún con mayor cantidad de lineas de cajas. Estas propiedades pueden tomar 5 valores, _flex-start_ ,_flex-end_ , _center_ , _baseline_ , _strech_ (_default_).


__align-self__: Se usa para ubicar un flex item en especifico. Esta propiedad es usada en unicamente en el hijo y puede tomar los 5 valores que vimos las propiedades anteriores: _flex-start_ ,_flex-end_ , _center_ , _baseline_ , _strech_ (_default_).

## Propiedades de Flex-items

__flex-grow__: Esta función indica que tanto se expandiran nuestros flex-items respecto al espacio sobrante.

__flex-wrap__: Por defecto flex container van a ubicar todo su contenido en una sola linea, de manera que daran nuevas dimensiones a los flex items. Si queremos que las dimensiones de los flex items se conserven y a medida que la resolución del dispositivo disminuya se vayan añadiendo mas lineas podemos usar esta linea en nuestro css: ´´´flex-wrap: wrap;´´´, otro posible valor para que se añadan mas lineas pero hacia la parte superior del elemento es: ´´´´flex-wrap: wrap-reverse;´´´. El valor por defecto de esta propiedad es _wrap_.

__flex-basis__: Es una propiedad que nos indica las dimensiones iniciales de un _flex-item_, es similar a la propiedad _width_, sin embargo el _flex-basis_ tiene mayor relevancia al momento de difinir las dimensiones.

__flex-shrink__: Indica el espacio que va a ceder un _flex-item_ respecto a sus hermanos cuando requieren encogerse.

