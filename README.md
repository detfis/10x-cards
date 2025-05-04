# 10x-cards

> A web application for quick creation and management of educational flashcards, powered by LLM-based AI generation and spaced repetition.

<!-- TOC -->
- [Project Description](#project-description)
- [Tech Stack](#tech-stack)
- [Getting Started Locally](#getting-started-locally)
- [Available Scripts](#available-scripts)
- [Project Scope](#project-scope)
- [Project Status](#project-status)
- [License](#license)
<!-- TOC -->

## Project Description

10x-cards helps learners drastically reduce the time and effort needed to create high-quality flashcards. By pasting any text (e.g., a textbook excerpt), the application calls an LLM API to generate suggested question-and-answer flashcards. Users can review, edit, accept, or reject suggestions, then store approved cards in their personal library, all secured behind user authentication. A spaced repetition algorithm schedules review sessions to optimize learning retention.

## Tech Stack

**Frontend**
- Astro 5
- React 19
- TypeScript 5
- Tailwind CSS 4
- Shadcn/ui component library

**Backend**
- Supabase (PostgreSQL database & Auth)

**AI Integration**
- Openrouter.ai (access to OpenAI, Anthropic, Google, etc., models with cost-control features)

**CI/CD & Hosting**
- GitHub Actions for build/test/deploy pipelines
- Docker on DigitalOcean for production hosting

## Getting Started Locally

### Prerequisites

- Node.js v22.15.0 (see `.nvmrc`)
- Git
- A Supabase project (for database & auth)
- Openrouter.ai API key

### Clone and Install

```bash
git clone https://github.com/<your-org>/10x-cards.git
cd 10x-cards
nvm use
npm install
```

### Environment Variables

Create a `.env` file in the project root with:

```ini
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_anon_key
OPENROUTER_API_KEY=your_openrouter_api_key
```

### Development Server

```bash
npm run dev
```

Visit `http://localhost:3000` (or the port indicated in the terminal) to view the app.

## Available Scripts

| Script            | Description                     |
| ----------------- | ------------------------------- |
| `npm run dev`     | Start Astro in dev mode         |
| `npm run build`   | Build the site for production   |
| `npm run preview` | Preview production build        |
| `npm run astro`   | Run Astro CLI                   |
| `npm run lint`    | Run ESLint checks               |
| `npm run lint:fix`| Run ESLint with auto-fixes      |
| `npm run format`  | Format code with Prettier       |

## Project Scope

### In-Scope (MVP)

- AI-driven flashcard generation from user-provided text
- Manual flashcard creation, editing, and deletion
- User authentication (register, login, delete account)
- Integration with an open-source spaced repetition algorithm
- Secure, scalable storage of users and flashcards using Supabase
- Basic generation statistics (AI-generated vs. accepted)
- GDPR compliance (data access & deletion on request)

### Out-of-Scope (Future)

- Custom SRS algorithm or advanced notifications
- Gamification features
- Native mobile applications
- Bulk import of document formats (PDF, DOCX, etc.)
- Public API or flashcard sharing between users
- Advanced search and filtering of flashcards

## Project Status

🚧 This project is in **active development** as an MVP. Features and APIs may change. Contributions and feedback are welcome!

## License

_No license specified._
Please add a `LICENSE` file to clearly define the project's licensing terms.