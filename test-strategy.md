# Pruebas Iniciales

## 1.
Abrir el index.html y F12 para identificar porque el boton no está tomando datos.

Encontrado Uncaught TypeError: guessSubmit.addeventListener is not a function

-- guessSubmit.addeventListener('click', checkGuess); --

Cambiada 

-- guessSubmit.addEventListener('click', checkGuess); --


## 2.

index.html:77 Uncaught TypeError: Cannot set properties of null (setting 'textContent')
    at HTMLInputElement.checkGuess (index.html:77:29)
Error en linea 
-- const lowOrHi = document.querySelector('lowOrHi'); --

Cambiada a

-- const lowOrHi = document.querySelector('.lowOrHi'); --




## 3.
Uncaught TypeError: Cannot set properties of null (setting 'textContent')
    at HTMLInputElement.checkGuess (index.html:79:29)



## 4. 
index.html:95 Uncaught TypeError: resetButton.addeventListener is not a function
    at setGameOver (index.html:95:16)
    at HTMLInputElement.checkGuess (index.html:72:7)


Linea con error -- resetButton.addEventListener('click', resetGame); --

Cambiada a -- resetButton.addEventListener('click', resetGame); --

## 5. Revision de codigo 
Revision para determinar si es a lo que se describe

#### Numeros mal generados
Linea solo genera numeros entre 0 y 1 (forma decimal) 
-- let randomNumber = Math.random() * 10; --

Linea cambiada para generar enteros de 1 a 100:

-- let randomNumber = Math.floor(Math.random() * 100) + 1; --



#### Cantidad de intentos permitidos incorrectos
Linea solo permite 5 intentos:
-- const ATTEMPS = 5; --

Cambiada para permitir 10 intentos:
-- const ATTEMPS = 10; --


#### Lineas erroneas en mensajes de determinar si gana o pierde.

#### Codigo de colores erroneo


#### No hace verificacion de que numero es entero

#### Cuando encuentra el numero correcto no muestra mensaje correcto de felicitacion lowOrHi se queda en blanco

