# Curso de Git y Terminal

## Clase 1: Comandos básicos de terminal

```bash
pwd             # Muestra la ruta actual
cd              # Cambia de directorio
cd /            # Va a la raíz del disco
cd ~            # Va al directorio del usuario
ls              # Lista archivos en el directorio
ls -al          # Lista todos los archivos, incluso ocultos
ls -l           # Lista con detalles
ls -a           # Lista ocultos sin detalles
clear           # Limpia la consola (Ctrl + L)
cd ..           # Subir un nivel
cd U + tab      # Autocompletado de ruta
cd /D           # Cambiar de disco en Windows
```

```bash
df -h           # Ver espacios de disco (Ubuntu)
cd /mnt/d       # Acceder a disco desde WSL
```

### Crear carpetas:

```bash
cd /mnt/c
cd ~
mkdir Tecnicatura
cd tecnicatura
mkdir Python Java JavaScript
```

## Clase 2: Archivos y comandos

```bash
touch vacio.txt             # Crear archivo vacío
cat vacio.txt               # Mostrar contenido
history                     # Ver historial de comandos
!72                         # Ejecutar comando #72
rm vacio.txt                # Eliminar archivo
rm --help                   # Ayuda de rm
```

## Crear repositorio Git y primer commit

```bash
cd tecnicatura
mkdir class-git && cd class-git
git init                    # Iniciar repositorio Git
code .                      # Abrir en VS Code
ctrl + n / ctrl + s         # Crear y guardar historia.txt
git status                  # Ver estado
```

```bash
git add historia.txt
# Quitar del staging
git rm --cached historia.txt
```

### Configuración inicial

```bash
git config --global user.name "Ariel Betancud"
git config --global user.email "betancudariel@gmail.com"
git config --list
```

### Primeros commits

```bash
git add .
git commit -m "Mensaje importante del commit"
code .  # Modificamos el archivo
```

## Clase 3: Manejo de archivos

```bash
rm historia.txt
rm --recursive -R Git
mkdir class-git
cd class-git
touch README.md
code .  # Crear README.md
```

### Commits:

```bash
git add .
git commit -m "Cargamos el README dentro del directorio class-git"
```

## Clase 4: Edición con vim y commits

```bash
touch historia.txt
code .
# Editamos y guardamos
```

```bash
git commit               # Abre vim
ESC -> :wq! (guardar y salir)
```

## Clase 6: Reset y ramas

```bash
git commit -a           # Commit con edición en vim
ESC + i (escribir)
ESC + :wq! (guardar y salir)
```

```bash
git reset --soft <hash>
git reset --hard <hash>
git diff
```

```bash
git checkout <hash>     # Ver versión antigua
git checkout master     # Volver a master
```

### Ramas

```bash
git branch cambios
git checkout master
git branch second tuNombre hotfix
git branch -d cambios
```

## Clase 7: Git reset vs. rm

```bash
git reset --soft        # Borra historial pero guarda en staging
git reset --hard        # Borra todo
```

```bash
git rm --cached         # Elimina de staging, mantiene en disco
git rm --force          # Elimina del disco y de Git
```

## Clase 8: Trabajo con servidor remoto

```bash
git clone <url>
git push
git fetch
git merge
git pull
```

### Logs avanzados

```bash
git log --oneline
log --stat
log --decorate
log --graph --oneline --all
```

## Clase 9: Más sobre ramas

```bash
git branch nueva_rama
git checkout nueva_rama
git checkout -b nueva_rama
```

```bash
git reset <hash>
git checkout <hash>
```

## Clase 10: Merge de ramas

```bash
git checkout master
git merge segunda
```

```bash
git commit -am "Mensaje"
```

## Clase 11: SSH en Git

```bash
git config --global user.email "alumnos@mail.com"
ssh-keygen -t rsa -b 4096 -C "alumnos@mail.com"
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_nombre
```

---

> **Nota:** Este README resume las clases de Git y línea de comandos. Cada bloque de comandos debe practicarse en una terminal para afianzar conocimientos. Asegúrate de tener Git y una terminal correctamente configurada (Git Bash en Windows o Terminal en Linux/macOS).

---

*Repositorio educativo para el curso de Tecnicatura en programación. Realizado por Ariel Betancud y colaboradores.*

