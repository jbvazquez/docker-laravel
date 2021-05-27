# docker-laravel

## Informacion General
Pasos seguidos en el siguiente video https://youtu.be/q7v2Qqf2Vmk
- Como Instalar Laravel en Windows  [Getting Started On Windows](https://laravel.com/docs/8.x/installation#getting-started-on-windows)
- Como abrir WSL en VSCode [Remote development in WSL](https://code.visualstudio.com/docs/remote/wsl-tutorial)

**Nota:** Después de instalar y habilitar WSL2, debe asegurarse de que Docker Desktop esté configurado para usar el backend de WSL2.

### 1. Instalar Debian WSL
Acceder a la Microsoft Store y descargar la imagen de [Debian](https://www.microsoft.com/es-mx/p/debian/9msvkqc78pk6#activetab=pivot:overviewtab) para el subsistema de Windows para Linux (WSL)
### 2. Verificar el modo de WSL 
`wsl.exe -l -v`

Ejemplo de salida
```
C:\Users\user>wsl.exe -l -v
  NAME                   STATE           VERSION
* Debian                 Running         2
  docker-desktop-data    Running         2
  docker-desktop         Running         2
```

Documentacion completa en [Docker Desktop WSL 2 backend](https://docs.docker.com/docker-for-windows/wsl/)


### 3. Crear un nuevo proyecto de Laravel
`curl -s https://laravel.build/example-prod | bash`


### 4. Build Docker
`docker-compose -f "docker-compose.yml" up -d --build`

### 5. Acceder al sitio
    http://127.0.0.1:8200/