# Reporte de Proyecto: Portfolio Profesional con Git

Este documento detalla la secuencia de comandos utilizada para la gestión del repositorio del Portfolio, cubriendo desde la inicialización hasta la migración final a los estándares actuales.

---

## 🏗️ Ejercicio 1: Cimientos e Infraestructura
* [cite_start]**Identidad y Alias:** - `git config --global user.name "Tu Nombre"` [cite: 31]
  - [cite_start]`git config --global user.email "tu@email.com"` [cite: 31]
  - [cite_start]`git config --global alias.s "status -s"` [cite: 32]
* **Inicialización:** `mkdir portfolio-git`, `cd portfolio-git` y `git init`.
* [cite_start]**Ignorar archivos:** Creación de `.gitignore` con `.vscode/` y `.idea/`. [cite: 33]
* [cite_start]**Primer Commit:** `git add .` y `git commit -m "Initial commit"`. [cite: 34]
* [cite_start]**GitHub:** `git remote add origin [URL]` y `git push -u origin master`. [cite: 35]

---

## 🌿 Ejercicio 2: Desarrollo Paralelo
* [cite_start]**Nueva Rama:** `git checkout -b feature/proyectos`. [cite: 37]
* **Snapshots Atómicos:**
  - [cite_start]Estructura: `git add index.html` y `git commit -m "feat: estructura de tarjetas"`. [cite: 40]
  - [cite_start]Estilos: `git add style.css` y `git commit -m "style: diseño de tarjetas"`. [cite: 40]
* [cite_start]**Verificación:** `git log --oneline --decorate`. [cite: 41]

---

## 🚑 Ejercicio 3: Interrupción por Fallo Crítico
* [cite_start]**Cambio de Contexto:** `git checkout master`. [cite: 44]
* [cite_start]**Rama Hotfix:** `git checkout -b hotfix/nav-color`. [cite: 44]
* **Fusión Fast-Forward:** ```bash
  git checkout master
  git merge hotfix/nav-color
  ``` [cite: 46]
* **Limpieza:** `git branch -d hotfix/nav-color`.

---

## ⚔️ Ejercicio 4: Sincronización y Conflictos
* [cite_start]**Actualización:** `git merge master` dentro de la rama de funcionalidad. [cite: 47]
* [cite_start]**Resolución de Conflicto:** Edición manual del "Hero" en `index.html` para unir las descripciones. [cite: 53]
* [cite_start]**Finalización:** `git add index.html` y `git commit -m "merge: resolución de conflicto en Hero"`. [cite: 55]

---

## 📦 Ejercicio 5: Gestión de Trabajo Pendiente (Stash)
* [cite_start]**Uso de Stash:** `git stash` para pausar el footer.
* [cite_start]**Corrección en Master:** `git checkout master`, fix del logo y `git commit`. 
* [cite_start]**Retorno:** `git checkout feature/footer` y `git stash pop`. 

---

## 🔍 Ejercicio 6: Auditoría del Historial
* [cite_start]**Gráfico Total:** `git log --graph --all --oneline --decorate`. 
* **Inspección de Cambios:** `git diff` antes de confirmar márgenes.
* **Filtrado Temporal:** `git log --since="30 minutes ago"`.
* [cite_start]**Estadísticas:** `git log --stat`. 

---

## 🏷️ Ejercicio 7: Versionado de Software
* [cite_start]**Release 1.0:** `git tag -a v1.0 -m "Primera entrega del Portfolio"`. 
* [cite_start]**Release 1.1:** `git tag v1.1` (tag ligero tras cambio de fuente). 
* [cite_start]**Distribución:** `git push origin --tags`. 

---

## 🔄 Ejercicio 8: Migración y Entrega Final
* [cite_start]**Renombrado a Main:** `git branch -m master main`. 
* [cite_start]**Actualización Remota:** `git push -u origin main` y `git push origin --delete master`.
* [cite_start]**Alias Personalizado:** `git config --global alias.borrar "branch -D"`. 

##  Evidencia gráfica
![alt text](img/Ej2_2_4.png)
![alt text](img/Ej2_2_5.png)
![alt text](img/Ej2_3_4.png)
![alt text](img/Ej2_4_4.png)
![alt text](img/Ej2_5_1.png) 
![alt text](img/Ej2_5_4.png)
![alt text](img/Ej2_5_5.png) 
![alt text](img/Ej2_6_2.png) 
![alt text](img/Ej2_6_5.png)
![alt text](img/Ej3_1_1.png)
![alt text](img/Ej3_2_3.png) 
![alt text](img/Ej3_2_5.png)