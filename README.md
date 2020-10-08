# Bot para automatizar la BPPDAFME
Queremos un bot que automatize el proceso de recibir una solicitud de alumno y hacerla llegar a los profesores.

## Esquema de pasos
### Paso 1: de Gmail a WhatsApp
Una vez llegue el mail con la solicitud del alumno, queremos que este sea enviado por privado a una lista de contactos (los profesores).
Los correos que nos interesan son los que tienen como asunto "Demanda alumno" o "Demanda alumne".
![Lista de correos con diferentes asuntos](./img/README/borsadeprofesmail.png "Correo de la BPPDAFME")
El formato del mail es cómo se muestra en el ejemplo:
```xml
<dl>
    <dt>Su nombre</dt>
    <dd>Andreu</dd><span class="im">

    <dt>Su número de teléfono de contacto</dt>
    </span><dd>+34 666 666 666</dd><span class="im">

    <dt>¿Qué estudios está cursando?</dt>
    <dd>Universidad</dd>

    <dt>¿En qué curso está usted?</dt>
    <dd>Primero</dd>

    <dt>En qué zona(s) preferiría recibir las clases?</dt>
    </span><dd>Sarrià - Sant Gervasi</dd><span class="im">

    <dt>¿Aceptaría hacer clases a distancia?</dt>
    <dd>0</dd>

    <dt>Comentarios</dt>
    </span><dd>Quisiera clases de refuerzo de las asignaturas de cálculo y álgebra, que son las que más me cuestan de momento.</dd>
</dl>
```

### Paso 2: la respuesta de los profesores
Cuándo el bot pase el alumno a los profesores.
Ellos tendrán la opción de decir si lo quieren para ellos.
Puede ser con una simple comanda "/mine" o con una palabra clave.
Una vez el bot vea que un profesor diga que lo quiere para él, tiene que avisar a todos los otros que ese alumno ya no está disponible.

### Paso 3: el procedimiento del profesor que ha pedido el alumno
Cuando el bot haya avisado que el alumno ya no está disponible, tiene que dar los datos de contacto a el profesor para que él lo pueda abrir.
Además, se tendría que loggear que el profesor X ha recibido un alumno. 
Si puede ser en una spreadsheet, mejor. Nosotros tenemos este para ir guardando a quién le damos los alumnos.
![Google Spreadsheet con información sobre los profesores y sobre cuántos alumnos tienen](./img/README/excel-bppdafme.png "Google Spreadsheet con los alumnos")
Si no, que el bot tenga un grupo con los organizadores y nos vaya avisando "NOMBRE PROFESOR - ALUMNO".
Así tenemos constancia de quién nos tendrá que pagar su primera clase (es así como financiamos la campaña).

### Paso 4: gestión de problemas
Se tiene que también añadir una opción de respuesta al bot cuando un alumno no funciona.
Es más común de lo que parece.
Que entonces se loggée también que no ha funcionado para X profesor y que no se cuente cómo buena.

## Recursos y presupuesto
Lo ideal seria hacer el bot por WhatsApp, si no se puede, Telegram es una buena segunda opción.
Si se tiene que comprar un número extra para hacer el bot, se hace.
Se pueden usar terceros siempre y cuando tengan licencia comercial.
Cualquier duda de qué podemos conseguir, me abrís a por WhatsApp.

## Cuentas y contraseñas
Las cuentas y contraseñas de los correos, spreadsheets, etc. Lo habláis conmigo por WhatsApp también.
