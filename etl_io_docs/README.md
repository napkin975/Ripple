# ETL.io - AI ETL Agent for Google Workspace

AI-powered Extract, Transform, Load agent with a Sanctuary-inspired dark theme.

## Live Demo
https://etlio.vercel.app

## GitHub Repository
https://github.com/mahdi1234-hub/etl.io

## Features

### Google OAuth Authentication (NextAuth)
- All Google Workspace scopes
- Token refresh with offline access
- Session management

### Google Workspace Integrations
- **Gmail**: List, read, send emails
- **Drive**: List files, read content (Docs/Sheets/Slides auto-export)
- **Sheets**: List, read, write, create spreadsheets
- **Docs**: List, read, create documents
- **Calendar**: List events, create events
- **Tasks**: List task lists, list tasks
- **Contacts**: List contacts

### AI ETL Agent
- Cerebras LLM (llama3.1-8b) powered
- Tool calling with automatic Google API execution
- Multi-step ETL pipelines (extract -> transform -> load)
- Cross-service data transfer (emails to sheets, calendar to docs, etc.)

### Sanctuary Theme
- Dark aesthetic (#1a1c1a background)
- Cormorant Garamond serif + Syncopate sans-serif fonts
- Noise texture overlay
- Nature background on login
- Animated transitions

## Tech Stack
- Next.js 16 (App Router)
- TypeScript, Tailwind CSS
- NextAuth v4 (Google OAuth)
- googleapis npm package
- Cerebras AI API
- Vercel deployment
