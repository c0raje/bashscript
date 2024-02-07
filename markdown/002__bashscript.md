# BashScript (002)

## Arreglos (Arrays)

Puedes almacenar multiples valores en un solo nombre de variable.

```bash
#!/bin/bash

frutas=("Manzana" "Banana" "Uva")

echo "Las frutas en el arreglo son: ${frutas[0]}, ${frutas[1]} y ${frutas[2]}"
```

## Condicionales (if-elif-else)

Puedes manejar multiples condiciones.

```bash
#!/bin/bash

echo "Cual es tu edad?"

read edad

if[ $edad -lt 13 ]; then
  echo "Eres un nino."
elif [ $edad -ge 13 -a $edad -lt 20 ]; then
  echo "Eres un adolecente."
else
  echo "Eres un adulto"
fi
```

## Bucles (while)

Otra forma de repetir acciones.

```bash
#!/bin/bash

contador=1

echo "Contando hasta 5..."

while [ $contador -le 5 ]; do
  echo $contador
  ((contador++))
done

echo "Listo!"
```

## Argumentos de Script

Puedes pasar argumentos cuando ejecutas un script.

```bash
#!/bin/bash

echo "El primer argumento es: $1"
echo "El segundo argumento es: $2"
```

## Leer de un archivo

Puedes leer lineas de un archivo.

```bash
#!/bin/bash
archivo="mi_archivo.txt"

while IFS= read -r linea; do
  echo "Linea leida: $linea"
done < "$archivo"
```

## Ejecucion condicional (&& y ||)

Puedes ejecutar comandos en funcion del exito o fracaso de otros.

```bash
#!/bin/bash

mkdir carpeta_nueva && echo "Carpeta creada correctamente" || echo "Error al crear carpeta"
```

## Subprocesos y Comandos en SubShell

Puedes ejecutar comandos en un subshell usando parentesis `()`, y capturar su salida.

```bash
#!/bin/bash

resultado=$(echo "Hola, subshell!")
echo $resultado
```

## Funcionamiento de manipulacion de cadenas

Puedes manipular cadenas de texto facilmente.

```bash
#!/bin/bash

cadena="Hola mundo"

echo "Longitud de la cadena: ${#cadena}"
echo "Subcadena: ${cadena:0:4}" #Hola
```

## Expancion de rangos

Puedes generar secuencias numericas usando la expansion de rangos.

```bash
#!/bin/bash

echo {1..5}
```

## Redireccion de Entrada/Salida

Puedes redirigir la entrada y salida estandar.

```bash
#!/bin/bash

echo "Hola" > saludo.txt
cat < saludo.txt
```

## Operadores logicos

Puedes utilizar operadores logicos en tus expresiones condicionales.

```bash
edad=25

if [ $edad -gt 18 ] && [ $edad -lt 30 ]; then
  echo "Eres un adulto joven."
fi
```

## Comodines (Willdcards)

Puedes usar comodines para hacer coincidir patrones de nombres de archivos

```bash
#!/bin/bash

for archivo in *.txt; do
  echo "Procesando archivo: $archivo"
done
```

## Variables especiales

Bash tiene variables especiales que contienen informacion util.

```bash
#!/bin/bash

echo "Numero de argumentos: $#"
echo "Nombre del script: $0"
echo "PID del script: $$"
```

[003__bashscript](003__bashscript.md)