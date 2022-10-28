# Código Inicial - Trivia App 

## Descripción del Proyecto

En este módulo los estudiantes trabajarán en grupos para construir un proyecto usando HTML, CSS y React. El objetivo principal es desarrollar el front-end para una aplicación tipo Kahoot que permita mostrar una pregunta con sus posibles respuestas, que un usuario pueda seleccionar una respuesta y que el sistema determine si respondieron o no correctamente. 


## Día 1: Componentes de React y props

### Meta 1: Mostrar en pantalla una pregunta del archivo sample_data.json.

- [ ] En el archivo App.jsx crear un componente llamado Question.
- [ ] Mostrar una instancia del componente `<Question />` dentro de `<App />`.
- [ ] Agregar propiedades (props) a `<Question />` con el texto "Aquí va la pregunta".
- [ ] En `<App />`, agregar una variable que asigne el número de pregunta actual a 0.
- [ ] Reemplazar el texto asignado "Aquí va la pregunta"con el campo `question.text` que se encuentra en data para la primera pregunta.
  - [ ] PISTA: Usa la variable creada para obtener el número de la pregunta.
- [ ] BONUS: Agrega estilos a la aplicación.

>![Meta para el día 1](https://i.imgur.com/eTZAXGk.png)

### Meta 2: Mostrar el botón de "Siguiente Pregunta" en pantalla.

- [ ] En el archivo App.jsx crear un componente llamado NextQuestion.
- [ ] Escribe el JSX para que le muestre al usuario un botón que le permita avanzar a la siguiente pregunta. Por ahora no tendrá ninguna funcionalidad.
- [ ] Mostrar una instancia del componente `<NextQuestion />` dentro de `<App />`.

>![Meta día 1.5](https://i.imgur.com/o4MzPjL.png)


## Día 2: Componentes anidados y estados. 

### Meta 1: Mostrar las opciones de respuesta del archivo sample_data.json en pantalla.

- [ ] En el archivo App.jsx, crear un componente llamado Answer.
- [ ] Mostrar una instancia del componente `<Answer />` dentro de `<Question />`.
- [ ] Agregar propiedades al componente `<Answer />` con el texto "Aquí va la respuesta".
  - [ ] Pasar las propiedades para las opciones de respuesta al componente `<Question />`.
  - [ ] Usar las propiedades para mostrar los componentes Answer dentro de `<Question />` y presentar las opciones de respuesta.
- [ ] Refactorizar para usar map to map sobre todas las opciones de respuesta.

>![Meta para el día 2](https://i.imgur.com/VpA8eRc.png)

### Meta 2: Mostrar un botón en pantalla que revele la opción correcta una vez clickeado.

- [ ] Usando `useState` en `<App />`, crear una varieable de estados booleana llamada `answerDisplayed` para saber si se debe o no mostrar la respuesta correcta.
- [ ] Agregar un botón al componente App que actualizará el estado para mostrar la respuesta correcta cuando se clickea.
- [ ] Crear una función onClick que asigna el estado para mostrar la opción correcta cuando el botón es clickeado. 
  - [ ] PISTA: Obtén la respuesta correcta usando el archivo `sample_data.json`.

>![Meta día 2.5 - sin respuesta](https://i.imgur.com/JI6GroE.png)
>![Meta día 2.5 - con respuesta](https://i.imgur.com/rufYX84.png)


## Día 3: Manejadores de Eventos

### Meta 1: Agrega funcionalidad al botón de "Siguiente Pregunta" para que muestre la próxima pregunta una vez clickeado.

- [ ] Agregar estado a `<App />` usando el hook de React `useState` para mantener registro del número de pregunta actual.
  - [ ] Reemplaza la variable del número de pregunta actual asignada el Día 1.
- [ ] Crea una función que actualice el estado al siguiente número de pregunta.
- [ ] Crea una propiedad en `<NextQuestion />` para asignar el prop al botón para llamar la función cuando el botón es clickeado. 
- [ ] Revisa que cada parte de las preguntas y respuestas se actualicen para reflejar la pregunta actual.
- [ ] Reinicia el estado de `answerDisplayed` cuando el botón de Siguiente Pregunta es clickeado para que la respuesta correcta no se muestre. 
- [ ] BONUS: Agrega [conditional rendering](https://reactjs.org/docs/conditional-rendering.html) para ocultar el componente `<NextQuestion />` cuando ya no queden próximas preguntas.

>![Meta día 3](https://i.imgur.com/fetraPF.png)
>![Meta día 3 con bonus](https://i.imgur.com/GruM8g2.png)

### Meta 2: Agrega funcionalidad para que, al momento de seleccionar una opción, la respuesta correcta se muestre en pantalla.

- [ ] Usando `useState` en `<App />`, crea una variable de estado para mantener registro de la opción que escoge el usuario.
  - [ ] Dentro de la función de map para los componentes Answer, agrega un manejador de eventos que actualice el estado para asignarle la opción que el usuario escoge.
  - [ ] PISTA: Usar propiedades para pasarle el estado de `<App />`.
  - [ ] PISTA: No olvides pasar el `onClick` también.
- [ ] Dentro de `<App />` (debajo del state y arriba del return), escribe un condicional que verifique si la respuesta seleccionada es la correcta.
  - [ ] Muestra el texto en pantalla indicándole al usuario si su respuesta es correcta.
  - [ ] Muestra un texto en pantalla indicándole la opción correcta al usuario en caso de haber seleccionado una diferente.
  - [ ] PISTA: Para hacer esto, deberías crear una variable y asignarla dentro de la sentencia de retorno (return statement).
  - [ ] BONUS: Usa [plantillas literales](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals) en vez de la concatenación de strings.

### Meta 3: Organiza tu app en diversos archivos e importa/exporta los componentes.

- [ ] Crea un nuevo archivo `.js` dentro de la carpeta componenta para cada uno de los componentes.
- [ ] Mueve  el código de cada uno de los componentes a sus archivos correspondientes.
- [ ] Agrega la sentencia que exporta cada uno de los componentes. 
- [ ] Importa todos los componentes en los archivos correctos.

>![Día 3.5 correcto](https://i.imgur.com/HC7M6LH.png)
>![Día 3.5 incorrecto](https://i.imgur.com/DWQu3bb.png)
