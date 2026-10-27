---
name: it-curriculum-builder
description: Build complete, progressive IT training curricula (Beginner → Intermediate → Professional) for networking, infrastructure and cybersecurity courses — with lesson objectives, simple explanations, analogy and technical diagrams, real-world examples, hands-on labs, quizzes and trainer notes, delivered as a trainer document plus a slide deck, in English or Egyptian colloquial Arabic. Use this skill whenever an IT trainer or instructor asks to design, plan, outline or write a course, curriculum, syllabus, training program, منهج, كورس, دورة, or lesson plan on networking, CCNA, servers, Linux/Windows Server, data center, firewalls, SOC, pentesting, Security+ or any related IT topic — even if they only give a topic and a number of hours, or only ask for "lessons" or "slides for my students".
---

# IT Curriculum Builder

Turns a topic + duration + student profile into a full, ready-to-teach IT curriculum that climbs from zero knowledge to professional level. The trainer should be able to walk into class with the slides and teach from the document without rewriting anything.

The audience is students, often with no background, so every choice below serves one goal: **each new idea must stand on something the student already understood.** That is why the curriculum is staged, why every concept gets a picture, and why beginner lessons lean on everyday analogies before any jargon.

## Step 1 — Collect the inputs

The trainer usually gives three things. Extract them from the request; ask only for what is missing, in one short message (use multiple-choice questions if the tool exists):

| Input | Example | Default if not given |
|---|---|---|
| Topic / track | "CCNA networking", "SOC analyst", "Linux server admin" | — must ask |
| Total duration | "40 hours", "6 weeks, 2 sessions/week, 3h each" | ask; if trainer says "you decide", use 30 h |
| Student profile | "university students, no experience" | assume complete beginners |
| Presentation language | English or Egyptian Arabic (عامية مصرية) | match the language of the request |

Also note any constraints the trainer mentions (lab equipment available, Packet Tracer vs real devices, online vs classroom, target certificate).

## Step 2 — Design the curriculum map, then pause for approval

Before writing lessons, build the skeleton and show it to the trainer. Full lesson content is long and expensive to redo, so getting the structure right first saves everyone time.

**The three levels** — every curriculum uses exactly these:

1. **Beginner (مبتدئ)** — what it is and why it matters. Concepts through analogies, basic terms, guided labs.
2. **Intermediate (متوسط)** — how it works and how to configure it. Real commands, standard configurations, troubleshooting common problems.
3. **Professional (محترف)** — design, scale, security and real-world operations. Multi-component scenarios, best practices, performance and failure analysis.

**Splitting the hours** — start from 40% / 35% / 25% and adjust:
- Students with zero background and short course (< 20 h) → spend more on Beginner (≈50/35/15) and say so.
- Students who already have basics → shrink Beginner (≈20/40/40).
- Each level ends with a level checkpoint (mini-project or assessment) before moving up.

**Certification mapping** — map each level to the most relevant certificate where one exists. Read `references/tracks-and-certs.md` for the module progression and certificate mapping of the networking, infrastructure and security tracks. Exam codes change over time; if web search is available, confirm the current exam version before writing it into the curriculum.

**Show the map** as a compact table: Level → Modules → Lessons (titles) → Hours → Linked certificate. Then ask: "Is this structure OK, or do you want to change anything before I write the full lessons?" Wait for the answer (if the trainer isn't present or said "just do it", continue and state the assumptions at the top of the document).

## Step 3 — Write each lesson

Every lesson follows the same structure so students know what to expect and the trainer can scan quickly. Read `references/lesson-template.md` for the exact template and a worked example.

Each lesson contains:
1. **Learning objectives** — 3–4 measurable outcomes ("By the end, you can configure a VLAN on a switch"), not vague ones ("understand VLANs").
2. **Explanation** — short paragraphs, one idea at a time. Define a term the first time it appears.
3. **Diagram** — at least one per lesson (see Step 4).
4. **Real-world example** — a situation from a real company, home or campus network that shows why this matters.
5. **Hands-on lab** — goal, tools needed, numbered steps, expected result, and a "what if it doesn't work" hint. Prefer free tools (Cisco Packet Tracer, GNS3, VirtualBox, Kali/Ubuntu VMs, TryHackMe free rooms) unless the trainer named their equipment.
6. **Quick quiz** — 3–5 questions (multiple choice and short answer) with an answer key.
7. **Trainer notes** — common student mistakes, timing tips, questions to ask the class, and how to explain the idea differently if students get stuck.

Keep the difficulty honest per level: a Beginner lab is guided step by step; a Professional lab gives the goal and constraints and lets students design the solution.

## Step 4 — Diagrams

Diagrams are the heart of this skill: most students understand a picture before they understand the words. Use **both styles**, chosen by level:

- **Beginner → analogy diagram.** Show the concept as an everyday scene, labeled with the technical term. Router = post office sorting letters; IP address = home address; firewall = building security guard checking IDs; VLAN = separate floors in one building.
- **Intermediate and Professional → technical diagram.** Real topology or flow: devices, interfaces, IP ranges, VLAN IDs, packet path, attack chain.
- When a Beginner concept reappears at a higher level, show the analogy again briefly next to the technical diagram — it links the new detail to what the student already knows.

Read `references/diagrams.md` for how to draw them (SVG/Mermaid), the visual style rules, and how to embed them in documents and slides.

## Step 5 — Language

Read `references/language-guide.md` before writing. In short:
- **English** — plain, short sentences, no unnecessary jargon.
- **Egyptian Arabic (عامية مصرية)** — friendly classroom tone, right-to-left layout, but **technical terms stay in English** (Router, VLAN, IP Address, Firewall) because that is what students will see on devices, in exams and at work. Commands and configuration are always in English.

## Step 6 — Produce the deliverables

Two outputs, both from the same content:

1. **Trainer document** — the full curriculum: cover, course overview, curriculum map table, then every lesson in the Step 3 structure, level checkpoints, and a final project. Answer keys and trainer notes live here.
2. **Slide deck** — for teaching in class: one title slide per level, then per lesson about 5–8 slides (objectives → concept + diagram → example → lab steps → quiz). Slides carry the diagrams and few words; the explanation stays in the document and the trainer's voice. No answer keys on slides.

Format choice: if the environment offers Claude's own document and slide artifact types (Docs / Slides), use them — the trainer can edit and export to Word, PDF or PowerPoint. If the trainer explicitly asks for Word / PowerPoint / PDF files, or no artifact types exist, use the docx and pptx skills. For Arabic output, make sure the layout is RTL in both deliverables.

For long curricula, build in stages: write and deliver Level 1 first, then Levels 2 and 3, so the trainer can react early. Tell the trainer when each level is ready.

## Step 7 — Check before delivering

Go through this quickly:
- Every lesson has all 7 parts, and at least one diagram.
- Lesson order never uses a concept before it was taught (e.g., no subnetting before IP addressing).
- Hours in the map add up to the total duration.
- Commands and configuration are syntactically correct for the stated platform (Cisco IOS, Linux distro, Windows Server version).
- Quiz answers match the lesson content.
- Arabic version: technical terms in English, RTL layout, consistent Egyptian tone.

Then hand over both deliverables with one line each, and offer one useful next step (e.g., "Want me to build a final exam bank or a Packet Tracer lab file list?").
