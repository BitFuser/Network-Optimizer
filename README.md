# 🌐 Network Optimizer v1.0

A Windows-based GUI tool to automatically run common network reset and optimization commands. Useful for fixing DNS issues, renewing IP configurations, resetting Winsock, and more—all in one click.

---

## ⚡ Features

- 🖱️ One-click network optimization
- 📜 Flush DNS, reset TCP/IP, Winsock, and more
- 📶 Ping test to Google DNS
- 🪟 Minimalist, hacker-style console UI with live logs
- 🧠 Built-in output window with color-coded sections
- ✔️ Compatible with Windows 10/11

---

## 📦 Requirements

- **Platform:** Windows only  
- **Dependencies:** Standard Python libraries (no external packages)

✅ No installation required — just run with Python 3.

---

## 🚀 How to Run

```bash
python network_optimizer.py
```

---

## 🖥️ GUI Preview

```
+----------------------------------------------------+
|            Network Optimizer v1.0                  |
|----------------------------------------------------|
| > Flushing DNS...                                  |
| Successfully flushed the DNS Resolver Cache.       |
|                                                    |
| > Releasing IP...                                  |
| Windows IP Configuration                           |
|                                                    |
| > Renewing IP...                                   |
| ...                                                |
|                                                    |
| [✔] Optimization Complete.                         |
+----------------------------------------------------+
|              [ Run Optimization ]                  |
+----------------------------------------------------+
```

---

## ⚙️ Optimization Commands Used

| Action                 | Command                        |
|------------------------|--------------------------------|
| Flush DNS              | `ipconfig /flushdns`           |
| Release IP             | `ipconfig /release`            |
| Renew IP               | `ipconfig /renew`              |
| Reset Winsock          | `netsh winsock reset`          |
| Reset TCP/IP Stack     | `netsh int ip reset`           |
| Ping Google DNS        | `ping 8.8.8.8 -n 4`            |

All output is captured and displayed in a scrollable console-style text area with color-coded highlights.

---

## 🧠 How It Works

- Uses `subprocess.run` to execute network-related commands
- Live feedback is displayed in a read-only `tkinter.scrolledtext` widget
- Optimizations run in sequence and show real-time results
- Designed for troubleshooting slow connections or DNS caching issues

---

## ⚠️ Disclaimer

This tool:
- **Requires Administrator privileges** to fully function
- **Is intended for Windows systems only**
- Does not make permanent registry/network config changes outside standard resets
