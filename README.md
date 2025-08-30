# 📖 Guía de Commits Semánticos (Conventional Commits)

## 🔹 Estructura del Commit

<tipo>(opcional-alcance): <descripción corta>

- **tipo** → Categoría del cambio (feat, fix, chore, etc.)
- **alcance** (opcional) → Módulo, carpeta o parte del proyecto afectada
- **descripción** → Breve explicación en **imperativo**

---

## 🔸 Tipos de Commits

- **feat** → Nueva funcionalidad
  - `feat(auth): agregar login con JWT`
- **fix** → Corrección de errores
  - `fix(users): corregir bug al guardar usuario duplicado`
- **chore** → Tareas de mantenimiento (dependencias, configs, build)
  - `chore: actualizar dependencias npm`
- **docs** → Documentación
  - `docs: agregar guía de instalación en README`
- **style** → Cambios de formato (espacios, comas, indentación, sin lógica)
  - `style: aplicar prettier al proyecto`
- **refactor** → Cambio de código sin alterar funcionalidad
  - `refactor(api): simplificar controlador de usuarios`
- **test** → Agregar o modificar pruebas
  - `test(auth): agregar pruebas unitarias al login`
- **perf** → Mejoras de rendimiento
  - `perf(query): optimizar consulta de usuarios`
- **ci** → Cambios en la configuración de CI/CD
  - `ci: agregar workflow de GitHub Actions`

---

## 🔹 Buenas Prácticas

- ✅ Usa verbos en **imperativo** (ej: "agregar", "corregir").
- ✅ Máximo **50 caracteres** en la descripción corta.
- ✅ Si necesitas más detalle, agrega un **cuerpo**:
  ```bash
  git commit -m "fix(auth): corregir bug en validación de tokens" \
               -m "El bug se daba cuando el token expirado no era capturado correctamente. 
               Ahora se lanza un error 401."


✅ Commits pequeños y frecuentes son más fáciles de revisar.

❌ No usar mensajes vagos como: update, cambios varios, arreglo.

🔹 Ejemplos de Uso
git add .
git commit -m "feat(api): crear endpoint de productos"

git add user_model.py
git commit -m "fix(users): corregir validación de email duplicado"

git commit -m "docs: actualizar instrucciones de instalación"

🔹 Recursos

Conventional Commits

Commitlint
 → Para validar automáticamente tus mensajes de commit
