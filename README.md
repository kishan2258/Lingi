# 🌍 Language Practice App

A personalized, interactive language-learning web application for **English, French, and German**.

The goal of this project is to go beyond simple text summaries. The application uses the learner's **current language level, uploaded study material, interactive exercises, audio, speaking practice, stories, jokes, and learning history** to create a more engaging language-learning experience.

---

## ✨ Features

### 🌐 Three Languages

Currently supported:

* 🇩🇪 German
* 🇫🇷 French
* 🇬🇧 English

When the user first opens the application, they choose:

1. The language they want to learn.
2. Their current level.

Supported levels:

* Beginner
* A1
* A2
* B1
* B2
* C1

The selected language and level are used throughout the application.

---

## 📚 Personalized Learning

The application is designed around the learner rather than a fixed course.

Users can practice:

* Vocabulary
* Grammar
* Reading
* Listening
* Writing
* Speaking
* Pronunciation

Learning activities should adapt to the user's previous performance, mistakes, confidence, and progress.

---

## 📖 User Learning Material

The application can be designed to use the learner's own educational material as the primary source of content.

Each language has three main content categories:

```text
English/
├── Study Material
├── Stories
└── Jokes

French/
├── Study Material
├── Stories
└── Jokes

German/
├── Study Material
├── Stories
└── Jokes
```

Supported source formats can include:

* TXT
* PDF
* DOCX

Uploaded content is processed, divided into useful sections/chunks, and stored so that relevant material can be retrieved when generating lessons.

The AI should not simply invent an unrelated curriculum. Uploaded material is treated as the primary learning source.

---

# 🧠 Learning Architecture

The main learning cycle is:

```text
Source Material
      ↓
Text Extraction
      ↓
Cleaning & Chunking
      ↓
Content Storage
      ↓
Relevant Content Retrieval
      ↓
AI Lesson Generation
      ↓
Learning
      ↓
Practice
      ↓
Review
      ↓
Progress Tracking
      ↓
Adaptive Recommendations
```

---

# 🏠 Main Sections

## Home

The dashboard gives the learner a quick overview of their current progress.

It can display:

* Current language
* Current level
* Daily goal
* Daily progress
* Recent lesson
* Vocabulary due for review
* Speaking practice
* Recommended activity
* Learning streak

---

## 📚 Learn

The Learn section provides structured lessons based on the user's selected language and level.

A lesson can contain:

* Explanation
* Vocabulary
* Example sentences
* Grammar notes
* Listening activities
* Interactive exercises

Important words and example sentences should have audio playback.

---

## 🔄 Review

The Review section helps learners remember previously learned material.

Review frequency can be based on:

* Correct answers
* Incorrect answers
* Confidence
* Previous review date
* Vocabulary difficulty

Difficult words should appear more frequently while well-known words should gradually appear less often.

---

## 🗣️ Practice

Practice activities can include:

* Multiple choice
* Translation
* Fill in the blank
* Vocabulary recall
* Listening
* Speaking
* Conversation

Every submitted answer should be evaluated and recorded.

---

## 📖 Stories

Stories provide contextual language exposure.

A story can support:

* Reading
* Listening
* Sentence-level audio
* Vocabulary explanations
* Translation/reveal
* Comprehension questions
* Retelling exercises

---

## 😂 Jokes

Jokes provide casual and natural language exposure.

Each joke can contain:

* Original text
* Audio
* Vocabulary
* Translation/reveal
* Explanation of difficult expressions
* Comprehension activities

The original joke should remain intact rather than being unnecessarily rewritten.

---

## 📊 Progress

The Progress section tracks real learning activity.

Possible measurements include:

* Lessons completed
* Vocabulary learned
* Exercise accuracy
* Study time
* Listening practice
* Speaking practice
* Writing practice
* Learning streak
* Common mistakes

Skill areas:

```text
Reading
Listening
Speaking
Writing
Vocabulary
Grammar
```

Progress values should come from actual user activity rather than fabricated statistics.

