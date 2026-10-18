Round 4: Fire Awareness course + certificate verification.
- courses/fire-awareness/index.html + course-data.js: NEW paid-course page (6 modules, knowledge checks, 15-question
  final assessment marked server-side, 80% pass, certificate PNG/print with number, valid 12 months).
  If the learner has joined a team in the game, a pass is logged to that team's manager dashboard.
  Config at the top of the script: ISSUER, SIGNATORY, CPD_LINE (fill in once CPD accredited).
- verify/index.html: NEW public certificate lookup (/verify/?code=HH-XXXXX-XXXXX).
- sitemap.xml: adds /courses/fire-awareness/.
Setup: run hh-course-migration.sql in the Supabase SQL editor FIRST (kept outside this repo: it holds the answer key).
Deploy: copy over repo, commit, push. Then request indexing for /courses/fire-awareness/.
Not in yet: payment gate (Stripe), employer seats. Course is currently open to anyone with the link.
