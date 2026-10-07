# Study BOX

### ./One Question. A Complete Study Kit.

**HackForge Theme:** 🌍 Open Innovation

**Status:** Working prototype (Binary Search Tree demo)

**Live Demo:** https://<your-username>.github.io/study-box/

---

# 1. Problem Statement

## The Problem

Students study every day, but one question usually means many steps:

- Search the topic
- Read a long text answer
- Look for diagrams
- Find a video
- Make notes or slides

The difficulty is not finding an answer.

The difficulty is **understanding** it quickly and in the right format.

Most chatbots reply with plain text in a casual style. Students still have to collect visuals, videos and slides on their own.

### ./Who Experiences This Problem?

- School and college students
- Self-learners preparing for exams
- Teachers who need quick slides
- Study groups sharing material

### ./Why Is It a Problem?

When learning feels slow and scattered:

```text
Question
   ↓
Text-only reply
   ↓
Search videos and diagrams
   ↓
Make notes and slides
   ↓
Lost time, less understanding
```

The challenge is therefore not simply **getting answers**.

It is:

> How can one question return everything a student needs to understand the topic?

---

# 2. Existing Solutions

## Search Engines

Return links and pages.

**Limitation:** The student collects and sorts everything alone.

## AI Chatbots

Give fast text answers.

**Limitation:** Mostly text, often casual, and not exam-ready.

## Video Platforms

Offer visual lessons.

**Limitation:** Not tailored to the exact question asked.

## Note and Slide Tools

Help organise and present content.

**Limitation:** The student must create the content.

## Identified Gap

Most tools give **one format**.

> Study BOX delivers every format from one question.

---

# 3. Proposed Solution

## Study BOX

Study BOX is an AI study chatbot that turns every question into a **complete study kit**.

```text
Student Question
      ↓
Formal Answer
      ↓
Visuals and Graphs
      ↓
Matching Video
      ↓
Auto-generated PPT
      ↓
Quick Quiz
```

### ./The Core Idea

Instead of:

> "Search, read, watch and make notes separately."

Think:

> "Ask once and get everything."

The question remains the objective. Study BOX adds visuals, video, slides and a quiz around the answer.

---

# 4. Key Features

## 1. Formal Answers

Textbook-style, structured explanations instead of casual chat text.

## 2. Visuals and Graphs

Diagrams and charts generated for the topic.

## 3. Interactive Diagrams

Students can try the concept hands-on (for example, insert and search in a Binary Search Tree).

## 4. Video Lessons

A matching YouTube video for the same topic.

## 5. Auto-generated PPT

Slides prepared from the answer.

## 6. Quick Quiz

Questions at the end to check understanding.

## 7. Typo-Friendly Input

Understands misspelled questions such as "BINEARY SEAECH TREE".

## 8. Syllabus-Aware Answers *(planned)*

Answers tailored to a student's course.

---

# 5. Technical Approach

## System Overview

```text
              USER
                │
                ▼
      Web UI (HTML / CSS / JS)
                │
                ▼
        Backend API (FastAPI)
                │
     ┌──────────┼──────────┐
     ▼          ▼          ▼
 Answer      Visual      Media
 Engine      Engine      Engine
(Gemini)   (Diagrams,   (YouTube,
            Graphs)      PPT, Quiz)
```

## Answer Engine

Uses the Gemini API to detect the topic and write a formal, structured answer.

## Visual Engine

Creates diagrams, graphs and interactive demos for the topic.

## Media Engine

Finds a matching video, builds the slides and prepares the quiz.

---

# 6. Technology Stack

| Layer | Technology |
|-------|------------|
| Frontend | HTML, CSS, JavaScript |
| Backend | Python, FastAPI |
| AI | Google Gemini API |
| Video | YouTube search |
| Output | PPT generation |

---

# 7. Live Demo

Try the prototype in your browser (no setup needed):

**https://<your-username>.github.io/study-box/**

### ./What To Try

1. Press **Ask** with the prompt `i want to learn binary search tree`
2. Insert and search numbers in the interactive tree
3. Read the formal answer, view the graph, open the video, flip the slides and take the quiz

> The demo page lives in the `docs/` folder and is served with GitHub Pages.

---

# 8. Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/study-box.git
cd study-box

# 2. Install dependencies
pip install -r requirements.txt

# 3. Add your Gemini API key
export GEMINI_API_KEY="your_key_here"

# 4. Run the server
uvicorn main:app --reload
```

Then open `http://localhost:8000` in your browser.

### ./Try This Prompt

```text
i want to learn binary search tree
```

---

# 9. Limitations and Future Scope

## Current Limitations

- AI answers need accuracy checks
- Auto-made visuals can vary in quality
- Video match depends on search results
- The demo currently covers one topic (Binary Search Tree)

## Future Scope

- Syllabus-aware answers
- Regional language support
- Progress and weak-topic tracking
- Downloadable PPT inside the app

---

# 10. License

Released under the [MIT License](LICENSE).
