# Search Skills

**Path:** Free Path (my own order)
**Date:** [11/6/2026]
**Room Link:** [Search Skills](https://tryhackme.com/room/searchskillscS)

## Overview

Knowing where to search is as important as knowing what to search for. This room introduces websites and tools that security people use to gather information, for both offensive and defensive work.

## Key Terms

- **IoT** = Internet of Things: everyday devices connected to the internet (cameras, routers, etc.).
- **Banner** = information a device shares about itself, like the software name and version.
- **Hash** = a unique fingerprint of a file. Same file, same hash.
- **CVE** = a unique ID for a known vulnerability, in the format `CVE-YEAR-NUMBER`.
- **CVSS** = a score from 0 to 10 showing how serious a vulnerability is.
- **PoC** = Proof of Concept: a script that shows a vulnerability really works.
- **Apache** = a program that runs on a server and sends website pages to browsers.

## Tools and What They Answer

| Tool | What it does |
|---|---|
| **Shodan** | Search engine for internet-connected devices and the software they run |
| **VirusTotal** | Checks a file, URL, domain, or hash against 70+ antivirus engines |
| **CVE / Vulnerability DB** | Gives each known vulnerability a unique ID and severity score |
| **GitHub** | Researchers share PoCs, tools, and reports (check safety first) |
| **Man pages** | Built-in Linux manuals: `man <command>` |

## Shodan Filters

| Filter | Example | Meaning |
|---|---|---|
| `country` | `country:IE` | Results from one country |
| `port` | `port:22` | Devices with that port open |
| `org` | `org:"Amazon"` | Devices owned by an organisation |
| `hostname` | `hostname:fakebank.thm` | Devices matching a domain |

Filters can be combined to narrow results.

## What I Did

1. Used a Shodan simulation to search with filters.
2. Used a VirusTotal simulation to check a file or link.
3. Searched a vulnerability database for CVE details.
4. Read a Linux man page for a command (`nc`).
5. Looked through a GitHub repository for a PoC script.

## How the Tools Connect

Shodan finds a device running old software → the CVE gives the vulnerability its name and score → GitHub may have a PoC that demonstrates it → VirusTotal and man pages help me check and understand things safely.

## Safety Notes

- Searching Shodan is legal, but accessing devices without permission is not.
- Files uploaded to VirusTotal become visible to others, so never upload private files.
- Not every PoC on GitHub is safe. Read the code first and run it in a VM.
- Only test vulnerabilities on systems I own or have permission to test.
