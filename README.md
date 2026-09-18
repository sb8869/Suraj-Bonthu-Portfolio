# Welcome! I'm Suraj Bonthu.
🌐 [Portfolio](https://surajbonthu.vercel.app/) | 📄 [Resume](https://github.com/user-attachments/files/30668418/Suraj_Bonthu_Resume.pdf)
 | 💼 [LinkedIn](https://www.linkedin.com/in/suraj-bonthu/)

A software engineer with a passion for building things people actually enjoy using — whether that's a slick React component, a computer vision pipeline, or an AR drawing experience. I've shipped production code at CarGurus, rebuilt landing pages for video games, and taken projects from zero to deployed across the full stack. My work spans web apps, game mods, and research — because I think the best engineers stay curious across domains. I'm at my best when craft meets complexity: turning hard problems into clean, interactive experiences.

## Work Experience

### SMT TechHub LLC
Software Engineer Intern | Feb 2026
- Engineered modular React components for a flagship CRM product, improving the reusability of the UI library and accelerating the front-end development cycle.
- Developed dynamic dashboard features using JavaScript (ES6+), enabling real-time data visualization of customer interactions and sales pipelines.
- Integrated RESTful APIs and third-party services into the React front-end to streamline lead management and external data.

### CarGurus
Software Engineer Intern | July - Dec 2022
- Developed Showroom, an internal tool used company-wide to manage service/job/system data.
- Led front-end development for a new feature allowing users to add/edit service configurations.
- Built and optimized React.js components to improve performance and user experience.
- Increased code coverage to 80% by implementing tests using React Testing Library.
  
### Changeling
Web Developer | May - August 2021
- Worked with a team of seven web developers to create an interactive website for the Changeling VR game.
- Responsible for redesigning and creating the landing page using Vue.js.
- Worked on overall site maintenance and managed several dependencies to help with the performance of the website.
- Link: https://www.changelingvr.com/

## Certifications

### AWS Certified Solutions Architect - Associate
https://www.credly.com/badges/fc8e1a8b-a230-42e1-ba8d-1d2b252e3b96/linked_in_profile

## Projects

### Glitch Lab - Don't lower the difficulty. Find the bug.
Diagnostic Math Game & Bayesian Inference Engine | 2026
- About: Glitch Lab is a K–5 math game that works out which broken arithmetic procedure a child is running, instead of concluding they're "bad at subtraction" and serving them easier sums. A child who writes 40 − 27 = 27 isn't guessing — they're running a consistent rule (take the smaller digit from the larger one, every column) and they'll run it again tomorrow. Standard adaptive systems read that as "wrong answer, lower difficulty," which is backwards: that child doesn't need easier problems, they need the bug named. Grounded in Brown & Burton's BUGGY (1978) and VanLehn's repair theory.
- The diagnosis loop: The child meets a robot that does math wrong and a suspect board holding one card per rule it might be running — thirteen broken procedures plus "nothing is wrong at all." Each card displays what that rule writes, so the evidence is checkable by a five-year-old. The child picks which problem to test the robot with, the robot answers wrong, and every card that would have written something different is crossed off. A single well-chosen question routinely eliminates thirteen of the fourteen.
- Mutual diagnosis: The child has to answer each test problem themselves before the board narrows — you can't spot a deviation from a rule you don't know. Those answers feed a second posterior over the same fourteen hypotheses, pointed at the child. The same engine runs in both directions; only one of them is visible.
- The inference engine: Each of the thirteen misconceptions is an executable function, not a label — applies(item) says whether the bug fires, compute(item) returns exactly what a child running it would write. The posterior is Bayes with a slip-and-guess likelihood, floored so nothing is ever eliminated outright, and the next problem is chosen by expected information gain. There is no LLM anywhere in the inference path: auditable, reproducible, offline, zero per-session cost, and incapable of hallucinating a diagnosis.
- Measured, not asserted: 500 simulated students at a 10% slip rate, identical students in both arms, evaluated on a hand-verified 37-item bank the game itself never draws from — 98.8% identified the exact misconception against 79.0% for a difficulty-ladder baseline, in 4.35 questions against 9.73. McNemar χ² = 89.92, 1 df.
- Remediation that shows the working: Once the rule is named, the app replays both procedures column by column — every borrow and carry, the robot's method beside the correct one, with the digit where they diverge lit up. Every number is computed by the same bug object the diagnosis used; a validator extracts each arithmetic claim in the generated copy and checks it against engine-computed truth, for all thirteen bugs, in the test suite.
- Mastery, not streaks: Three correct in a row moves a robot to probation, never to "repaired." The repair only counts when that same misconception resurfaces days later — unlabeled, never first, one per visit, buried inside an ordinary warm-up the child has no reason to read as a test. A failed retest cracks the robot back open and returns it to the repair loop.
- The band ladder: Four bands — place value, addition regrouping, subtraction regrouping, fractions as numbers — gated so a rung opens the session after the one below is finished. One rung per visit: a child can't cram down the ladder in an afternoon, which is the behavior the entire mastery rule exists to refuse to reward.
- Knowing when it can't tell: Two hypothesis pairs are structurally confounded — they write the identical answer on every problem available in the child's band. Rather than guess, the app says so on the board and names the one problem that would separate them. A structural invariant enforced around every bug also prevents it from claiming an item where its own procedure happens to return the correct answer.
- Character system: Thirteen robots from one SVG skeleton plus a palette table — two colors, an eye group, a head/antenna/feet silhouette, and one glitch "tell" each. Adding a bug to the library without adding a skin is a test failure, so the cast can never silently fall out of sync with the engine.
- Design system: A "Case Files" detective treatment — thick ink outlines, hard offset shadows, index cards on pushpins, rubber stamps. One stylesheet with a guard test that fails the build if a class is applied with no rule, if a rule is never applied, or if two unrelated components quietly share a global class name.
- Demo film pipeline: The 2:46 demo is Remotion composed over real footage of the real app — a scripted Playwright session driving the built site, with no mocked screens and multi-session state that was played rather than fabricated. Rendered at 50fps against a hard-25fps capture (an integer 2× so nothing is ever resampled) and verified frame by frame against both neighbors: zero torn frames in 8,300.
- Privacy and cost: No sign-in, no accounts, no backend, no network at play time, no data leaving the device. Progress lives in localStorage, which is what makes a retest days later possible at all. Append ?peek for a read-only view of the retest schedule — the delayed retest is invisible by design, which makes it invisible to anyone evaluating it too.
- Tech Stack: React 18, TypeScript (Node 22 native type stripping), Vite, node:test, Remotion, Playwright, Vercel. 147 tests, zero runtime dependencies below the UI.
- Try it now!: https://glitchlab-lyart.vercel.app
- Demo video: https://youtu.be/ngI9026qLbM
- Code: https://github.com/sb8869/glitchlab

### FanBase - Your Teams. One Home.
Full-Stack Sports Aggregation Platform | 2026
- About: FanBase is a personalized sports dashboard that lets fans follow teams across MLB, NFL, NBA, and EPL and see everything that matters to them — live scores, schedules, standings, results, and news — in one feed, instead of digging through four different league sites and apps.
- Today digest: the home view surfaces a fan's followed teams at a glance: live games, today's results with a running win/loss tally, what's up next, and yesterday's results — all computed from the user's followed-team list, not a generic scoreboard.
- Live game detail: a deep-dive view per game with a scoreboard, sport-aware box score (MLB batting/pitching lines, NFL passing/rushing/receiving, NBA full stat table), a scoring-plays timeline, and a Match Stats comparison panel that pulls ESPN's team-level advanced stats (possession, shots, first downs, shooting splits) depending on the sport.
- Standings: division-level tables for followed teams with a one-click toggle to the full league table — NBA groups by conference rather than division, matching how most fans actually track it.
- Schedule & results: a rolling 14-day fixture list grouped by day and league, plus a date-steppable results browser for any past day.
- News: a per-league collapsible accordion feed pulling live headlines for only the leagues a user actually follows.
- Onboarding & team management: new users pick their teams in an onboarding flow (searchable, filterable by league, with a save-and-continue gate); existing users can add/remove teams anytime from a dedicated "My Teams" screen.
- Design system: underwent a full visual rebrand ("Broadcast Ignition") — a dark, broadcast-grade theme built on Anton/Archivo/IBM Plex Mono typography, an amber "my team" personalization signal kept independent from per-league accent colors, and live-game pulse/blink micro-animations.
- Data source: all live sports data is pulled directly from ESPN's public site API in real time — no license fees, no stale cached datasets — normalized across four very different sports into one consistent internal team/game model.
- Authentication and persistence: NextAuth (Auth.js) handles session management with Google OAuth and credentials (bcrypt-hashed password) sign-in; Postgres via Prisma stores followed teams and notification preferences.
- Tech Stack: Next.js (App Router), React, TypeScript, Tailwind CSS, Radix UI, Zustand, SWR, Prisma, PostgreSQL (Neon serverless), NextAuth v5, Vercel.
- Try it now!: https://fanbase-eosin.vercel.app/

### QA Agent - AI-Powered Automated Bug Detection
Internal Tool / Company Initiative | SMT TechHub LLC | 2026 (In Progress) (🚧🚧🚧)
- About: QA Agent is an adaptive AI testing platform developed as an internal initiative at SMT TechHub. The system controls a real web browser, explores forms it has never seen before, generates its own test cases from what it actually observes on screen, and produces structured bug reports with screenshots. Unlike scripted tools like Selenium or Cypress, it reasons about the UI the way a human tester would — discovering unexpected behaviour rather than simply verifying predetermined expectations.
- Engineered a three-phase adaptive agent loop: an exploration phase where Claude Opus analyses a live screenshot and generates a bespoke test plan, an execution phase where the agent navigates, types, and clicks through real browser interactions, and an adaptive follow-up phase where the agent chases threads opened by bugs it already found.
- Integrated Playwright for full browser automation including form filling, button clicks, keyboard input, and page navigation across any web application without app-specific configuration.
- Implemented a vision-based UI reader that identifies actual DOM selectors, field labels, and interactive elements from screenshots — enabling the agent to test forms it has never encountered before without any hardcoded assumptions.
- Designed a cost-optimised three-tier model routing system: Claude Opus for high-reasoning tasks (exploration, follow-up decisions), Claude Sonnet for step-by-step execution, and Claude Haiku for result classification — reducing per-run API cost by approximately 85% versus a single-model approach.
- Built a text-history summarisation system that replaces screenshot re-transmission across agent steps, eliminating the largest source of token waste in multi-step vision agent loops.
- Implemented JPEG screenshot compression at 55% quality via Pillow, reducing image token costs by ~70% with no meaningful loss in Claude's ability to read UI elements.
- Developed a structured bug reporting pipeline that captures severity, reproduction steps, expected vs actual behaviour, and a timestamped screenshot of the exact failure state for every bug found.
- Engineered real-time API cost tracking across all model calls, writing estimated spend per run directly into the final report so cost is always visible and auditable.
- Built a companion web interface (Claude-powered) allowing users to test known apps by URL or upload a screenshot of any unknown form for instant AI-generated analysis, with expandable bug cards and one-click markdown export.
- Tech Stack: Python, Playwright, Anthropic Claude API (Opus / Sonnet / Haiku), Pillow, Faker, python-dotenv, JavaScript, HTML/CSS
- Key Features: Vision-based UI exploration, Adaptive test generation, Real browser control, Three-tier model cost routing, Screenshot-backed bug reports, Freeform scope input, Per-run cost tracking, Web companion interface

### Planorix - Computer Vision Floor Plan to 3D Converter
Full-Stack Web Application | 2025 
- About: Planorix is an intelligent web application that transforms 2D floor plan images into interactive 3D models using computer vision and advanced image processing. Users can upload JPG or PDF floor plans and instantly visualize them as navigable 3D environments with intuitive camera controls for architectural visualization and space planning.
- Designed and developed a full-stack application combining React frontend with FastAPI backend for seamless floor plan processing and 3D visualization.
- Implemented advanced computer vision algorithms using OpenCV for wall detection, featuring thickness-based pattern recognition that achieves 60-70% accuracy in distinguishing structural elements from fixtures and text.
- Built a sophisticated 3D rendering system with interactive canvas-based visualization, including orbit/pan/zoom camera controls anchored to the floor center for intuitive navigation.
- Created an intelligent wall detection pipeline with dominant thickness analysis, two-tier filtering (lenient for thick walls, strict for thin walls), and automated line merging to optimize structural accuracy.
- Developed a dual 3D generation system supporting both lightweight JSON models for web viewing and optional Blender GLB export for professional use cases.
- Engineered a responsive file upload interface with drag-and-drop functionality, real-time progress tracking, and comprehensive error handling for various image formats.
- Implemented an interactive 3D viewer with solid-color wall rendering, depth-based face sorting, and dynamic camera controls for optimal user experience.
- Built modular backend architecture with separate image processing, model generation, and API layers, enabling easy scaling and feature expansion.
- Tech Stack: React, FastAPI, OpenCV, NumPy, JavaScript (ES6), Python, Canvas API, Axios, HTML5 File API
- Key Features: Computer vision wall detection, Interactive 3D visualization, Real-time image processing, Thickness-based pattern recognition, Drag-and-drop file upload, Camera orbit controls

### FlipPoint - Buy. Flip. Profit. Repeat.
Web Application | 2025 
- About: FlipPoint is an in-progress browser-based simulation that places players in the role of a used-car dealership owner. The project blends market economics, negotiation psychology, and progression systems to create strategic, replayable gameplay.
- Core loop: buy, inspect, repair, list, negotiate, and sell. I implemented a procedural car generator and a robust 6-factor pricing engine (age, mileage, condition, rarity, demand/trend, randomness) so inventory feels varied and market-driven.
- Appraisal & inspection: a 10-level "Expert Eye" skill tree provides progressively tighter resale/damage estimates; players can purchase rarity-scaled inspections for exact diagnostics, creating a risk-versus-certainty tradeoff.
- Staff & facilities: full hiring and capacity systems (mechanics, salespeople, detailers, appraisers) and facility upgrades (workshop, showroom, office, security, technology) that influence repair throughput, listing capacity, negotiation outcomes, and appraisal accuracy.
- Market systems: supply & demand dynamics, trending events, hot deals, and an interest-based sales timeline deliver realistic buyer behavior and strategic opportunities.
- Selling flows: listings, auctions, negotiation modal with seller patience, hidden reserves, and counteroffer logic.
- Product and engineering practices: modular React architecture, Tailwind-powered responsive UI, comprehensive gameplay documentation, and a phased roadmap for expansion (analytics, customer personalities, multiplayer hooks).
- Authentication and persistence: the app uses Supabase for signup, login, cloud save persistence, and the public leaderboard.
- OAuth providers: players can also sign in using Google or Discord (OAuth) for convenience.
- Tech Stack: React, Vite, TailwindCSS, JavaScript (ES6), Lucide-React, Node.js, Supabase, Vercel.
- Try it now!: https://flippoint.vercel.app/

### Graduate Capstone Research
Lead Researcher | January - May 2025
- Lead researcher on "Designing Thermal Feedback for Neck-Worn Haptic Devices.
- Conducting usability research on thermal feedback in neck-worn haptic devices.

### Travel Guide Website
Web Application | January - May 2025
- Developed a travel website for Atlanta using Vanilla JavaScript, reusable PHP components, HTML/CSS
- https://people.rit.edu/sb8869/iste646/project1/index.html

### KeyRush - A minigame
Web Application | June 2025
- An interactive reflex game built with HTML/CSS/JS to simulate a timed minigame.
- Features randomized input sequences, a dynamic timer bar, and multi-round progression.

### Undergraduate Capstone Project - ArtTag
Web Application | December 2021 - April 2022
- About: ArtTag is a drawing experience that allows you to post your drawings on walls in AR and see them alongside the drawings of other users. By allowing our users to contribute to their community through drawing, we're hoping to incentivize them to explore and discover the artistic expressions of the people around them.
- Collaborated with five designers and two developers to design and develop an interactive web application for mobile.
- Acted as a back-end developer and was responsible for creating a moderation bot, setting up a database to store all data, and working on AR functionality.
- Used Node.js and packages such as discord.js, mongoose, and mongoose-events to build the back-end of the application.
- Used JS frameworks such as Konva.js, p5.js, and A-Frame to set up the AR functionality of the application.
- Used React to develop the front-end of the application.
- Social Media: 
  - Instagram - https://www.instagram.com/arttag_rit/
  - Facebook - https://www.facebook.com/ArtTag-RIT-101273502460458
  - Demo: https://youtu.be/fPXnCINi3rA
 
### Stardew Valley Mod - Rejuvenating Forest
Game Mod | December 2021
- Developed and released a content-rich Stardew Valley mod featuring a custom questline, new explorable area, and original gameplay mechanics.
- Implemented in C# using the Stardew Valley Modding API (SMAPI) with multiple modding frameworks to extend base game functionality.
- Managed compatibility and dependency integration with other popular modding libraries (e.g., Content Patcher, JSON Assets).
- Netted over 2900 downloads on NexusMods - https://www.nexusmods.com/stardewvalley/mods/10322

### Ranked-Choice Voting Application
Web Application | October 2021
- Collaborated with a group of five designers to develop a voting ballot for the NY State Ranked Choice Voting system.
- Acted as tech lead for a group of three developers to develop a web application for 1920x1080 touchscreen devices.
- Demo: https://people.rit.edu/sb8869/nmde401/rcv/

### Movie Finder Application
Web Application | October 2021
- Designed and developed an application that allows users to search for movies based on genre and language.
- Application features a theatre finder through which users can locate their nearest movie theatres.
- Used the 'TheMovieDB' API to fetch movie information and 'YelpAPI' to fetch nearest movie theatres.
- Used the Bulma framework to design a responsive application.
- Demo: https://people.rit.edu/sb8869/330/project2/

### Image Builder Application
Application | March 2022
- Worked with a group of five developers to develop an application that accepts images and re-creates them using images of dogs.
- References a Tile library developed by Professor Travis Stodter. 
- Used Dog API to gather images of dogs to use in the re-creation.
- Demo: https://observablehq.com/@epr4296/tiles-random

### Asteroids Game
Web Application | December 2021
- Developed an asteroids game using vanilla javascript.
- Demo: https://people.rit.edu/sb8869/330/project3/