---

# 🎤 Speaking & Conversation

A future version of the application will support speaking practice.

The user can:

1. Listen to a target sentence.
2. Record their response.
3. Convert speech to text.
4. Compare the response with the target.
5. Receive useful feedback.
6. Save recurring mistakes.

The application can also provide AI conversation scenarios such as:

* Café
* Travel
* University
* Shopping
* Job interview
* Daily conversation
* Self introduction

At the end of a conversation, the system can provide feedback on:

* Vocabulary
* Grammar
* Repeated mistakes
* Useful expressions
* Suggested review topics

---

# 🔊 Text-to-Speech

Spoken content should be available throughout the application.

Possible controls:

```text
▶ Play
⏸ Pause
↻ Replay

0.75×   1×   1.25×
```

Audio can be provided for:

* Vocabulary
* Example sentences
* Stories
* Jokes
* AI conversation responses

Generated audio should be cached and reused rather than regenerated every time.

---

# 🌍 Language-Specific Experience

The interface can change slightly according to the selected language.

### 🇬🇧 English

Use a subtle British-inspired visual atmosphere:

* London/UK-inspired architecture
* Books
* Classrooms
* Cultural elements

Also provide an educational section such as:

**English Around the World**

Examples:

* United Kingdom
* United States
* India
* Canada
* Australia
* New Zealand
* Ireland

The visual design should not imply that English belongs only to Britain.

### 🇩🇪 German

Use a subtle Central European/German visual atmosphere and provide information about places where German is spoken.

### 🇫🇷 French

Use a subtle French visual atmosphere and provide information about major French-speaking countries and regions.

---

# 🧑‍🏫 AI-Generated Learning Characters

The Learn section can use friendly AI-generated human characters to make the learning experience more engaging.

Characters should be:

* Educational
* Friendly
* Human-looking
* Consistent with the selected language environment
* Visually modern

Images should be generated/stored once and reused rather than generated on every page load.

Large images should be optimized and lazy-loaded to reduce page load time.

---

# ⚡ Performance Goals

The application should prioritize performance, especially on mobile devices.

Important principles:

* Avoid unnecessary re-renders.
* Avoid repeated API calls.
* Cache reusable data.
* Lazy-load large images.
* Optimize images to modern formats where practical.
* Fetch only data needed for the current page.
* Avoid expensive AI calls during every render.
* Use server-side rendering/data fetching where appropriate.
* Use client components only when interactivity requires them.
* Show skeleton loading states for genuinely asynchronous content.

The application should not feel like a static prototype with slow interactions.

---

# 📱 Mobile First

The application is designed primarily for mobile use.

The interface should work comfortably around:

* 360px
* 390px
* 430px

Requirements:

* Touch-friendly buttons
* Readable text
* No horizontal scrolling
* Easy audio controls
* Responsive lesson layouts
* Mobile navigation
* Fast page transitions

Desktop layouts should be supported as well.

---

# 🛠️ Suggested Technology Stack

### Frontend

* Next.js
* React
* TypeScript
* Tailwind CSS

### Backend

* Next.js server/API routes or a dedicated backend such as FastAPI

### Database

* PostgreSQL

### ORM

* Prisma

### Validation

* Zod

### State Management

* Zustand

### Forms

* React Hook Form

### AI

Provider-independent LLM integration.

### Audio

Provider-independent:

* Text-to-Speech (TTS)
* Speech-to-Text (STT)

The AI, TTS, and STT providers should be separated from the application logic so they can be replaced later.

---

# 🗂️ Suggested Project Structure

```text
language-practice/
│
├── app/
│   ├── page.tsx
│   ├── learn/
│   ├── practice/
│   ├── review/
│   ├── stories/
│   ├── jokes/
│   └── progress/
│
├── components/
│   ├── ui/
│   ├── lessons/
│   ├── exercises/
│   ├── audio/
│   ├── speaking/
│   └── dashboard/
│
├── lib/
│   ├── ai/
│   ├── audio/
│   ├── speech/
│   ├── content/
│   ├── review/
│   └── database/
│
├── prisma/
│   └── schema.prisma
│
├── public/
│   ├── images/
│   └── audio/
│
├── types/
│
├── .env.example
├── package.json
└── README.md
```

