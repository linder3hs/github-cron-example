# Github actions

Explicación de `hello-world.yml`:
on: push: Esta acción se ejecuta cuando haces un push en cualquier rama.
jobs: Define los trabajos que se ejecutarán en el flujo de trabajo.
steps: Son las acciones dentro de un trabajo.
uses: actions/checkout@v3: Este paso clona el código del repositorio en el entorno.
run: echo "Hola Mundo!": Ejecuta un comando echo.
if: success(): Verifica si la acción anterior fue exitosa antes de ejecutar el comando.
