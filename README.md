# MockPrep India — CBT Mock Tests for Government Exams

A complete Computer-Based Test (CBT) mock test platform for Indian government competitive examinations — SSC, UPSC, Banking, Railway, Defence, Teaching, Police, Insurance, State PSC & Postal.

## Coverage

- **10 exam categories, 22 exams, 22 mock tests, ~640 questions**
- Authentic exam-like CBT interface with live ticking timer (auto-submit at zero)
- Question palette with 5 status colors (Not Visited / Not Answered / Answered / Marked / Answered & Marked)
- Per-exam negative marking schemes (SSC −0.50, IBPS −0.25, AFCAT −1.00, etc.)
- Detailed result page: score, accuracy, time taken, section-wise breakdown, question-by-question solutions
- Tier-wise exam pattern + original syllabus for every exam
- Mobile-first responsive design with sticky footer

## Exams included

| Category | Exams |
|---|---|
| SSC | CGL, CHSL, MTS, GD Constable |
| UPSC | Civil Services (Prelims GS + CSAT), CDS, NDA |
| Banking | IBPS PO, IBPS Clerk, SBI PO, RBI Grade B |
| Railway | RRB NTPC, RRB Group D |
| Defence | AFCAT, Territorial Army |
| Teaching | CTET |
| Police | Delhi Police Constable |
| Insurance | LIC AAO |
| State PSC | BPSC |
| Postal | India Post GDS |

## Tech stack

- **Framework**: Next.js 16 (App Router) + TypeScript 5
- **Styling**: Tailwind CSS 4 + shadcn/ui (New York)
- **State**: Zustand (client-side test runtime + scoring)
- **Database**: Prisma ORM + SQLite (configured but not required for mock test runtime)
- **Icons**: lucide-react
- **Animations**: Framer Motion

## Getting started

### Prerequisites
- Node.js 18+ (or [Bun](https://bun.sh) 1.0+)
- npm / pnpm / yarn / bun

### Install & run locally

```bash
# Install dependencies
npm install        # or: bun install

# Start dev server
npm run dev        # or: bun run dev
```

Open **http://localhost:3000** in your browser.

### Build for production

```bash
npm run build
npm start
```

## Project structure

```
src/
├── app/
│   ├── layout.tsx          # Root layout
│   └── page.tsx            # Home page + footer (single-route app)
├── components/
│   ├── mock-test/          # 6 views: home, category, exam-detail, instructions, test-running, result
│   └── ui/                 # shadcn/ui components
├── lib/
│   ├── categories.ts       # 10 exam category definitions
│   ├── exams/              # Exam data: SSC, UPSC, Banking, Railway, Other (Defence, Teaching, Police, Insurance, State PSC, Postal)
│   ├── test-store.ts       # Zustand store: timer, palette, scoring, navigation
│   └── types.ts            # TypeScript interfaces for Exam, MockTest, Question, etc.
└── hooks/                  # Custom React hooks
```

## How to use

1. From the **Home** page, pick an exam category (SSC, UPSC, Banking, etc.)
2. Browse the list of exams in that category
3. Click **View Exam Details** to see the original syllabus and tier-wise exam pattern
4. Pick a **Mock Test** → read the instructions → click **Start Test Now**
5. The timer starts immediately. Use Save & Next, Mark for Review, Clear Response, and the question palette to navigate
6. Click **Submit Test** (or let the timer hit zero) to see your detailed result with section-wise breakdown and explanations

## Disclaimer

Mock tests on this platform are practice tests designed to mirror the pattern, timer and marking scheme of the original examinations. They are not affiliated with or endorsed by the conducting bodies (SSC, UPSC, IBPS, RBI, RRB, LIC, etc.). Refer to official notifications for accurate exam details.

## Powered by

[The Project Wala](https://www.theprojectwala.com)

---

© MockPrep India · Built for aspirants, by aspirants.
