![Logo Mielma Developer](image/Logo_Mielma_Developer.png)
# [keydown: Elemento: Evento de pulsación de tecla](https://developer.mozilla.org/en-US/docs/Web/API/Element/keydown_event)

El keydown El evento se activa cuando se presiona una tecla..

A diferencia del obsoleto keypress evento, el keydown El evento se activa para todas las claves, independientemente de si producen un valor de carácter.

El keydown y keyup Los eventos proporcionan un código que indica qué tecla se presiona, mientras que keypress indica qué carácter se ingresó. Por ejemplo, una "a" minúscula será reportada como 65 por keydown y keyup, pero como 97 por keypress. Todos los eventos informan que una "A" mayúscula es 65.

El objetivo del evento de un evento clave es el elemento actualmente enfocado que está procesando la actividad del teclado. Esto incluye:  `<input>`, `<textarea>`, cualquier cosa que sea contentEditable, y cualquier otra cosa con la que se pueda interactuar con el teclado, como `<a>`, `<button>`, y `<summary>`. Si no hay ningún elemento adecuado enfocado, el objetivo del evento será el `<body>` o la raíz. Si no se detecta, el evento hasta el hasta llegar Document.

keydown / keyup

`addEventListener().`
```js
addEventListener("keydown", (event) => {});

onkeydown = (event) => {};
```
> [!CAUTION]
> Esto ignora la distribución del teclado del usuario, de modo que si el usuario presiona la tecla en la posición "Y" en una distribución de teclado QWERTY (cerca del centro de la fila encima de la fila de inicio), esto siempre devolverá "KeyY", incluso si el El usuario tiene un teclado QWERTZ (lo que significaría que el usuario espera una "Z" y todas las demás propiedades indicarían una "Z") o una distribución de teclado Dvorak (donde el usuario esperaría una "F"). Si desea mostrar las pulsaciones de teclas correctas al usuario, puede utilizar Keyboard.getLayoutMap().


**Sigue leyendo en el enlace**
