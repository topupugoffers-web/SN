# SN

I think this is a great project. For your specific work (Excel, emails, CRM updates, student applications), I'd build it in phases so you get something useful within a few weeks instead of trying to build "Jarvis" all at once.

Project: Local AI Desktop Assistant
Goal

An AI that sits in the background, watches how you work, learns your routines, and gradually automates repetitive office tasks—all running primarily on your own PC.

Phase 1 — Desktop Observer (Week 1)

The AI doesn't talk or automate yet. It only watches.

Desktop Assistant
│
├── Screen Capture
├── OCR
├── Active Window
├── Mouse Position
├── Keyboard Events
└── Local Database
It records things like:
09:00
Chrome opened

09:02
Gmail opened

09:05
Downloaded CAS Letter

09:06
Excel opened

09:08
Student status changed

No AI yet.

Just collecting data.

Phase 2 — Memory Engine (Week 2)

Instead of screenshots, convert everything into events.

Example:

{
 "time":"09:08",
 "application":"Excel",
 "action":"Updated Student Status",
 "student":"ABC123"
}

Save everything into SQLite.

Now your PC begins building memories.

Phase 3 — Tiny Local AI (Week 3)

Install a lightweight model.

Examples

Qwen 3 4B
Gemma 3 4B
Llama 3.2 3B

Now the AI can answer questions like

What have I done today?

or

Which student files haven't been processed?

Phase 4 — Pattern Detection (Week 4)

The AI notices things like

Download CAS

↓

Update Excel

↓

Update CRM

↓

Send Email

After seeing this 15 times

it saves

Workflow #12

CAS Processing
Phase 5 — Suggestions

Instead of controlling your PC

it asks

I noticed you're processing a CAS.

Would you like me to

✓ Update CRM

✓ Draft Email

✓ Move PDF

?

You press

YES

Phase 6 — Automation

The AI performs

Mouse Clicks

Keyboard

Open Programs

Move Files

Excel Updates

Emails

Everything locally.

Phase 7 — Learning

Now the AI starts remembering things forever.

Example

User always writes

"Kind Regards,
BPP Visa Team-HK"

at the end of emails.

It remembers.

Phase 8 — Personal Assistant

Eventually

Good morning.

Today's work

18 pending students

4 refunds

2 CAS

7 interview bookings

Would you like me to start?
Software Stack
Language

Python

Reason:

Huge AI ecosystem
Excellent automation libraries
Cross-platform
Local AI
Ollama

Runs

Gemma
Qwen
Llama

with one command.

OCR
PaddleOCR

Reads

Excel

Emails

PDF

Websites

Screen Capture
mss

Fast

Very lightweight

Automation
PyAutoGUI

Playwright

pywinauto

Can

Click

Type

Open programs

Fill forms

Memory
SQLite

Stores

Actions

Habits

Workflows

History


No server required.

Voice (optional)
Whisper

+

Piper

Offline.

Folder Structure
AI-Assistant/

│

├── observer/

│      screen.py

│      keyboard.py

│      mouse.py

│

├── ai/

│      local_ai.py

│      memory.py

│      planner.py

│

├── automation/

│      excel.py

│      browser.py

│      email.py

│

├── database/

│      assistant.db

│

├── logs/

│

└── app.py
Estimated Resource Usage
Component	RAM	CPU
Screen Watcher	150 MB	2%
OCR	300 MB	5%
Tiny AI Model	4–8 GB	10–20% (higher only while generating)
SQLite	Negligible	0%
Automation	Negligible	1%

Total

RAM

≈ 8–10 GB

CPU

≈ 10%

Future Features

Imagine six months from now:

Morning!

Today's schedule

12 CAS

5 Refunds

8 Interview Bookings

3 Offer Letters

I already:

✓ Downloaded attachments

✓ Updated Excel

✓ Sorted documents

Drafted 8 emails.

Would you like to review them?

You spend your time reviewing and approving instead of repeating mechanical work.

One enhancement I'd recommend

Instead of relying only on a language model to "learn," create a workflow engine alongside it. The workflow engine records actions as structured events (e.g., "opened Excel," "updated row," "sent email") and detects repeated sequences. The language model then explains those workflows, answers questions about them, and helps generalize them. This combination is more reliable, uses less compute, and learns repetitive office tasks much faster than asking the AI to infer everything from screenshots alone
