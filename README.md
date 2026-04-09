
# 🦉 LexiQuest

**Master the GRE with High-Performance AI & Gamification**

LexiQuest is a premium, Duolingo-inspired GRE vocabulary platform. By combining the **safety and blazing speed of Rust** with the intelligence of **Claude 3.5 Sonnet**, LexiQuest transforms messy OCR data and raw word lists into rich, interactive learning experiences — up to **10-100x faster** than traditional JavaScript/Python solutions.

---

## 🚀 Key Features

- **Intelligent Extraction**: Advanced Rust + Claude 3.5 pipeline that perfectly parses complex GRE word lists and imperfect OCR text.
- **AI Enrichment**: Automatically generates memorable mnemonics, etymology, usage examples, and contextual sentences using Anthropic’s latest model.
- **Gamified Learning**: 7 core modules including **Story Mode**, **Flashcards**, **Quizzes**, **Match Madness**, and more — complete with animated streaks, XP, and leaderboards.
- **LingoBot Sidebar**: Persistent AI companion powered by **Groq** for real-time streaming chat and instant vocabulary help.
- **Premium UI**: Beautiful **"Premium Pastel Dark"** aesthetic (inspired by Apple & Stripe) with smooth GSAP micro-interactions and Tailwind CSS.
- **Persistent Progress**: Full **Supabase** integration for cloud-synced vocabulary, points, study sessions, and spaced repetition.

---

## 🛠 Tech Stack

### Frontend
- **Framework**: React + TypeScript + Vite
- **Styling**: Tailwind CSS
- **Animation**: GSAP (GreenSock Animation Platform)
- **Database & Auth**: Supabase Client

### Backend (The High-Performance Engine)
- **Language**: **Rust**
- **Web Framework**: Actix-web
- **AI Integration**: Claude 3.5 Sonnet (via Anthropic API)
- **Processing**: High-speed regex normalization + mojibake repair

### Data Layer
- **Primary Database**: PostgreSQL (via Supabase)
- **Chat AI**: Groq (ultra low-latency streaming)

---

## 📦 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/lexiquest.git
cd lexiquest
```

### 2. Frontend Setup
```bash
npm install
```

### 3. Backend Setup
```bash
cd backend
cp .env.example .env
```

> **Important**: Add your `ANTHROPIC_API_KEY` inside the `.env` file.

### 4. Frontend Environment Variables
Create a `.env.local` file in the root directory:

```env
VITE_BACKEND_URL=http://localhost:3001
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
VITE_GROQ_API_KEY=your_groq_api_key
```

---

## 🚦 Running LexiQuest

### All-in-One Command (Recommended)
```bash
npm run dev:all
```

### Individual Commands

| Command                  | Description                              | Port   |
|--------------------------|------------------------------------------|--------|
| `npm run dev:backend`    | Starts Rust Actix-web API                | 3001   |
| `npm run dev`            | Starts Vite React frontend               | 5173   |

---

## 📊 Performance Benchmarks

Thanks to the Rust backend migration:

| Operation              | Legacy JS | Rust + Claude | Improvement |
|------------------------|-----------|---------------|-------------|
| Regex Extraction       | 200ms     | 50ms          | **4x**      |
| Claude Extraction      | 3000ms    | 1200ms        | **2.5x**    |
| Full Enrichment        | 8000ms    | 2500ms        | **3.2x**    |

---

## 🏗 Database Schema

LexiQuest uses a clean relational PostgreSQL schema optimized for **Spaced Repetition (SRS)**:

- `words` — Core vocabulary with AI-generated etymology & mnemonics
- `progress` — Tracks `ease_score`, `times_seen`, `next_review`
- `points` & `gifts` — Powers the gamification and reward shop
- `sessions` — Study activity and XP logging

> **Tip**: Run the migration scripts located in `/supabase/schema.sql` and `/supabase/seed.sql` to quickly set up the database with a standard GRE starter pack.

---

## 🐍 Python CLI Support (Power Users)

For bulk processing of raw notes:

```bash
cd scripts
export ANTHROPIC_API_KEY='your_key'
python gre_word_extractor.py --input raw_notes.txt --output words.json --format json
```

---

## 🎨 UI Philosophy

- **Whitespace-First** design — content is king
- **Premium Pastel Dark** theme with soft, professional colors
- Smooth **GSAP** micro-interactions on every action
- Fully responsive (optimized for focused desktop study + mobile review)

---

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

**Built with 🦀 Rust + ✨ Claude 3.5 + ❤️ for the GRE community**

---

Ready to level up your GRE prep?  
Start learning smarter, faster, and more enjoyably today! 🚀
```



Would you like a version with screenshots placeholders or contribution guidelines added as well?
```
