# PortWatcher

PortWatcher is a Python-based network monitoring tool that uses Nmap to scan a target host, store port scan history in SQLite, and detect changes in exposed services over time.

## Features

- Scan a target host using Nmap
- Parse scan results from XML output
- Store scan history in SQLite
- Compare the current scan with the previous scan
- Detect newly opened ports
- Detect closed ports
- Show unchanged open ports

## Technologies Used

- Python 3
- Nmap
- SQLite
- XML parsing with ElementTree

## How It Works

1. The user enters a target IP address
2. PortWatcher runs an Nmap scan on that target
3. Open ports are extracted from the XML output
4. The scan results are saved into a SQLite database
5. The new scan is compared with the previous scan for the same target
6. Changes are displayed in the terminal

## Example Output

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
