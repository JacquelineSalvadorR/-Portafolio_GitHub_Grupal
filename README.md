# -Portafolio_GitHub_Grupal
## ✅ Resumen del flujo GitFlow aplicado

Durante el desarrollo del portafolio grupal se aplicó correctamente el modelo de **trabajo colaborativo con GitFlow**, implementando las siguientes ramas y pasos:

---

### 🌿 Ramas utilizadas:

- **`main`**: rama principal, contiene el código en estado estable y final.
- **`develop`**: rama de integración donde se fusionan las funcionalidades en desarrollo.
- **`feature/readme`**: rama para trabajar de forma aislada en la documentación del proyecto.
- **`release/v1.0.0`**: rama usada para preparar la entrega final, realizar ajustes visuales y detalles en el `README.md`.
- **`hotfix/fix-readme`**: rama para simular una corrección urgente ya en producción, siguiendo el flujo correcto: merge a `main` y luego a `develop`.

---

### 💠 Flujo aplicado:

1. Se creó el repositorio base y se clonó localmente.
2. Se copiaron los archivos del portafolio ya desarrollado.
3. Se generó la rama `develop` a partir de `main`.
4. Se trabajó la documentación en `feature/readme`, luego se hizo `merge` a `develop`.
5. Se creó la rama `release/v1.0.0` para simular una entrega oficial.
6. Se finalizó la rama `release` haciendo `merge` hacia `main` y `develop`.
7. Finalmente, se creó la rama `hotfix/fix-readme` para simular una corrección urgente, aplicando el flujo completo.

---

### 📸 Evidencia de comandos utilizados:

```bash
git checkout -b develop
git checkout -b feature/readme
git add .
git commit -m "feat: agregar contenido al README"
git push origin feature/readme
git checkout develop
git merge feature/readme
git push origin develop

git checkout -b release/v1.0.0
git add .
git commit -m "docs: ajustes finales para la entrega"
git push origin release/v1.0.0
git checkout main
git merge release/v1.0.0
git push origin main
git checkout develop
git merge release/v1.0.0
git push origin develop

git checkout -b hotfix/fix-readme
git add .
git commit -m "fix: corregido texto en README"
git push origin hotfix/fix-readme
git checkout main
git merge hotfix/fix-readme
git push origin main
git checkout develop
git merge hotfix/fix-readme
git push origin develop
```

---

### ✨ Conclusión

> La implementación de GitFlow permitió organizar el desarrollo del portafolio, trabajar en equipo de forma estructurada, mantener una rama estable (`main`) y una rama en constante evolución (`develop`), además de gestionar funcionalidades (`feature`), entregas (`release`) y correcciones urgentes (`hotfix`) de manera clara.
