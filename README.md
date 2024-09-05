# Github actions

## Explicación de `hello-world.yml`:

on: push: Esta acción se ejecuta cuando haces un push en cualquier rama.
jobs: Define los trabajos que se ejecutarán en el flujo de trabajo.
steps: Son las acciones dentro de un trabajo.
uses: actions/checkout@v3: Este paso clona el código del repositorio en el entorno.
run: echo "Hola Mundo!": Ejecuta un comando echo.
if: success(): Verifica si la acción anterior fue exitosa antes de ejecutar el comando.

## Cron

Un cron es una expresión que se usa para programar la ejecución automática de tareas a intervalos específicos de tiempo. Se compone de cinco campos separados por espacios, que definen cuándo debe ejecutarse una tarea.

```md
---

│ │ │ │ │
│ │ │ │ └── Día de la semana (0 - 7) (domingo a sábado)
│ │ │ └──── Mes (1 - 12)
│ │ └────── Día del mes (1 - 31)
│ └──────── Hora (0 - 23)
└────────── Minuto (0 - 59)
```

## Ejemplo de cron

```md
0 0 \* \* _: Ejecuta una tarea todos los días a la medianoche.
0 0 _ _ 0: Ejecuta una tarea todos los domingos a la medianoche.
0 0 1 _ _: Ejecuta una tarea el primer día de cada mes a la medianoche.
0 0 1 1 _: Ejecuta una tarea el primer día de enero a la medianoche.
```

- Casos de uso comunes:
  - Actualización de dependencias.
  - Ejecución de pruebas.
  - Generación de informes.
  - Publicación de artefactos.
  - Backup de bases de datos.
  - Limpieza de archivos temporales.
  - Notificación de errores.

## Restriccion de 5 minutos

Las acciones de GitHub tienen una restricción de 5 minutos para completarse. Si una acción tarda más de 5 minutos en ejecutarse, se cancelará automáticamente.
