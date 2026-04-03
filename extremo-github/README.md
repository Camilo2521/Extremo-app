# Retorno del Extremo — Cómo obtener el APK

## Pasos (15 minutos, todo gratis)

---

### PASO 1 — Crear cuenta en GitHub
1. Ve a https://github.com
2. Clic en **Sign up** — registra una cuenta gratis
3. Confirma tu email

---

### PASO 2 — Crear repositorio
1. Una vez dentro de GitHub, clic en el botón verde **"New"** (esquina superior izquierda)
2. Nombre del repositorio: `extremo-app`
3. Selecciona **Public**
4. Clic en **"Create repository"**

---

### PASO 3 — Subir los archivos
1. En la página de tu nuevo repositorio, clic en **"uploading an existing file"**
2. Descomprime el ZIP que descargaste
3. Arrastra **TODA** la carpeta descomprimida al área de GitHub
4. Clic en **"Commit changes"** (botón verde abajo)

---

### PASO 4 — Esperar la compilación (5-10 minutos)
1. Ve a la pestaña **"Actions"** de tu repositorio
2. Verás un workflow corriendo llamado **"Build Android APK"**
3. Espera a que el círculo amarillo se vuelva verde ✓
4. Si se pone rojo, abre el workflow y lee el error (escríbeme y lo resuelvo)

---

### PASO 5 — Descargar el APK
1. Clic en el workflow completado (el verde)
2. Baja hasta la sección **"Artifacts"**
3. Clic en **"extremo-app-debug"** — se descarga un ZIP
4. Descomprime ese ZIP → adentro está el archivo **`app-debug.apk`**

---

### PASO 6 — Instalar en tu Android
1. Pasa el APK a tu teléfono (WhatsApp, cable USB, Google Drive, etc.)
2. En tu Android: **Ajustes → Seguridad → Instalar apps de fuentes desconocidas** → Activar
3. Abre el archivo APK desde el teléfono
4. Toca **"Instalar"**
5. La app aparece en tu pantalla de inicio como **"Extremo"**

---

## ¿Algo salió mal?
- Si el workflow falla → ve a la pestaña Actions, abre el error y mándame captura
- Si el APK no instala → verifica que activaste "fuentes desconocidas" en tu Android

---

## Estructura del proyecto
```
extremo-app/
├── www/
│   ├── index.html        ← App completa
│   └── icons/            ← Iconos de la app
├── .github/
│   └── workflows/
│       └── build-apk.yml ← Compilación automática
├── capacitor.config.json ← Configuración Android
├── package.json          ← Dependencias
└── README.md             ← Este archivo
```
