<!--HEADING -->


# taller Colaborativo Cadenas

##  Descripcion

*Diseñar e implementar una clase que a través de métodos de comportamiento ofrezcan una funcionalidad de manejo decadenas al usuario. La clase debe tener un atributo de tipo String inmutable, es decir, una vez definido en el constructorde la clase, no se debe poder cambiar su contenido.*

*Los métodos a implementar deben cumplir con el siguiente contrato1*

 |descripcion | Entradas |Salida|Ejemplo|
 |------------|----------|------|-------|
 |Convertir en nombre Propio el contenido de la cadena  |N/A|Un String con el contenido original como nombre propio.|Sogamoso Ciudad Del Sol y Del Acero|
 |Buscar Cadena de caracteres  |Cadena a buscar (del)|Entero con el número de veces que existe la cadena|eexiste la cadena2 (ignora mayúsculas/minúsculas)|
|Encriptar (método estático)|Cadena a encriptar|La cadena de entrada encriptada,|N/A. Se debe definir el Algoritmo de Encriptación|
|Desencriptar (método estático)|Cadena a desencriptar|La cadena de entrada desencriptada|N/A. Inverso a la encriptación|
|Llenar caracteres|Carácter, cuantas veces, derecha o izquierda|Una cadena concatenada con el carácter n veces por izquierda o por derecha|AAAASogamoso Ciudad del sol y del acero|
|Borrar caracteres|Carácter a borrar |La cadena sin los caracteres|Sgams Ciudad del sl y del acer (Ignorar Mayúsculas/Minúsculas)
|
|Diferencia|Cadena de Caracteres|La diferencia de caracteres de la cadena original con la de entrada|Para cadena de entrada Colombia, Salida = Sgs udd de s y de er|
|Borrar caracteres Izquierda o Derecha|Cadena de Caracteres, por izquierda o por derecha|Borra a la Izquierda o a la Derecha de la cadena los caracteres que existen en la cadena de entrada, hasta que encuentre un carácter que no existe en la cadena de entrada|Para cadena de entrada curador por Derecha = Sogamoso ciudad del sol y del ace (Ignorar Mayúsculas/Minúsculas)|
|Validar dirección de correo electrónico|Correo electrónico a validar |Valor lógico, que indica si la dirección el correo entrante es válida o no.||

## Implementacion de UML

![visual estuds](UML.png)

*se realiza la implementacion de el siguiente diagrama uml en lenguaje java utilizando el IDE eclipse y realizando el documento readme con visual estudio code en estos se carcateriza y se especifica los atributos y los metodos*

*la clase de asociacion Funciones realiza la modificacion de un string , cuya frase es "Sogamoso ciudad del sol y del acero"  se realiza metodos para modificacion conversion especificados en el diagrama que realizan*

* conversion
* buscar repeticion
* mostrar repeticion
* encriptar
* mostrar
* desemcriptar
* borrar
* diferencia
* interseccion
* validad
* borrarcaracteres
* llenar 

## Aspectos de la implementacion 

## funcion convertir 

```java 
public static void Convert(String message) {
		String mensaje = "";
		
		//aqui se divide las palabras 
		String[] palabras = message.split(" ");
		for (int s = 0; s < palabras.length; s++) {
			
			//luego comienza a dividir cada una de las palabras
			String letra1 = palabras[s];
			String stg = "";
			char letrauno = ' ';
			char c = ' ';
			
			for (int i = 0; i < letra1.length(); i++) {
				letrauno = letra1.charAt(0);
				c=letra1.charAt(i);
				
				if (letrauno == ' ') {
					stg = "un nombre no puede empezar por espacio";
				}else if (!Character.isLetter(letrauno)) {
					stg="un nombre no puede empezar por ningun tipo de caracter que no sea letra del alfabeto"+letrauno;
				}
				if (i==0) {
					c=Character.toUpperCase(c);
				}
				stg += c;
				
				
			}
			mensaje += stg + " ";
			
		}
		JOptionPane.showMessageDialog(null, mensaje );	
	}
	
```

## clase runner se utilizo coidgo switch case

```java 
	switch (key) {
	case value: {
		
		yield type;
	}
	default:
		throw new IllegalArgumentException("Unexpected value: " + key);
	}
```
## herramientas usadas 

* StarUML
* Java11
* JUnit 5
* Visual Studio Code

