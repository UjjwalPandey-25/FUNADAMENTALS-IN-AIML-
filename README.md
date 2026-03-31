# FUNADAMENTALS-IN-AIML-
StudyDesk — Terminal-Based Smart Student Task Manager
# 📚 StudyDesk — Terminal-Based Smart Student Task Manager

> A lightweight, offline, zero-dependency CLI task manager built entirely with Python's standard library.

![Python](https://img.shields.io/badge/Python-3.7%2B-blue?style=flat-square&logo=python)
![Dependencies](https://img.shields.io/badge/Dependencies-None-brightgreen?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

---

## 📖 About

Students often struggle to manage multiple assignments, deadlines, and exams — tasks get scattered across notebooks, WhatsApp chats, and memory, leading to missed deadlines and reduced productivity.

**StudyDesk** solves this with a fast, distraction-free terminal interface. No internet, no installations, no frameworks — just Python.

---

## ✨ Features

| Feature | Description |
|---|---|
| ➕ Add Tasks | Title, subject, type, priority, deadline, and notes |
| 📋 View Tasks | Colour-coded list sorted by urgency |
| ✅ Mark Done | Toggle tasks complete / incomplete |
| 🗑 Delete Tasks | Remove tasks with confirmation prompt |
| 🔍 Search | Filter by title or subject |
| 📊 Stats Bar | Live counts — Total, Pending, Overdue, Due Today, Done |
| ⏰ Reminders | Automatic alerts for overdue and today's tasks |
| 💾 Persistent Storage | Tasks saved to `studydesk_tasks.json` |

---

## 🖥️ Sample Output

```
══════════════════════════════════════════════════════════════════════════════
                       📚  S T U D Y D E S K  📚
                    Smart Task Manager for Students
                       Tuesday, 31 March 2026   10:41
══════════════════════════════════════════════════════════════════════════════
       5              4              2              1              1
     Total          Pending        Overdue       Due Today        Done
──────────────────────────────────────────────────────────────────────────────
  Filter: ALL

  1. ✘ OVERDUE  HIGH  Physics Chapter 5 Assignment [Physics] Assignment
       Deadline: 2d overdue   ID:1

  2. ✘ OVERDUE  HIGH  Math Integral Calculus Test [Maths] Exam
       Deadline: 5h overdue   ID:2
       Notes: Chapters 6-9, bring calculator

  3. ⏰ TODAY    MED   History Essay Submission [History] Project
       Deadline: 2h left   ID:3
       Notes: Min 1500 words, MLA format

  4. ○ SOON     MED   Read Shakespeare Act 3 [English] Reading
       Deadline: Tomorrow 10:40   ID:4

  5. ✔ DONE     LOW   Biology Diagram Labelling [Biology] Assignment
       Deadline: 10h overdue   ID:5

  ⚠️  2 OVERDUE task(s):
      • Physics Chapter 5 Assignment
      • Math Integral Calculus Test

  ⏰  1 task(s) due TODAY:
      • History Essay Submission  (13:40)

──────────────────────────────────────────────────────────────────────────────
  [A] Add new task   [D] Mark done/undo   [X] Delete task
  [F] Change filter  [S] Search           [R] Refresh   [Q] Quit
──────────────────────────────────────────────────────────────────────────────
  →
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.7 or higher
- Any terminal / command prompt

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/studydesk.git

# 2. Navigate into the folder
cd studydesk

# 3. Run the app
python studydesk.py
```

No `pip install` needed. It just works.

---

## 🎮 How to Use

| Key | Action |
|-----|--------|
| `A` | Add a new task |
| `D` | Mark a task as done / undo |
| `X` | Delete a task |
| `F` | Change filter (All / Active / Overdue / Today / Soon / Done) |
| `S` | Search tasks by title or subject |
| `R` | Refresh / clear search |
| `Q` | Quit |

### Adding a Task

```
  Task / Assignment title: Physics Lab Report
  Subject: Physics
  Type (Assignment/Exam/...): Assignment
  Priority (high/medium/low) [medium]: high
  Deadline [2026-04-02 23:59]: 2026-04-03 17:00
  Notes: Include error analysis section

  ✅  Task added successfully!
```

### Deadline Formats Accepted

```
2026-06-15 14:00      → Full date and time
2026-06-15            → Date only (defaults to midnight)
15/06/2026 14:00      → DD/MM/YYYY with time
15/06/2026            → DD/MM/YYYY only
```

---

## 🗂️ Project Structure

```
studydesk/
│
├── studydesk.py           # Main application
├── studydesk_tasks.json   # Auto-created task data file
└── README.md              # This file
```

---

## ⚙️ How It Works

The app follows standard **CRUD operations** on a local JSON file:

```
Create  →  Add new task (saved to JSON)
Read    →  View / filter / search tasks
Update  →  Mark task done or undone
Delete  →  Remove task permanently
```

### Core Modules Used

| Module | Purpose |
|--------|---------|
| `json` | Save and load tasks from disk |
| `datetime` | Deadline parsing and countdown |
| `os` | Terminal width detection and screen clear |
| `pathlib` | Cross-platform file path handling |
| `re` | Strip ANSI codes for alignment |

---

## 🔬 Algorithm

```
1. Start program
2. Load tasks from studydesk_tasks.json (if exists)
3. Display colour-coded task list with stats
4. Show reminder alerts for overdue / today's tasks
5. Accept menu input from user:
     A → Collect task details → Save to file
     D → Toggle done status  → Save to file
     X → Confirm → Remove    → Save to file
     F → Update active filter
     S → Set search query
     Q → Exit
6. Repeat from step 3
```

---

## 🛣️ Future Enhancements

- [ ] Desktop / system notifications for deadlines
- [ ] Export tasks to PDF or CSV
- [ ] Cross-platform sync via cloud
- [ ] Recurring tasks (weekly assignments)
- [ ] Subject-wise progress report

---

## 📚 References

- [Python Official Documentation](https://docs.python.org/3/)
- [W3Schools Python Tutorial](https://www.w3schools.com/python/)
- [GeeksforGeeks Python](https://www.geeksforgeeks.org/python-programming-language/)
- [FreeCodeCamp Python Guide](https://www.freecodecamp.org/)

---

## 📄 License

This project is licensed under the **MIT License** — free to use, modify, and distribute.

---

<p align="center">Made with ❤️ for students, by a student.</p>
