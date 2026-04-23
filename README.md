# 🚗 Amiabila — AI-Powered Digital Accident Reporting

> **1st Place Winner** at Moldova's GovTech Hackathon 🏆
> Official recognition from the **Ministry of Internal Affairs** for delivering exactly what was needed.

Amiabila is an AI-powered mobile-first web application that digitizes the road accident reporting process in Moldova. It replaces the traditional paper-based "Constatare Amiabilă" (amicable accident report) with a guided digital experience, featuring an **AI voice assistant** that walks users through the stressful process of documenting a car accident step by step.

At the hackathon demo, **the AI voice agent itself presented the product** to Ministry of Internal Affairs officials.

---

## ✨ Key Features

### 🎙️ AI Voice Assistant
- Real-time conversational AI powered by **ElevenLabs** that guides users step-by-step through the accident report in Romanian
- Context-aware instructions adapted to each form section
- Floating microphone button with visual feedback (connecting, listening, speaking states)
- Secure server-side agent configuration — credentials never exposed to the client

### 📋 11-Step Digital Form Wizard
A comprehensive guided flow covering every aspect of the legal accident report:

| Step | Feature | Highlights |
|------|---------|------------|
| 1 | **Legal Preconditions** | Checklist ensuring the amicable report is applicable |
| 2 | **Collaborative Session** | QR code for the second driver to join on their device |
| 3 | **Date, Time & Location** | Auto-filled via GPS + reverse geocoding (Nominatim) |
| 4 | **Witnesses** | Dynamic witness management with contact details |
| 5 | **Circumstances** | Vehicle status, actions, and road conditions |
| 6 | **Driver & Vehicle Data** | Auto-import from government digital identity services |
| 7 | **Accident Sketch** | Canvas editor with draggable/rotatable cars, arrows, text on a map background |
| 8 | **Damage Mapping** | Interactive SVG car diagrams — tap to mark impact zones + AI photo analysis |
| 9 | **Responsibility** | Legal responsibility declaration |
| 10 | **Review** | Complete expandable summary of all entered data |
| 11 | **Digital Signatures & Export** | Digital signing + PDF export |

### 🗺️ GPS & Maps
- Automatic location detection via browser Geolocation API
- Reverse geocoding (coordinates → street address) using OpenStreetMap Nominatim
- Embedded interactive map pinpointing the accident location

### 🚙 Interactive Damage Mapping
- Top-down SVG car diagrams with 15 clickable body zones per vehicle
- Multi-select impact point marking for both vehicles
- Photo upload with preview (up to 5 photos)
- AI-powered damage analysis from uploaded photos

### 🎨 Accident Sketch Editor
- HTML5 Canvas drawing tool with satellite map background
- Draggable, rotatable, and scalable car icons (Vehicle A & B)
- Directional arrows and text annotations
- Touch-optimized for mobile use

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Framework** | Next.js 15 (App Router) |
| **Language** | TypeScript |
| **AI Voice** | ElevenLabs Conversational AI |
| **UI Components** | Radix UI + shadcn/ui |
| **Styling** | Tailwind CSS |
| **Forms** | React Hook Form + Zod |
| **Maps** | OpenStreetMap + Nominatim |
| **Typography** | Onest + JetBrains Mono |

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- pnpm

### Installation

```bash
git clone https://github.com/DanD21/Amiabila.git
cd amiabila

pnpm install

cp .env.example .env.local
```

Edit `.env.local` and add your ElevenLabs Agent ID:

```env
ELEVENLABS_AGENT_ID=your_agent_id_here
```

> You can get an Agent ID by creating a Conversational AI agent at [elevenlabs.io](https://elevenlabs.io/conversational-ai).

### Run

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) — the app is optimized for mobile viewports.

---

## 📱 How It Works

```
┌─────────────────────────────────────────────────┐
│  User opens app after a minor car accident      │
│                                                 │
│  1. Confirms legal preconditions are met        │
│  2. Second driver joins via QR code             │
│  3. GPS auto-detects location                   │
│  4. AI voice guides through each section        │
│  5. Users mark damage on interactive car maps   │
│  6. Optional: sketch the accident scene         │
│  7. Both drivers sign digitally                 │
│  8. PDF report generated instantly              │
└─────────────────────────────────────────────────┘
```

The AI voice assistant is available throughout the entire process as a floating button, providing step-specific guidance in Romanian and adapting its instructions to the current context.

---

## 🏆 Hackathon & Recognition

- **Event:** GovTech Hackathon 2025, organized by Technovator Moldova in partnership with government institutions
- **Challenge:** Digitization of road accident reporting — presented by the Ministry of Internal Affairs
- **Team size:** 2 people
- **Result:** 🥇 **First Place**
- **Recognition:** Official gratitude diploma from the **Director of the Information Technology Service, Ministry of Internal Affairs**

The Ministry's official diploma noted that the prototype was developed *"with the possibility of integrating it into the existing government services infrastructure within the governmental digital ecosystem"* and that the initiative *"makes a significant contribution toward simplifying bureaucratic processes, reducing response times, and increasing accessibility for citizens."*

The solution was described by hackathon judges as one of the *"most innovative and practical presentations"* — a functional MVP that could be seamlessly integrated into real-life road accident scenarios. The AI voice assistant was the key differentiator: it calms users down during a high-stress situation and ensures they don't miss any required legal information.

---

## 📄 License

This project was built as a hackathon prototype and is shared for portfolio and educational purposes.

---

*Built with ❤️ in Moldova*