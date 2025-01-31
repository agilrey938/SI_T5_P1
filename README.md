# SI_T5_P1
1. import keyboard

   Esta línea importa la biblioteca keyboard, que permite interactuar con el teclado y escuchar las pulsaciones de teclas.
2. def pressedKeys(key):

   Aquí se define una función llamada pressedKeys que toma un argumento key. Esta función se ejecutará cada vez que se presione una tecla.
3. with open("keylog.txt", "a") as file:

   Dentro de la función, se abre (o crea si no existe) un archivo llamado keylog.txt en modo de adjuntar (a). Esto significa que cualquier nueva información se añadirá al final del archivo sin sobrescribir el contenido existente.
4. if key.name == "space":
    file.write(" ")
else:
    file.write(key.name)
    
   Se comprueba si la tecla presionada es la barra espaciadora (space). Si es así, se escribe un espacio en el archivo. Si no, se escribe el nombre de la tecla presionada.
5. keyboard.on_press(pressedKeys)

   Esta línea registra la función pressedKeys para que se llame cada vez que se presione una tecla.
6. keyboard.wait()

   Esta línea hace que el programa espere indefinidamente hasta que se presione una tecla. Mantiene el programa en ejecución para seguir registrando las teclas.
