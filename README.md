# 🪘 Caporales Centralistas · Registro de Grupos
**Inauguración de Trajes · 13·06·2026**
Desarrollado e implementado por [Zynexall](https://zynexall.com)

---

## 🔥 Configuración Firebase — sincronización para hasta 15 personas

### Paso 1 — Crear proyecto Firebase
1. Ve a [console.firebase.google.com](https://console.firebase.google.com)
2. **"Agregar proyecto"** → nombre: `caporales-centralistas` → Crear
3. Desactiva Google Analytics → **Crear proyecto**

### Paso 2 — Realtime Database
1. Menú izquierdo → **Realtime Database** → **Crear base de datos**
2. **"Iniciar en modo de prueba"** → Habilitar
3. Copia tu URL: `https://TU-PROYECTO-default-rtdb.firebaseio.com`

### Paso 3 — Reglas de seguridad (importante para 15 usuarios)
En Realtime Database → pestaña **Reglas**, pega esto:
```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```
Clic en **Publicar**.

### Paso 4 — Actualizar index.html
Busca en el `<script>`:
```js
const FB_URL = 'https://caporales-centralistas-default-rtdb.firebaseio.com';
```
Reemplaza con tu URL real.

---

## 👤 Roles

| Rol | Acceso | Función |
|-----|--------|---------|
| **Registra** | Libre | Ingresa nuevos grupos |
| **Gestiona** | Libre | Ordena cola y marca participación |
| **Administrador** | Contraseña | Borrar datos, ver usuarios online |

**Contraseña admin:** `Zynexall2026`

---

## 📊 Capacidad
- Hasta **15 usuarios simultáneos** (sincronización cada 1.5 segundos)
- Panel admin muestra cuántas personas están conectadas en tiempo real
- Log de actividad con últimas 50 acciones

---
*Implementado por [Zynexall](https://zynexall.com)*
