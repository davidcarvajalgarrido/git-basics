# 🔀 CHULETA: Flujo de Trabajo Colaborativo con Pull Requests

## 📋 Antes de empezar
```bash
git pull origin main  # Asegúrate de tener la última versión
```

---

## 1️⃣ PASO 1: Crear y cambiar a tu rama
```bash
git checkout -b nombre-rama-descriptiva
# o si tienes Git 2.23+:
git switch -c nombre-rama-descriptiva
```
💡 Usa nombres claros: `feature/login`, `fix/bug-123`, `docs/readme`

---

## 2️⃣ PASO 2: Trabajar en tu rama
```bash
git add archivo.txt
git commit -m "Mensaje descriptivo del cambio"
git commit -m "Otro commit si es necesario"
```

---

## 3️⃣ PASO 3: Subir tu rama al repositorio
```bash
git push -u origin nombre-rama-descriptiva
```

---

## 4️⃣ PASO 4: Solicitar Pull Request
1. Ve a GitHub/GitLab/etc.
2. Haz clic en "New Pull Request"
3. Selecciona tu rama → rama principal (`main` o `master`)
4. Escribe descripción clara de qué cambios hiciste
5. Crea el Pull Request

---

## 5️⃣ PASO 5A: Revisor AUTORIZA
✅ El revisor aprueba y hace merge

---

## 5️⃣ PASO 5B: Si hay CONFLICTOS
```bash
# El revisor resuelve en GitHub o localmente
# Luego intenta hacer merge
```

---

## 6️⃣ PASO 6: Limpiar después del merge
```bash
git switch main              # Vuelve a la rama principal
git pull origin main         # Descarga los cambios
git branch -d nombre-rama    # Borra tu rama localmente
git push origin --delete nombre-rama  # Borra en el servidor
```

---

## ⚡ RESUMEN RÁPIDO
```
CREAR    → git checkout -b rama
TRABAJAR → git add . && git commit -m "mensaje"
SUBIR    → git push origin rama
PR       → Crea en GitHub
MERGE    → Revisor autoriza
LIMPIAR  → git switch main && git pull && git branch -d rama
```

---

## 📝 TIPS
- Haz commits pequeños y frecuentes
- Escribe mensajes claros en los commits
- Una rama = una característica (no mezcles cambios)
- Actualiza tu rama si te dicen que tiene conflictos
- Antes de crear PR, verifica que tu código funciona
