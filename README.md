# MT-I Online Class Test — Non-Traditional Machining

Online, proctored class test for **Manufacturing Technology – I**
Topics: Ultrasonic Machining · Chemical Machining · Electric Discharge Machining · Laser Beam Machining
Mapping: **CO5 · ILO9** · 20 marks · 45 minutes

## Features
- **Login page** (name, roll no., registration no., semester, branch) → **instructions & integrity pledge** → **test** → **result page**
- Question pattern (20 marks):
  | Section | Format | Marks |
  |---|---|---|
  | A | 10 MCQs × 1 | 10 |
  | B | 5 Fill in the blanks × 1 | 5 |
  | C | 2 schematic figures (USM set-up, EDM RC circuit) × 5 parts × 0.5 | 5 |
- Questions drawn at random from topic pools, **question order and MCQ options shuffled** per student
- **One question at a time**, question palette, mark-for-review, clear response, 45-min timer with auto-submit
- **Anti-cheat:** full-screen enforced, tab switch / window blur, mouse leaving the window, copy/paste/right-click/print/PrtSc/DevTools shortcuts blocked, reload keeps the timer running, name + roll watermark, auto-submit after 3 violations, one attempt per roll no. per device
- **Result page** with score, section-wise and topic-wise analysis
- **Professional PDF report** (student details, CO/ILO, score, integrity log, question-wise responses, figures, declaration, signature boxes for student and class teacher)

## Host on GitHub Pages
1. Create a new repository on GitHub (e.g. `mt1-ntm-test`).
2. Upload **all files keeping the folder structure**: `index.html`, `lib/`, `.nojekyll`, `README.md`.
3. Repository → **Settings → Pages** → Source: *Deploy from a branch* → Branch `main`, folder `/ (root)` → Save.
4. After a minute the test is live at `https://<your-username>.github.io/mt1-ntm-test/`. Share this link with students.

No server, database or internet CDN is needed — the PDF libraries are bundled in `lib/`.

## Customise
Open `index.html` and edit the `CONFIG` block (search for `CONFIGURATION`):
- `institute`, `department`, `faculty`, `course`, `assessmentTitle`
- `coText`, `iloText` — replace with the exact CO5 / ILO9 statements from your syllabus
- `durationMin`, `maxViolations`, `countCursorLeave`
- `showAnswerKeyInReport` — set `true` to print correct answers in the PDF (keep `false` while other students are still writing)
- `quota` — how many questions per topic are drawn from the pools

Questions are in the `BANK` block — add or edit MCQs, blanks and accepted answers there.

## Notes for the teacher
- Ask students to submit the **signed printed PDF**; check the Attempt ID, score and violation log on it.
- To allow a re-test on the same computer, clear that site's data in the browser (Settings → Privacy → Site data).
- Phones: Android Chrome supports full screen. iPhone Safari does not, so the test runs without it there (this is noted in the report); laptops/desktops are recommended.
- Limitation: a static site cannot hide the answer key from a determined student who reads the page source on another device. The anti-cheat measures deter and log misconduct; supervise the lab for high-stakes use.
