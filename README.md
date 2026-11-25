# PCAP Lessons

**Live site: https://zeeviiii.github.io/pcap-lessons/**

A study site I use to prepare for the **PCAP-31-04** exam (Certified Associate Python Programmer, Python Institute).
The lessons are in Hebrew, and all code is in English. It works on phone, tablet and desktop.

This is the backup copy of my main study app. I designed and tested it with Claude (Anthropic's AI assistant).

## Features

- **22 short lessons, 120 questions.** Every lesson opens with an explanation: a concept, a code example and its real output. Short questions follow.
- **Hints in two steps** for every question, and an explanation after each answer that names the common trap.
- **"Choose two" questions**, like in the real exam.
- **Mock exam:** 42 questions in 65 minutes, split by topic the same way as the real exam, with a 72% pass mark and a score per topic.
- **Spaced review:** a wrong answer comes back the same day, then after 1, 3 and 7 days.
- **"10 minutes today":** 5 mixed questions for a short break.
- **"Where I stand":** accuracy per topic, an estimated score and a recommended next lesson.
- **PDF for every lesson**, for offline reading and printing.
- **Progress transfer:** copy a code on one device and paste it on another.

## Topics (weights from the official syllabus)

| Section | Exam weight | Lessons | Questions |
|---|---|---|---|
| Modules and packages | 12% | 3 | 14 |
| Exceptions | 12% | 4 | 20 |
| Strings | 9.5% | 2 | 12 |
| Object-oriented programming | 28.5% | 5 | 27 |
| Advanced topics and files | 24% | 5 | 29 |
| Testing, teamwork and AI | 14% | 3 | 18 |

## How it is built

- One self-contained `index.html`, with plain JavaScript and CSS and no framework.
- Progress is saved in the browser (`localStorage`). Stored data is validated on load, so a damaged copy cannot break the page.
- Every code example and every "what is printed?" answer was checked by running it in Python.
- The site was tested with Playwright: every lesson and question, the mock exam (including timeout), review, progress transfer, a 320px phone width, dark mode, and 600 random clicks.
- `pdf/` holds one PDF per lesson, generated with Chromium.

## Notes

- Progress is stored only in the browser you use. To move it, use **"העברת התקדמות"** (progress transfer) on the home page.
- On Safari, add the site to the Home Screen so the browser does not clear its data after 7 days without a visit.