---

# 🗄️ Core Data Models

The application can use models such as:

```text
User
Language
UserLanguage
SourceMaterial
ContentChunk
Lesson
Vocabulary
UserVocabulary
Exercise
ExerciseAttempt
StudySession
Mistake
ConversationSession
ConversationMessage
AudioAsset
```

These models allow the application to remember the learner and personalize future practice.

---

# 🔐 Environment Variables

Create a `.env` file based on `.env.example`.

Example:

```env
DATABASE_URL="your-postgresql-connection-string"

LLM_API_KEY="your-llm-api-key"

TTS_API_KEY="your-tts-api-key"

STT_API_KEY="your-stt-api-key"
```

Never commit real API keys to GitHub.

---

# 🚀 Getting Started

## 1. Clone the repository

```bash
git clone <your-repository-url>
cd language-practice
```

## 2. Install dependencies

```bash
npm install
```

## 3. Configure environment variables

Create:

```text
.env
```

and add the required configuration.

## 4. Generate Prisma client

```bash
npx prisma generate
```

## 5. Run database migrations

```bash
npx prisma migrate dev
```

## 6. Start the development server

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

---

# 🧪 Development Principles

This project should follow these rules:

### No fake interactions

Buttons should perform real actions.

### No fabricated progress

Progress statistics should come from real user activity.

### No unnecessary AI calls

Do not call the LLM every time a component renders.

### Source-grounded learning

Uploaded teaching material should be used as the primary source when generating lessons.

### Modular AI providers

The app should not be tightly coupled to one AI/TTS/STT provider.

### Mobile-first

Every feature should work on a phone before being considered complete.

---

# 🛣️ Development Roadmap

## Version 1 — Foundation

* [ ] Language selection
* [ ] Level selection
* [ ] User profile
* [ ] Database
* [ ] Basic navigation
* [ ] Mobile UI

## Version 2 — Learning

* [ ] Upload TXT/PDF/DOCX
* [ ] Source-material processing
* [ ] Lesson generation
* [ ] Vocabulary
* [ ] Grammar
* [ ] Exercises

## Version 3 — Audio

* [ ] Text-to-Speech
* [ ] Audio player
* [ ] Slow playback
* [ ] Cached audio

## Version 4 — Review

* [ ] Vocabulary review
* [ ] Spaced repetition
* [ ] Exercise history
* [ ] Mistake tracking

## Version 5 — Speaking

* [ ] Voice recording
* [ ] Speech-to-text
* [ ] Speaking exercises
* [ ] Pronunciation feedback

## Version 6 — AI Tutor

* [ ] Conversation mode
* [ ] Real-world scenarios
* [ ] Personalized corrections
* [ ] Adaptive recommendations

## Version 7 — Advanced Personalization

* [ ] Adaptive curriculum
* [ ] Weak-topic detection
* [ ] Personalized stories
* [ ] Personalized conversations
* [ ] Long-term learning analytics

---

# 🎯 Project Goal

The long-term goal is to build a language-learning platform where the learner does not simply **read AI-generated explanations**, but actively:

```text
READ
 ↓
LISTEN
 ↓
UNDERSTAND
 ↓
PRACTICE
 ↓
SPEAK
 ↓
MAKE MISTAKES
 ↓
GET FEEDBACK
 ↓
REVIEW
 ↓
IMPROVE
```

The user's own learning material provides the foundation, while AI, audio, interactive exercises, and adaptive review turn that material into a personalized learning experience.

---

## 📌 Current Status

**Project:** Language Practice App
**Languages:** German 🇩🇪 · French 🇫🇷 · English 🇬🇧
**Status:** In Development
**Primary Goal:** Build a functional, personalized, mobile-first language-learning application.
