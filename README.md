# CyberCode - All-in-One Cybersecurity Platform

An ultra-modern cybersecurity toolkit built with Next.js, TypeScript, Tailwind CSS, and Shadcn UI. Features 10 real security analysis tools with a futuristic dark theme.

## Features

- **IP Address Analyzer** — IPv4/IPv6 lookup, geolocation, ISP, ASN, VPN/proxy detection, risk scoring
- **Website Security Scanner** — SSL inspection, security headers analysis, DNS records, vulnerability scoring
- **Phishing Detector** — URL analysis, homograph detection, suspicious keyword scanning, risk scoring
- **Privacy Dashboard** — Browser fingerprint, cookie/storage analysis, permission auditing, privacy score
- **Password Center** — Secure generator (Web Crypto API), entropy calculator, strength analyzer, encrypted vault
- **Security Monitor** — Real-time threat visualization with interactive charts (Recharts)
- **Network Analyzer** — Full DNS record analysis, latency testing, SOA record inspection
- **Threat Intelligence Hub** — CVE search via NVD API, MITRE ATT&CK framework explorer
- **Digital Footprint Analyzer** — Username availability checker across 6 platforms
- **OS Info** — Server system information (hostname, CPU, memory, network interfaces)

## Deploy to Vercel (One-Click)

This project is pre-configured for Vercel deployment — everything runs as Next.js API routes, no separate backend needed.

### Method 1: Vercel CLI

```bash
cd frontend
npx vercel
```

### Method 2: Git + Vercel

1. Push the `frontend/` directory to a GitHub repo (or the entire project)
2. Import into Vercel — set **Root Directory** to `frontend`
3. Framework preset: **Next.js**
4. Deploy — that's it

The API routes (`/api/*`) become Vercel serverless functions automatically.

### Local Development

```bash
cd frontend
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Tech Stack

- **Framework**: Next.js 16
- **Language**: TypeScript
- **Styling**: Tailwind CSS 4 + Shadcn UI
- **Charts**: Recharts
- **Icons**: Lucide React
- **APIs**: ipapi.co, ipwho.is, ipinfo.io, NVD (CVE), all called server-side via API routes

## Project Structure

```
frontend/
├── src/
│   ├── app/
│   │   ├── api/               # API routes (serverless functions)
│   │   │   ├── ip/lookup/[ip]
│   │   │   ├── security/scan
│   │   │   ├── phishing/analyze
│   │   │   ├── network/dns
│   │   │   ├── threat/cve/{search,latest}
│   │   │   ├── footprint/username
│   │   │   ├── os
│   │   │   └── health
│   │   ├── (page directories)  # 11 frontend pages
│   │   ├── globals.css         # Cyber theme
│   │   ├── layout.tsx           # Root layout + sidebar
│   │   └── page.tsx             # Dashboard
│   ├── components/             # Shared UI (Sidebar, StatCard, ThreatMeter, etc.)
│   ├── services/               # Server-side logic (DNS, SSL, IP, CVE, phishing, etc.)
│   └── utils/                  # Risk scoring engine
```

## API Endpoints

| Endpoint | Description |
|----------|-------------|
| `GET /api/health` | Health check |
| `GET /api/ip/lookup/:ip` | IP address lookup |
| `GET /api/security/scan?url=` | Website security scan |
| `POST /api/phishing/analyze` | Phishing URL analysis |
| `GET /api/network/dns?hostname=` | DNS analysis |
| `GET /api/threat/cve/search?q=` | CVE search |
| `GET /api/threat/cve/latest` | Latest CVEs |
| `GET /api/footprint/username?username=` | Username check |
| `GET /api/os` | Server OS information |

## Design

- Dark cyberpunk theme with glassmorphism cards
- Neon blue (#00d4ff), cyan (#00ff88), purple (#7c3aed) accents
- Animated particle network background
- Scan-line effects on input cards
- Smooth entrance animations
- Fully responsive layout
