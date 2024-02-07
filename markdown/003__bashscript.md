# BashScript (003)

## Case statement

El caso (`case`) es util para manejar multiples condiciones de manera mas clara.

```bash
#!/bin/bash

fruta="Manzana"

case $fruta in
  "Manzana")
    echo "Es una manzana."
    ;;
  "Banana" | "Platano")
    echo "Es una banana o platano."
    ;;
  *)
    echo "No se que fruta es."
    ;;
esac
```

## Seleccion de rutas (path selection)

Puedes usar diferentes rutas basadas en condiciones.

```bash
#!/bin/bash

sistema="Linux"

ruta_archivos="/home/usuario/archivos"
ruta_temp="/temp"

ruta_seleccionada=""

if [ $sistema == "Linux" ]; then
  ruta_seleccionada=$ruta_archivos
else
  ruta_seleccionada=$ruta_temp
fi

echo "La ruta seleccionada es: $ruta_seleccionada"
```

## Variables de entorno personalizadas

Puedes crear y utilizar tus propias variables de entorno.

```bash
export MI_VARIABLE="Hola desde mi script"

echo $MI_VARIABLE
```

## Evaluacion de expresiones aritmeticas

Puedes realizar calculos aritmeticos dentro de scripts.

```bash
#!/bin/bash

numero1=5
numero2=3

resultado=$((numero1 + numero2))

echo "La suma es: $resultado"
```

## Manipulacion de fechas y tiempos

Puedes trabar con fechas y tiempos.

```bash
#!/bin/bash

fecha_actual=$(date +"%Y-%m-%d")
hora_actual=$(date +"%H:%M:%S")

echo "Fecha: $fecha_actual"
echo "Hora actual: $hora_actual"
```

## Interrupciones y senales

Puedes manejar interrupciones y senales.

```bash
#!/bin/bash

trap 'echo "Script interrumpido"; exit' INT TERM

echo "Este escript sigue ejecutandose. Presiona Ctrl + C para detenerlo."

while true; do
  sleep 1
done
```

## Ejecucion de comandos en paralelo

Puedes ejecutar comandos en paralelo utilizando `&`.

```bash
#!/bin/bash

echo "Iniciando tarea 1..."
comando_tarea1 &

echo "Iniciando tarea 2..."
comando_tarea2 &

echo "Esperando a que las tareas finalicen..."
wait

echo "Todas las tareas han terminado."
```

[004__bashscript](004__bashscript.md)