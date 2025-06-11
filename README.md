# 🧠 Comandos Básicos de Git

Este documento contiene una lista de comandos esenciales para trabajar con Git, el sistema de control de versiones más usado por desarrolladores.

---

## 🔧 Configuración inicial

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
```

---

## 📁 Crear o clonar un repositorio

```bash
git init                 # Inicializa un nuevo repositorio Git
git clone <url>          # Clona un repositorio existente
```

---

## 📄 Estado y manejo de cambios

```bash
git status               # Muestra el estado del repositorio
git add <archivo>        # Agrega archivo(s) al área de staging
git add .                # Agrega todos los archivos modificados
git commit -m "Mensaje"  # Crea un commit con los cambios
```

---

## 📜 Ver historial de cambios

```bash
git log                  # Muestra el historial de commits
git log --oneline        # Historial simplificado
```

---

## 🌿 Trabajar con ramas

```bash
git branch               # Lista las ramas
git branch <nombre>      # Crea una nueva rama
git checkout <rama>      # Cambia de rama
git checkout -b <rama>   # Crea y cambia a una nueva rama
```

---

## 🔄 Actualizar y subir cambios

```bash
git pull                 # Descarga y fusiona cambios del repositorio remoto
git push                 # Envía tus commits al repositorio remoto
git push -u origin <rama># Envía una rama nueva al remoto y establece seguimiento
```

---

## 🔀 Fusionar ramas

```bash
git merge <rama>         # Fusiona una rama en la actual
```

---

## ❌ Eliminar archivos o deshacer cambios

```bash
git rm <archivo>         # Elimina un archivo y lo marca para el commit
git restore <archivo>    # Revierte cambios no confirmados
git reset HEAD <archivo> # Quita el archivo del área de staging
```

---


## 🔃 Git Flow (Flujo de trabajo avanzado)

Git Flow es una estrategia de ramificación que ayuda a organizar el desarrollo de software. Para usarlo necesitas instalar la herramienta:

```bash
git flow init            # Inicializa Git Flow en tu repositorio
```

### Ramas principales:
- `main`: Contiene el código en producción
- `develop`: Contiene el código en desarrollo

### Ramas de soporte:
- `feature/*`: Para nuevas funcionalidades
- `release/*`: Preparación para una nueva versión
- `hotfix/*`: Correcciones rápidas en producción

### Comandos útiles:

```bash
git flow feature start <nombre>     # Inicia una nueva feature
git flow feature finish <nombre>    # Finaliza y fusiona la feature a develop

git flow release start <versión>    # Inicia una nueva release
git flow release finish <versión>   # Finaliza la release, fusiona a main y crea tag

git flow hotfix start <nombre>      # Inicia un hotfix desde main
git flow hotfix finish <nombre>     # Finaliza el hotfix, fusiona a main y develop
```

> 💡 Git Flow es ideal para equipos que liberan versiones con frecuencia y tienen entornos de desarrollo y producción separados.

---
