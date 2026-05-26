# CRT Classes Attendance Tracker

A personal attendance tracker built with pure HTML, CSS, and JavaScript — no frameworks, no backend, no dependencies. Data is saved in the browser's `localStorage` and persists across sessions.

---

## Student Info

| Field | Value |
|-------|-------|
| Name | MAMIDI YUGANDHAR RAO |
| Roll No | 2300032847 |
| Branch | CSE · CSE1 · Cluster C2 |
| Subject | IS201 |
| Room | R404A |

---

## Features

- ✅ Add attendance for any date with per-slot P / A toggle
- ✅ 8 configurable time slots per day (09:20 → 16:30)
- ✅ Edit or delete any past entry
- ✅ Live attendance percentage calculation
- ✅ Progress bar with 75% and 85% threshold markers
- ✅ **Bunk Calculator** — shows exactly how many classes you can skip and still stay above 85%
- ✅ Personalized advice based on current attendance
- ✅ Full attendance log with per-slot badges
- ✅ Data persists via `localStorage` — no login, no server
- ✅ Works fully offline after download

---

## Project Structure

```
crt_attendance/
├── index.html      # Main app — all HTML, CSS, JS in one file
└── vercel.json     # Vercel deployment config
```

---

## How to Run Locally

1. Clone or download this repository
2. Open `index.html` directly in any browser (Chrome, Edge, Firefox)
3. No installation, no server, no `npm install` needed

```bash
git clone https://github.com/Yugandhar06/crt_attendance.git
cd crt_attendance
# Just open index.html in your browser
```

---

## Deploying to Vercel

### Option 1 — Via GitHub (recommended)

1. Push this repo to GitHub
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Import the GitHub repo
4. Click **Deploy** — done ✅

### Option 2 — Via Vercel CLI

```bash
npm install -g vercel
cd crt_attendance
vercel
```

Follow the prompts, and your live URL will be ready in ~30 seconds.

---

## How the Bunk Calculator Works

Given your current **present (P)** and **total sessions**:

| Metric | Formula |
|--------|---------|
| Can bunk (85%) | `floor(P / 0.85 − total)` |
| Can bunk (75%) | `floor(P / 0.75 − total)` |
| Need to attend | `ceil((0.85 × total − P) / 0.15)` |

Example: 92 present out of 104 total → **88.4%** → can bunk **4 more** and stay above 85%.

---

## Data Storage

- All data is saved in `localStorage` under the key `att_tracker_v3`
- Tied to the browser + file location — moving the file or switching browsers resets data
- To back up: open browser DevTools → Application → Local Storage → copy the value

---

## Built With

- HTML5
- CSS3 (CSS Variables, Grid, Flexbox)
- Vanilla JavaScript (no frameworks)
- Google Fonts — DM Sans + Space Mono

---

##  License

Personal use only — built for tracking CRT attendance at university.
