# 🎮 MineMauro — Minecraft Server on Google Colab

Host a Minecraft Java **26.1.1 (Tiny Takeover)** server for free using Google Colab + Google Drive + Playit.gg. No VPS, no payments, nothing.

> 🌐 [English Manual](#-english-manual) | [Manual en Español](#-manual-en-español)

---

## 📋 Requirements

- Google account (for Colab and Drive)
- Account on [playit.gg](https://playit.gg) (free)
- Minecraft Java Edition (to connect)

Everything else (Java 25, server.jar, etc.) is downloaded automatically by the notebook.

---

## 📁 Google Drive folder structure

Just create an empty folder in your Drive:

```
My Drive/
└── Minecraft-server/
```

Everything (`server.jar`, `libraries/`, `versions/`, `world/`, etc.) is downloaded and generated automatically the first time you run the notebook.

---

## 🇬🇧 English Manual

### Step 1 — Open the notebook in Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MaurOSdev/MineMauro/blob/main/KernelServer.ipynb)

### Step 2 — Run the SETUP SCRIPT

Run the **SETUP SCRIPT** cell. This will:
- Download and install Java 25 (only if not already installed)
- Download server.jar (only if not already downloaded)
- Mount your Google Drive (will ask for permission the first time)
- Configure everything automatically

### Step 3 — Run the S.O.S SCRIPT (first time only)

If it's your first time, run the **S.O.S SCRIPT** cell:

```
🔗 A link will appear like: https://playit.gg/claim/xxxxxxxx
```

1. Open the link in your browser
2. Log in to playit.gg
3. Accept the claim
4. Wait for the timeout to finish (60 seconds)

> ✅ After this, the config is saved to your Drive automatically. Next time you can skip this step.

### Step 4 — Run the MAIN SCRIPT

Run the **MAIN SCRIPT** cell. This launches the playit tunnel and starts Minecraft. You'll see:

```
tunnel running, 1 tunnels registered
```

### Step 5 — Get the IP

Go to [playit.gg](https://playit.gg) → **Tunnels** and copy the address. It will look like:

```
abc123.ply.gg:25565
```

### Step 6 — Connect

In Minecraft Java:
1. Multiplayer → Add Server
2. Paste the tunnel address
3. Connect! 🎮

**Every session after the first:**
1. SETUP SCRIPT
2. MAIN SCRIPT

---

## ⚠️ Important notes

- **Colab sessions last ~12 hours** — after that you need to re-run the notebook
- **online-mode=false** — any user can join with any username. Use the whitelist if you want to control access
- **RAM** — the server uses 8GB by default. Colab Pro gives more stability
- **Don't close the Colab tab** or the server will shut down

---

## 🛠️ Troubleshooting

| Problem | Solution |
|---|---|
| `Invalid secret` | Run the S.O.S SCRIPT again |
| `Network unreachable` | Reconnect to Colab and run again |
| `No such file or directory` | Make sure the folder exists in `My Drive/Minecraft-server/` |
| Playit won't connect | Delete `/root/.config/playit_gg/playit.toml` and run S.O.S SCRIPT again |

---

## 🐛 Found a bug?

Open an issue at https://github.com/MaurOSdev/MineMauro/issues

---

---

# 🎮 MineMauro — Servidor de Minecraft en Google Colab

Hostea un servidor de Minecraft Java **26.1.1 (Tiny Takeover)** gratis usando Google Colab + Google Drive + Playit.gg. Sin VPS, sin pagar nada.

> 🌐 [English Manual](#-english-manual) | [Manual en Español](#-manual-en-español)

---

## 📋 Requisitos

- Cuenta de Google (para Colab y Drive)
- Cuenta en [playit.gg](https://playit.gg) (gratis)
- Minecraft Java Edition (para conectarte)

Todo lo demás (Java 25, server.jar, etc.) se descarga automáticamente con el notebook.

---

## 📁 Estructura de carpetas en Google Drive

Solo crea una carpeta vacía en tu Drive:

```
My Drive/
└── Minecraft-server/
```

Todo lo demás (`server.jar`, `libraries/`, `versions/`, `world/`, etc.) se descarga y genera automáticamente la primera vez que corres el notebook.

---

## 🇪🇸 Manual en Español

### Paso 1 — Abrir el notebook en Colab

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MaurOSdev/MineMauro/blob/main/KernelServer.ipynb)

### Paso 2 — Correr el SETUP SCRIPT

Corre la celda **SETUP SCRIPT**. Esto va a:
- Descargar e instalar Java 25 (solo si no está instalado)
- Descargar el server.jar (solo si no existe)
- Montar tu Google Drive (pedirá permiso la primera vez)
- Configurar todo automáticamente

### Paso 3 — Correr el S.O.S SCRIPT (solo la primera vez)

Si es tu primera vez, corre la celda **S.O.S SCRIPT**:

```
🔗 Aparecerá un link como: https://playit.gg/claim/xxxxxxxx
```

1. Abre el link en tu navegador
2. Inicia sesión en playit.gg
3. Acepta el claim
4. Espera que termine el timeout (60 segundos)

> ✅ Después de esto la config se guarda en tu Drive automáticamente. Las próximas veces puedes saltarte este paso.

### Paso 4 — Correr el MAIN SCRIPT

Corre la celda **MAIN SCRIPT**. Esto lanza el túnel de playit y arranca Minecraft. Verás:

```
tunnel running, 1 tunnels registered
```

### Paso 5 — Obtener la IP

Ve a [playit.gg](https://playit.gg) → **Tunnels** y copia la dirección. Será algo como:

```
abc123.ply.gg:25565
```

### Paso 6 — Conectarse

En Minecraft Java:
1. Multijugador → Añadir servidor
2. Pega la dirección del túnel
3. ¡Conectar! 🎮

**Cada sesión después de la primera:**
1. SETUP SCRIPT
2. MAIN SCRIPT

---

## ⚠️ Notas importantes

- **Las sesiones de Colab duran ~12 horas** — después necesitas volver a correr el notebook
- **online-mode=false** — cualquier usuario puede entrar con cualquier nombre. Usa la whitelist si quieres controlar el acceso
- **RAM** — el servidor usa 8GB por defecto. Colab Pro da más estabilidad
- **No cierres la pestaña de Colab** o el servidor se apaga

---

## 🛠️ Solución de problemas

| Problema | Solución |
|---|---|
| `Invalid secret` | Corre el S.O.S SCRIPT de nuevo |
| `Network unreachable` | Reconecta a Colab y vuelve a correr |
| `No such file or directory` | Verifica que la carpeta exista en `My Drive/Minecraft-server/` |
| Playit no conecta | Borra `/root/.config/playit_gg/playit.toml` y corre el S.O.S SCRIPT de nuevo |

---

## 🐛 ¿Encontraste un bug?

Abre un issue en https://github.com/MaurOSdev/MineMauro/issues

---

## 📄 Licencia

GPL-3.0 — ve el archivo [LICENSE](LICENSE) para más detalles.

---

Hecho con ☕ y 8 horas de sufrimiento por [MaurOSdev](https://github.com/MaurOSdev)
