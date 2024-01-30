# BashScript (001)

## Salida de texto (echo)
Este es el comando basico para escribir texto en pantalla:
```bash
#!/bin/bash

# Este es un comentario

echo "Hola"
```

## Variables y entrada del usuario
Puedes almacenar informacion en variables y pedir al usuario que ingrese datos.
```bash
#!/bin/bash

echo "Hola, como te llamas?"

read nombre

echo "Hola, $nombre. Bienvenido!"
```

## Condicionales (if-else)
Puedes tomar decisiones en tu programa.
```bash
#!/bin/bash

echo "Cual es tu edad?"
read edad

if [$edad -ge 18]; then
  echo "Eres mayor de edad, puedes continuar."
else
  echo "Eres menor de edad, acceso denegado."
fi
```

## Bucles (for)
Puedes repetir acciones
```bash
#!/bin/bash

for i in {1..5}; do
  echo $i
done

echo "Listo!"
```

## Funciones
Puedes organizar tu codigo en funciones
```bash
#!/bin/bash

saludar() {
  echo "Hola, $1"
}

saludar "C0raje"
```

[002__bashscript](002__bashscript.md)