# 🎮 MineMauro — Minecraft Server on Google Colab

Host a Minecraft Java **26.1.1 (Tiny Takeover)** server for free using Google Colab + Google Drive + Playit.gg. No VPS, no payments, nothing.

---

## 📋 Requirements

- Google account (for Colab and Drive)
- Account on [playit.gg](https://playit.gg) (free)
- Minecraft Java Edition (to connect)
- Server files (see below)

---

## 📁 Google Drive folder structure

Create this folder in your Drive with the server files:

```
My Drive/
└── Minecraft-server/
    ├── server.jar        ← 26.1.1 server JAR
    ├── libraries/        ← server libraries folder
    └── versions/         ← versions folder
```

> ⚠️ The `server.jar` and the `libraries/` and `versions/` folders are obtained by downloading the official Minecraft 26.1.1 server from [minecraft.net](https://minecraft.net).

---

## 🚀 How to use

### Step 1 — Open the notebook in Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MaurOSdev/MineMauro/blob/main/KernelServer.ipynb)

### Step 2 — Install Java 25

The server requires Java 25. Run this cell first (only the first time):

```python
!apt-get install -y wget > /dev/null 2>&1
!wget -q "https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz" -O /tmp/jdk25.tar.gz
!mkdir -p /opt/jdk-mc && tar -xzf /tmp/jdk25.tar.gz -C /opt/jdk-mc --strip-components=1
!java -version
```

### Step 3 — Cell 1: Setup

Run **Cell 1** of the notebook. This will:
- Mount your Google Drive
- Configure the environment
- Enable `online-mode=false` (required in Colab)
- Automatically accept the EULA

### Step 4 — Claim Cell (first time only)

If it's your first time, run the **Claim Cell**:

```
🔗 A link will appear like: https://playit.gg/claim/xxxxxxxx
```

1. Open the link in your browser
2. Log in to playit.gg
3. Accept the claim
4. Wait for the timeout to finish (60 seconds)

> ✅ After this, the config is saved automatically. Next time you don't need to repeat this step.

### Step 5 — Cell 2: Launch the server

Run **Cell 2**. This launches the playit tunnel and starts Minecraft. You'll see something like:

```
tunnel running, 1 tunnels registered
```

### Step 6 — Get the IP

Go to [playit.gg](https://playit.gg) → **Tunnels** and copy the address. It will look like:

```
abc123.ply.gg:25565
```

### Step 7 — Connect

In Minecraft Java:
1. Multiplayer → Add Server
2. Paste the tunnel address
3. Connect! 🎮

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
| `Invalid secret` | Run the Claim Cell again |
| `Network unreachable` | Reconnect to Colab and run again |
| `No such file or directory` | Make sure the files are in `My Drive/Minecraft-server/` |
| Playit won't connect | Delete `/root/.config/playit_gg/playit.toml` and claim again |

---

## 📄 License

GPL-3.0 — see the [LICENSE](LICENSE) file for details.

---

Made with ☕ and 8 hours of pain by [MaurOSdev](https://github.com/MaurOSdev)
