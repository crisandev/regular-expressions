Expresiones Regulares (Regex):

Las expresiones regulares, también conocidas como regex, son patrones de caracteres que se utilizan para buscar y manipular cadenas de texto. Permiten realizar búsquedas avanzadas, extracciones y reemplazos de texto de manera eficiente y flexible.

Imagina que son como recetas de búsqueda que le dices a tu computadora para encontrar cosas específicas en un texto. Imagina que estás buscando palabras que empiecen con "gat" en un libro. En lugar de leer todo el libro, puedes decirle a la computadora que busque palabras que comiencen con "gat", como "gato" o "gatito". Las expresiones regulares hacen eso, pero para cualquier patrón de letras o números que puedas imaginar.

Por lo general, las expresiones regulares se componen de caracteres literales y metacaracteres que representan conjuntos de caracteres, cuantificadores y otros elementos que definen el patrón a buscar en una cadena de texto.

Y ¿qué son los caracteres literales y metacaracteres?

Los caracteres literales en una expresión regular son aquellos que coinciden exactamente con el mismo carácter en la cadena de texto que se está buscando. Por ejemplo, si tienes la expresión regular `abc`, coincidirá únicamente con la secuencia de caracteres "abc" en la cadena de texto.

Por otro lado, los metacaracteres son caracteres especiales que tienen un significado especial dentro de una expresión regular y que se utilizan para definir patrones más complejos. Algunos ejemplos comunes de metacaracteres son el punto (.), circunflejo (^) y otros.

Los metacaracteres son muy útiles para definir patrones más complejos en una expresión regular, permitiendo realizar búsquedas más flexibles y avanzadas en cadenas de texto.

Ejemplo:

Supongamos que queremos validar si una cadena de texto contiene un número de teléfono en el formato común de 10 dígitos en Estados Unidos. Podemos utilizar la siguiente expresión regular:

regex

```javascript
console.log(^\d{3}-\d{3}-\d{4}$)
```

Esta expresión regular buscará cadenas que cumplan con el patrón de tres dígitos, seguidos de un guion, seguidos de otros tres dígitos, otro guion y finalmente cuatro dígitos. Por ejemplo, esta expresión regular coincidirá con cadenas como "123-456-7890" pero no con "abc-123-defg".

```javascript
// Expresión regular para validar un número de teléfono en el formato de 10 dígitos (XXX-XXX-XXXX)
let telefonoRegex = /^\d{3}-\d{3}-\d{4}$/;

// Cadena de texto a validar
let numeroTelefono = "123-456-7890";

// Verificar si la cadena de texto cumple con el patrón de la expresión regular
if (telefonoRegex.test(numeroTelefono)) {
  console.log("El número de teléfono es válido.");
} else {
  console.log("El número de teléfono no es válido.");
}
```

### Formación de Expresiones Regulares

Las expresiones regulares se forman utilizando una combinación de caracteres literales y metacaracteres que representan patrones de búsqueda. Aquí tienes una explicación detallada de cómo se forman y las reglas que siguen:

1. **Caracteres Literales**: Los caracteres literales coinciden exactamente con ellos mismos en la cadena de texto. Por ejemplo, `abc` coincidirá exactamente con la secuencia de caracteres "abc".

Por supuesto, aquí está el texto en formato Markdown sin enumeración y con el título comenzando en 2:

2. **Metacaracteres en Expresiones Regulares**

- **`.` (punto)**  
Expresión Regular: `b.t`  
Coincidencias: "bat", "bet", "bit", "bot", "but", pero no "b\nn" (debido a que el punto no coincide con saltos de línea).

- **`^` (circunflejo)**  
Expresión Regular: `^start`  
Coincidencias: "start", "start of something", pero no "in the start".

- **`$` (dólar)**  
Expresión Regular: `end$`  
Coincidencias: "end", "end of something", pero no "ending".

- **`*`**  
Expresión Regular: `go*gle`  
Coincidencias: "ggle", "gogle", "google", pero no "gooooogle" (debido a que solo coincide con cero o más repeticiones de "o").

- **`+`**  
Expresión Regular: `go+gle`  
Coincidencias: "gogle", "google", pero no "ggle" (debido a que al menos una "o" es necesaria).

- **`?`**  
Expresión Regular: `colou?r`  
Coincidencias: "color", "colour", pero no "colouur" (debido a que la "u" es opcional).

