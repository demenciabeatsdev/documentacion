
# Guía para Iniciar un Proyecto en Git desde Cero hasta Mergear en Main

## 1. Instalar Git
Si no tienes Git instalado, puedes descargarlo e instalarlo desde [aquí](https://git-scm.com/downloads).

## 2. Configurar Git (solo si es la primera vez)
Abre una terminal y configura tu nombre de usuario y correo electrónico:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu_email@example.com"
```

## 3. Iniciar un nuevo repositorio
Navega al directorio donde quieres crear el proyecto o crea un nuevo directorio:

```bash
mkdir mi_proyecto
cd mi_proyecto
```

Inicializa un nuevo repositorio de Git:

```bash
git init
```

## 4. Agregar archivos al repositorio
Crea los archivos que necesitas, por ejemplo, un archivo `README.md`:

```bash
echo "# Mi Proyecto" >> README.md
```

Añade los archivos al área de preparación:

```bash
git add .
```

## 5. Hacer el primer commit
Confirma los archivos en el repositorio con un mensaje descriptivo:

```bash
git commit -m "Primer commit: Inicialización del proyecto"
```

## 6. Conectar a un repositorio remoto (por ejemplo, GitHub)
Si ya tienes un repositorio remoto creado (por ejemplo, en GitHub), conéctalo:

```bash
git remote add origin https://github.com/usuario/mi_proyecto.git
```

**Nota:** Reemplaza la URL con la dirección de tu repositorio remoto.

## 7. Subir los cambios a la rama `main`
Sube los cambios al repositorio remoto:

```bash
git push -u origin main
```

## 8. (Opcional) Crear una rama para trabajar en una nueva funcionalidad
Crea una nueva rama para trabajar en una funcionalidad específica o para una tarea:

```bash
git checkout -b nombre_de_la_rama
```

**Ejemplo:**

```bash
git checkout -b nueva_funcionalidad
```

## 9. Trabajar en la nueva rama
Realiza los cambios necesarios en los archivos y confirma esos cambios en la nueva rama:

```bash
git add .
git commit -m "Descripción de los cambios realizados"
```

Si es necesario subir la rama al repositorio remoto, usa:

```bash
git push -u origin nombre_de_la_rama
```

## 10. Fusionar la rama con `main`
Una vez que hayas terminado de trabajar en la rama, cambia de nuevo a la rama `main`:

```bash
git checkout main
```

Fusiona los cambios de la rama en `main`:

```bash
git merge nombre_de_la_rama
```

## 11. Resolver conflictos (si los hay)
Si Git detecta conflictos, tendrás que resolverlos manualmente. Edita los archivos afectados, luego añade los archivos resueltos y confirma los cambios:

```bash
git add .
git commit -m "Resolviendo conflictos y fusionando rama"
```

## 12. Subir la rama `main` actualizada al repositorio remoto
Sube la rama `main` actualizada al repositorio remoto:

```bash
git push origin main
```

## 13. (Opcional) Eliminar la rama local
Si ya no necesitas la rama localmente, puedes eliminarla:

```bash
git branch -d nombre_de_la_rama
```

**Ejemplo:**

```bash
git branch -d nueva_funcionalidad
```

## 14. (Opcional) Eliminar la rama remota
Si ya no necesitas la rama en el repositorio remoto:

```bash
git push origin --delete nombre_de_la_rama
```

**Ejemplo:**

```bash
git push origin --delete nueva_funcionalidad
```

## Resumen
- Inicializa el repositorio (`git init`).
- Crea archivos, añade y confirma cambios (`git add` y `git commit`).
- Conecta y sube al repositorio remoto (`git remote add` y `git push`).
- Crea ramas para nuevas funcionalidades (`git checkout -b`).
- Trabaja en las ramas y luego fusiona con `main` (`git merge`).
- Maneja conflictos si es necesario y sube cambios (`git push`).

Con estos pasos, tendrás un flujo de trabajo básico en Git que te permitirá trabajar en proyectos, gestionar ramas y fusionar cambios.
