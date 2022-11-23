# WORKFLOW BASICO PARA AYUDARNOS A ENTENDER ACTIONS

name: CI # Como se llamará

# Controla cuando se ejecutará el workflow
on:
  # Dispara el workflow en eventos push o pull request pero solo para la branch "main" 
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

  # Te habilita a correr este workflow manualmente desde el tabulador Actions 
  workflow_dispatch:

# Un workflow está constituido de uno o más jobs que pueden correr secuencial o paralelamente
jobs:
  # Este workflow contiene un unico job llamado "build"
  build:
    # Sobre que SO va a correr el job
    runs-on: ubuntu-latest

    # Los Steps representan una secuencia de tareas que serán ejecutadas como parte del job.
    # Nos van a ayudar a configurar cada parte que va a suceder
    steps:
      # El primer step que siempre debe estar presente es la parte de Checkout. Nos permite llevar 
      # la configuracion de nuestro repositorio a este recurso en la nube.
      # A partir de ahi se podrán ejecutar el resto de scripts
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v3

      # Ejecuta el comando usando el bash shell
      - name: Run a one-line script
        run: echo Hello, world!

      # Ejecuta el comando usando el bash shell
      - name: Run a multi-line script
        run: |
          echo Add other actions to build,
          echo test, and deploy your project.