- **`\`**  
Expresión Regular: `\.`  
Coincidencias: ".", pero no "a" o cualquier otro carácter (debido a que el punto se ha escapado y ahora coincide literalmente con un punto).

- **`|` (barra vertical)**  
Expresión Regular: `cats|dogs`  
Coincidencias: "cats", "dogs", pero no "birds" (debido a que solo coincide con "cats" o "dogs").

- **`[]` (clase de caracteres)**  
Expresión Regular: `[aeiou]`  
Coincidencias: Cualquier vocal en minúscula.

- **`()` (paréntesis)**  
Expresión Regular: `(hello)+`  
Coincidencias: "hello", "hellohello", "hellohellohello", etc.

- **`{}` (cuantificador)**  
Expresión Regular: `o{2}`  
Coincidencias: "oo", pero no "o" o "ooo" (debido a que especifica exactamente dos repeticiones de "o").


3. **Clases de Caracteres**: Permiten especificar un conjunto de caracteres que pueden coincidir en una posición determinada en la cadena. Por ejemplo, `[abc]` coincidirá con cualquiera de los caracteres "a", "b" o "c".

4. **Cuantificadores**: Especifican cuántas veces debe aparecer un elemento en la cadena. Por ejemplo, `a{2,4}` coincidirá con "aa", "aaa" o "aaaa".

5. **Agrupamiento**: Los paréntesis se utilizan para agrupar elementos y aplicar operadores a grupos de caracteres. Por ejemplo, `(ab)+` coincidirá con "ab", "abab", "ababab", etc.

6. **Anclas**: Te permiten coincidir con el inicio o el final de una cadena. Por ejemplo, `^abc` coincidirá con "abc" solo si "abc" está al principio de la cadena.

### Ejemplo

La expresión regular `^\d{3}-\d{3}-\d{4}$` coincide con un número de teléfono en formato "###-###-####", donde cada "#" representa un dígito del 0 al 9. Aquí:
- `^\d{3}`: Coincide con tres dígitos al inicio de la cadena.
- `-`: Coincide con el guion literal entre los grupos de dígitos.
- `\d{3}`: Coincide con otros tres dígitos.
- `-`: Otro guion literal.
- `\d{4}$`: Coincide con cuatro dígitos al final de la cadena.

Espero que esta explicación te haya ayudado a comprender cómo se forman las expresiones regulares y las reglas que siguen.

### Guía para Validar Direcciones de Correo Electrónico con Expresiones Regulares

#### Paso 1: Definir el Patrón
Para validar direcciones de correo electrónico, necesitamos un patrón que describa la estructura básica de una dirección de correo electrónico. El patrón general es `usuario@dominio.extensión`, donde `usuario`, `dominio` y `extensión` pueden contener letras, números, guiones y puntos.

#### Paso 2: Utilizar Caracteres Literales
Incluimos los caracteres literales "@" y "." en nuestro patrón, ya que son parte fundamental de una dirección de correo electrónico.

#### Paso 3: Utilizar Metacaracteres para Patrones Más Complejos
Utilizamos metacaracteres como `+`, `@`, y `\.` para representar patrones más complejos. Por ejemplo, `+` indica que el conjunto de caracteres alfanuméricos antes de "@" puede aparecer una o más veces, y `\.` coincide literalmente con el carácter ".".

#### Paso 4: Prueba tu Expresión Regular
Una vez que hemos construido nuestra expresión regular, la probamos con diferentes ejemplos de direcciones de correo electrónico para asegurarnos de que funcione correctamente.

#### Paso 5: Ajustar y Refinar según sea Necesario
Si la expresión regular no coincide con todas las instancias deseadas o coincide con demasiadas, ajustamos y refinamos el patrón según sea necesario. Por ejemplo, podemos agregar restricciones adicionales para validar ciertos caracteres en el usuario o la extensión del correo electrónico.

#### Paso 6: Documentar tu Expresión Regular
Finalmente, documentamos claramente en nuestro código el propósito de la expresión regular y cómo se espera que funcione. Esto facilitará su comprensión y mantenimiento para nosotros y otros desarrolladores que trabajen en el proyecto.

---

#### Expresión Regular Completa:
```regex
/^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/
```
- `^`: Coincide con el inicio de la cadena.
- `[a-zA-Z0-9._%+-]+`: Coincide con uno o más caracteres alfanuméricos, así como con algunos caracteres especiales como ".", "_", "%", "+", y "-". Esto representa el usuario en la dirección de correo electrónico.
- `@`: Coincide literalmente con el carácter "@".
- `[a-zA-Z0-9.-]+`: Coincide con uno o más caracteres alfanuméricos, ".", o "-" para representar el dominio.
- `\.`: Coincide literalmente con el carácter ".".
- `[a-zA-Z]{2,}`: Coincide con dos o más caracteres alfabéticos para representar la extensión del dominio.
- `$`: Coincide con el final de la cadena.




VENTAJAS VS DESVENTAJAS 


| Ventajas                                           | Desventajas                                             |
|----------------------------------------------------|---------------------------------------------------------|
| Flexibilidad en la búsqueda de patrones           | Curva de aprendizaje inicialmente pronunciada           |
| Eficiencia en la manipulación de texto            | Dificultad para escribir y entender patrones complejos  |
| Validación de datos                                | Pueden volverse difíciles de mantener en patrones muy complejos |
| Búsqueda y filtrado avanzado                      | Pueden ser propensas a errores si no se escriben correctamente |
| Funciones integradas en muchos lenguajes de programación | No son adecuadas para todas las tareas de procesamiento de texto |
| Portabilidad                                       | Pueden afectar el rendimiento en grandes volúmenes de datos |


### Expresiones Regulares vs Operadores Lógicos

| Expresiones Regulares | Operadores Lógicos |
|-----------------------|--------------------|
| - Son ideales para buscar patrones complejos dentro de cadenas de texto. <br> - Proporcionan una forma poderosa y flexible de realizar búsquedas, extracciones y reemplazos de texto. <br> - Son eficientes en la manipulación y validación de datos cuando se trata de patrones específicos. | - Son simples y fáciles de entender, especialmente para tareas básicas de comparación y filtrado. <br> - No tienen una curva de aprendizaje pronunciada y son más intuitivos para muchos desarrolladores. |
| - Pueden tener una curva de aprendizaje pronunciada, especialmente para patrones complejos. <br> - Pueden ser propensas a errores si no se escriben correctamente. | - Pueden ser limitados en términos de la complejidad de los patrones que pueden manejar. <br> - No son tan flexibles como las expresiones regulares para tareas avanzadas de manipulación de texto. |







### Casos de uso de expresiones regulares:

1. **Validación de Formularios**: Las expresiones regulares son muy útiles para validar entradas de formularios en páginas web, como direcciones de correo electrónico, números de teléfono, códigos postales, etc. Por ejemplo, puedes usar una expresión regular para asegurarte de que un correo electrónico ingresado tenga el formato adecuado.

2. **Extracción de Datos**: Puedes usar expresiones regulares para extraer información específica de un texto, como nombres de archivos, direcciones web o números de serie de productos, haciendo que el procesamiento de datos sea más eficiente.

3. **Análisis de Logs**: En el análisis de registros (logs) de servidores o aplicaciones, las expresiones regulares pueden ayudar a identificar patrones específicos, como direcciones IP, URL solicitadas, o mensajes de error, lo que facilita la identificación de problemas y la optimización del rendimiento.

4. **Manipulación de Texto**: Las expresiones regulares son útiles para manipular texto, como eliminar espacios en blanco, cambiar el formato de fechas o reemplazar ciertas palabras por otras. Por ejemplo, puedes usar expresiones regulares para encontrar y reemplazar todas las ocurrencias de una palabra en un documento.

5. **Extracción de Datos de Texto no Estructurado**: Cuando trabajas con texto no estructurado, como páginas web o documentos de texto, las expresiones regulares pueden ayudar a extraer información específica de manera eficiente, como nombres de personas, fechas, o precios.

6. **Filtrado de Datos**: En bases de datos o conjuntos de datos grandes, las expresiones regulares pueden ser útiles para filtrar registros que coincidan con ciertos criterios, como direcciones de correo electrónico válidas o nombres de archivos específicos.

7. **Procesamiento de Texto en Línea de Comandos**: En entornos de línea de comandos, las expresiones regulares pueden ser utilizadas para realizar tareas de procesamiento de texto, como búsqueda y reemplazo en archivos, extracción de información de archivos de registro, etc.

8. **Validación de Código Postal**: En aplicaciones que requieren la entrada de códigos postales, las expresiones regulares pueden ayudar a validar que los códigos ingresados tengan el formato correcto para el país correspondiente.

9. **Análisis de Datos de Redes Sociales**: En el análisis de datos de redes sociales, las expresiones regulares pueden ser útiles para extraer información específica de publicaciones, comentarios o perfiles de usuarios, como menciones, hashtags o enlaces.

10. **Escaneo de Documentos**: En aplicaciones de escaneo de documentos, las expresiones regulares pueden ayudar a identificar y extraer información relevante, como números de identificación, fechas o nombres, de documentos escaneados o archivos de texto.

11. **Manipulación de HTML/XML**: Para trabajar con documentos HTML/XML, las expresiones regulares pueden ser útiles para extraer datos de etiquetas específicas, eliminar etiquetas o realizar cambios en el formato del documento.

12. **Análisis de Logs de Aplicaciones Web**: En el análisis de logs de aplicaciones web, las expresiones regulares pueden ser utilizadas para identificar patrones específicos de actividad, como solicitudes HTTP, errores de servidor o intentos de acceso no autorizados.


Puedes ir a la carpeta casos_practicos donde vas a ver algunas implementaciones
Los ejemplos se abordan en los lenguajes de programación de JavaScript, Java, C#