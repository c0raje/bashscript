# BashScript (004)

## Funciones anonimas (funciones lambda)

Puedes crear funciones anonimas utilizando la palabra clave `function`.

```bash
#!/bin/bash

mi_funcion () {
  echo "Hola desde la funcion."
}

# Llamada a la funcion
mi_funcion
```

## Manejo de errores con `trap`

Puedes utilizar `trap` para manejar errores y realizar acciones especificas al recibir senales.

```bash
#!/bin/bash

trap 'echo "Error detectado. Saliendo..."; exit 1' ERR

comando_que_puede_fallar
```

## Select loop

Puedes crear menus interactivos utilizando el bucle `select`.

```bash
#!/bib/bash

opciones=("Opcion 1" "Opcion 2" "Opcion 3" "Salir")

select opcion in "$opciones[@]"; do
  case $opcion in
    "Opcion 1")
      echo "Seleccionaste la Opcion 1";;
    "Opcion 2")
      echo "Seleccionaste la Opcion 2";;
    "Opcion 3")
      echo "Seleccionaste la Opcion 3";;
    "Salir")
      echo "Saliendo del menu."
      break;;
    *)
      echo "Opcion no valida."
  esac
done
```

## Uso de `awk` y `sed`

Puedes usar herramientas como `awk` y `sed` para procesar texto de manera mas avanzada dentro de tus scripts.

```bash
#!/bin/bash

echo "1: Juan 25
2: Maria 30
3: Pedro 22" | awk '{print $2}' | sed 's/:/ - Edad:/'
```

## Funciones recursivas

Bash tambien permite funciones recursivas.

```bash
#!/bin/bash

factorial() {
  if [ $1 -eq 0 ]; then
    echo 1
  else
    echo $(( $1 * $(factorial $(( $1 - 1 ))) ))
  fi
}

resultado=$(factorial 5)
echo "El factorial de 5 es: $resultado"
```

[005__bashscript](005__bashscript.md)