# 🚀 ucompose-for-udocker

A lightweight, rootless `docker-compose` CLI translation layer built specifically for **Termux** users and environments without a compiled/compatible kernel. 

Write your configurations as a native `docker-compose.yml` file, and `ucompose` will automatically translate and execute them as user-space `udocker` commands.

---

## 🌟 Key Features
* **Zero Root Required:** Runs completely in user-space using `PRoot` / `Fakechroot`.
* **Standard Syntax:** No need to learn complex `udocker` CLI flags. Write standard compose files.
* **Kernel Independent:** Perfect for Android power users and legacy Linux hardware.
* **Zero Maintenance Friction:** Designed for upstream stability with `udocker`.

---

## 📥 Installation

> ⚠️ **Prerequisite:** Ensure you have `udocker` installed natively in Termux via `pkg install udocker` or its official github https://github.com/indigo-dc/udocker before proceeding.

Instantly install ucompose and view the help menu using our official one-liner:

```bash
curl -sSL -o ucompose https://github.com/jimkardy/ucompose-for-udocker/releases/latest/download/ucompose.txt && chmod +x ucompose && ./ucompose --help
```

---

## 🛠️ Usage Examples

Interact with your containers exactly like you would using standard docker-compose:

```bash
# Spin up your environment in the background
./ucompose up -d

# Start your containers
./ucompose start

# Stop execution
./ucompose stop

# Tear down the stack
./ucompose down
```

---

## ⚖️ Advantages & System Limitations

* **Advantage:** Because `udocker` is a mature, slow-moving project, this wrapper layout is highly stable and will not require constant breaking-change updates over the long term.
* **Limitation:** Only core docker-compose commands translated by the script are supported. It is strictly optimized for user-space environment limitations.
