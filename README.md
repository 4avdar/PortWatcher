# 🔍 PortWatcher

PortWatcher is a Python-based network monitoring tool that uses Nmap to scan hosts, store port scan history in SQLite, and detect changes in network exposure over time.

---

## 🚀 Features

* 🔎 Scan a target host using Nmap
* 📊 Parse scan results from XML output
* 🗄️ Store scan history in SQLite
* 🔄 Compare current scan with previous scans
* ➕ Detect newly opened ports
* ➖ Detect closed ports
* 🟰 Identify unchanged open ports

---

## 🛠️ Technologies Used

* Python 3
* Nmap
* SQLite
* XML parsing with ElementTree

---

## ⚙️ Installation

Clone the repository:

```b=
git clone https://github.com/4avdar/PortWatcher.git
cd PortWatcher
```

Install required tools:

```bash
sudo apt update
sudo apt install nmap python3 -y
```

---

## ▶️ Usage

Run the tool:

```bash
python3 main.py
```

Enter the target IP address when prompted, or press Enter to use:

```text
127.0.0.1
```

---

## 📌 How It Works

1. The user enters a target IP address
2. PortWatcher runs an Nmap scan on the target
3. Open ports are extracted from XML output
4. Results are stored in a SQLite database
5. The current scan is compared with the previous scan
6. Changes are displayed in the terminal

---

## 📷 Example Output

```text
Scan time: 2026-03-25 18:30:00

Open ports now:
  22/tcp (ssh)
  80/tcp (http)
  3306/tcp (mysql)

Changes since last scan:
  + 3306/tcp opened (mysql)
  = 22/tcp unchanged (ssh)
  = 80/tcp unchanged (http)
```

---

## 📝 Notes

* The SQLite database (`portwatch.db`) is generated locally and is not included in the repository
* Nmap must be installed on the system
* This project is intended for educational and authorized security testing only

---

## 📈 Future Improvements

* Risk classification for common ports
* Network-wide host discovery (subnet scanning)
* JSON / CSV export
* Web dashboard (Flask)
* Scheduled automated scans

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

4avdar
