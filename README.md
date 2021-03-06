python-testapi-boilerplate
==========================
Boilerplate para test a un API


¿Que incluye?
--------------
* source Code (directorio app)
* Dockerfile (directorio dev/Dockerfile)
* Makefile

Requerimientos
--------------
* Docker
* Cmake

Ayuda
-----
* make
* make help

Comandos
--------
```console
  build            Construir imagen para development
  ssh              Conectar al container por el protocolo ssh
  venv-create      Crea el entorno virtual (virtualenv)
  venv-install-lib Instala las librerias en el entorno virtual (virtualenv)
```

Activar virtualenv
------------------
```console
~/python-testapi-boilerplate$ make ssh
[root@594ea994b77f]/app# source ../venv/bin/activate
(venv) [root@594ea994b77f]/app#
```

Ejecutar main.py
----------------
```console
(venv) [root@594ea994b77f]/app# pytest -v
```

<img style="width:100%;" src="doc/pytest-run.png">

Json recibido
-------------
<img style="width:100%;" src="doc/json-response.png">

Estructura del project
======================

Directorio de la Applicacion
-----------------------------
```console
app
├── api
├── schemas
├── tests
├── lib
└── requirements.txt
```

Directorio Dockerfiles
----------------------
```console
docker
└── dev
    └── Dockerfile
```

Empezando
=========
Ejecutar los siguientes pasos:
* make build
* make venv-create
* make venv-install-lib

Agregar/Eliminar librerias
==========================
Esto se realiza en el archivo requirements.txt. Luego ejecutar el comando:

* make venv-install-lib
