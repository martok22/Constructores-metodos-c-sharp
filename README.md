POO: Métodos constructores y sobrecargas
========================================
Prof. Octavio villegas  http://www.octavio.com.ar.

**Qué vas a aprender:**
  - [Constructores](#Contructores)
  - [Métodos](#Métodos)
  - [Enumerados](#Enumerados)
  - [Accesores de Visibilidad](#AccesoresDeVisibilidad)
 

los conceptos explicados son concatenados entre sí, toda la práctica  está dividida en clases y cada clase tienen objetivos intermedios que cumplir.

####Nota:*la clase 1 y la clase 2, son la introducción a la IDE y el paralelismo entre la sintaxis del lenguaje “C” con C# (C-Sharp).*
Clase 3
-------
Ejercitación

<h5>Objetivo: comprender el funcionamiento de un constructor por defecto, this, relacion de composición.</h5>
-------------------------------------------------------------------------------------
<h6> <strong>A. </strong> inicialización del objeto</h6>
<ol>

    	<li>Crear la clase publica Rueda, con un atributo de tipo  String llamado marca y el atributo de tipo int tamaño.</li>
	<li>Crear un objeto en el MAIN , inspeccionar los atributos y verificar que el string está en null y el tamaño en 0.</li>
</ol>

<h6> <strong>B.</strong> Modificación de valores por defecto.</h6>
<ol>

    	<li>Crear un constructor por defecto sin código en su implementación.</li>
	<li>Verificar ejecutando paso a paso que ingresa al constructor.</li>
	<li>Modificar el atributo “This. Marca”  dentro del constructor por defecto con el texto “Sin Marca”.</li>
	<li>Verificar ejecutando paso a paso que ingresa al constructor y que modifica el atributo.</li>
	<li>Crear 3 objetos RUEDA y ejecutar pasó a paso verificando el ingreso al constructor por defecto.</li>

</ol>
<h6> <strong>C. </strong> Relación de composición de clases.</h6>

<ol>
		<li>	Creamos la clase Auto, que posea un atributo string  fabricante y cuatro Ruedas con los siguientes nombres (ruedaDD, ruedaDI, ruedaTD, ruedaTI).</li>
		<li>Crear el constructor por defecto y verificar que cada objeto rueda es inicializado en NULL.</li>
		<li>Inicializar los objetos rueda en el constructor por defecto.</li>
		<li>Verificar que cada objeto no esté en NULL.</li>
</ol>


<h5>Objetivo: comprender la funcionalidad y la sintaxis de un constructor estático.</h5>
-------------------------------------------------------------------------------------
<h6> <strong>D. </strong>Constructor Estático.</h6>
<ol>
	<li>Crear un constructor de clase  en AUTO.</li>
	<li>Verificar que:
	<ul>
		<li>No puede tener modificador de visibilidad</li>
		<li>No se puede utilizar el THIS.</li>
		<li>Verificar, poniendo punto de quiebre, que es lo primero que se ejecuta, antes de utilizar cualquier miembro de instancia o de clase.</li>
	</ul>
	</li>
	<li>Crear un atributo estático llamado contador de objetos.</li>
	<li>En el constructor por defecto inicializarlo en 0.</li>
</ol>
<h5>Objetivo: definición, casteo y utilización de enumerados.</h5>
-------------------------------------------------------------------------------------
<h6> <strong>E. </strong> Enumerados e instancias únicas en atributos estáticos.</h6>

<ol>
		<li>Crear el enumerado <strong>eFabricante</strong> (Ford, Chevrolet y honda).</li>
		<li>Verificar en el MAIN como se crear una variable de tipo eFabricante.</li>
		<li>Verificar en el MAIN como se castea una variable de tipo eFabricante.</li>
		<li>Cambiar el tipo de datos del atributo fabricante de la clase auto, de string a eFabricante.</li>
		<li>En el constructor  por defecto inicializar el valor del atributo fabricante.</li>
		<li>Hacer que el fabricante se genere Random entre las tres opciones existentes.</li>
		<li>Crear 5  objetos autos y verificar que se carguen los fabricantes de manera Random.</li>
		<li>Crear un atributo estático de tipo Random.</li>
		<li>Iniciarlizar en objeto Random en el <strong>constructor estático.</strong></li>
</ol>
<h5>Objetivo: utilización de atributos públicos y privados.</h5>
-------------------------------------------------------------------------------------
<h6> <strong>F. </strong> Atributos públicos y privados.</h6>

<ol>
	<li>En la clase <strong>AUTO</strong> creamos el atributo privado “kilometrosRecorridos”.</li>
	<li>El atributo fabricante  de la clase <strong>AUTO</strong> debe ser PRIVADO</li>
	<li>Creamos los métodos que me permitan interactuar con el atributo por fuera de la clase:
	<ul>
		<li>public void AgregarKilometros (int kilometros).</li>
		<li>public void VolverACero ().</li>
		<li>public int GetKms ().</li>
	</ul>
	</li>
	<li>Hacer el método: public void MostrarAuto () que muestre el fabricante del vehículo.</li>
	<li>Hacer la clase <strong>CARRERA</strong> con 6 atributotos de clase <strong>AUTO</strong>, crear el método public void MostrarCarrera (), que muestre los datos de los autos de la carrera</li>
</ol>



<h3>*Ejercicio para los alumnos:*</h3>
hacer en la clase<strong>CARRERA </strong> el método “PorTiempo” que recibe como parámetro  “minutos”  representado por un entero y que la cantidad de minutos son las iteraciones que vamos a realizar (while o for), y en cada iteración le agregaremos una cantidad de kilómetros Random a cada auto participante de la  carrera. Por último el método mostrará por pantalla quien es el ganador con los kilómetros que recorrió.

Clase 4
-------

<h5>Objetivo: Poder definir y reutilizar constructores, llamada a constructores ya existentes.</h5>
-------------------------------------------------------------------------------------
<h6> <strong>G. </strong> Primeras sobrecargas de constructores.</h6>

<ol>

	<li>En la clase <strong>RUEDA</strong> creamos un nuevo constructor que reciba por parámetro un string “marca”.</li>
	<li>Utilizarlo en el MAIN, verificar que al abrir el paréntesis se ve las dos formar de usarlo.</li>
	<li>En la clase <strong>RUEDA</strong> creamos un nuevo constructor que reciba por parámetro un int “tamaño”.</li>
	<li>Utilizarlo en el MAIN, verificar que al abrir el paréntesis se ve las tres formar de usarlo.</li>
	<li>Agregarles los comentarios  a cada constructor con la tarea que realiza.</li>
</ol>

<pre><code>
 ///&lt;summary&gt;
 /// Constructor por defecto que inicializa el atributo marca con 'sin marca'		
 /// &lt;/summary&gt;
</pre></code>

<h6> <strong>H. </strong> Reutilización de código de constructores.</h6>

<ol>

	<li>En la clase <strong>RUEDA</strong> creamos un nuevo constructor que reciba por parámetro un string “marca” y un int tamaño.</li>
	<li>Verificar que tanto en la sobrecarga que recibe un string y en la que recibe dos parámetros, el atributo marca es inicializado, pero en la que solo recibe int, el atributo marca está en NULL.</li>
	<li>Utilizar el this para llamar desde el constructor que recibe un int al constructor por defecto para inicializar el atributo marca en “sin marca”.</li>
	<li>Crear un constructor que reciba un INT tamaño y un String marca, que no tenga código en su implementación y que utilice el THIS para llamar al constructor antes realizado.</li>
	<li>Agregarles los comentarios  a cada constructor con la tarea que realiza.</li>
</ol>

<h3>*Ejercicio para los alumnos:*</h3>
 hacer las sobrecargas de los constructores de <strong>AUTO</strong> para que todas pasen por el constructor por defecto para que aumente el contador de objetos.




<h5>Objetivo: Poder sobrecargar métodos.</h5>
-------------------------------------------------------------------------------------
<h6> <strong>I. </strong> Sobrecarga de métodos.</h6>

<ol>

	<li>Crear la clase<strong>TIEMPO</strong> y la clase <strong>KILOMETRO</strong>, cada una con un único atributo de tipo INT llamado “cantidad”.</li>
	<li>Cada uno  debe tener un único constructor que reciba por parámetro la cantidad.</li>
	<li>Ahora en la clase carrera crear el método “CorrerCarrera” con dos sobrecargas, una que reciba kilómetros y una que reciba tiempo.</li>
	<li>Agregamos a la clase auto el atributo privado “tiempoDemorado” donde acumularemos el tiempo demorado en recorrer los kilómetros.</li>
	<li>Agregamos al método “VolverACero”  las líneas para volver a cero  el “tiempoDemorado”.</li>
	<li>Creamos el método “AgregarTiempo” que agrega el int que recibe por parámetros al tiempo demorado.</li>
</ol>


<h3>*Ejercicio para los alumnos:*</h3>
Realizar la implementación  de cada sobrecarga del método “CorrerCarrera” e informar en cada caso quien es el ganador y el perdedor

		
