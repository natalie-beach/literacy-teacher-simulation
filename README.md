# Think Like a Literacy Teacher · GitHub Pages prototype

## What is included
- `original-scenario.h5p`: untouched original upload for archival and future native H5P deployment.
- `original-content.json`: exact H5P content configuration (49 nodes, 6 branches, 3 YouTube video URLs).
- `index.html`, `style.css`, `app.js`: a **custom HTML playback of the original H5P content and branch paths**, with supplemental graded checkpoints and one final mastery assessment.
- `questions.json`: draft instructor-review questions, two per segment and five final questions.
- `Code.gs`: Google Apps Script that records and scores responses server-side.

**Important:** This prototype faithfully traverses the original H5P text, video URLs, alternatives, feedback and destination IDs, but it is **not the native H5P runtime**. It does not reproduce H5P styling, all player behavior, or certify that every H5P branch has been tested. It preserves the original H5P archive for a future native player if desired. The H5P export contains only two files and lacks the player libraries, so native H5P cannot run from that archive alone.

## Setup
1. Upload all files except `Code.gs` to the root of `https://github.com/natalie-beach/literacy-teacher-simulation` (keep names intact).
2. In the provided Google Sheet, choose **Extensions → Apps Script**, paste `Code.gs`, save and run `setup` once; authorize permissions.
3. In Apps Script choose **Deploy → New deployment → Web app**. Execute as **Me**; access **Anyone** (anonymous student posts require this). Copy the `/exec` URL. Be aware that public endpoints accept unverified submissions; six-digit codes are not secure identities.
4. Edit `config.js`: paste the `/exec` URL between the quotes for `endpoint`. Do not publish until it is set.
5. In GitHub choose **Settings → Pages → Deploy from a branch → main / root**. Open `https://natalie-beach.github.io/literacy-teacher-simulation/`.
6. TEST with a code such as 999999, traverse every branch, complete all four checkpoints, fail and retry the final mastery, and check both sheet tabs. Delete test records before assigning.

## Important limitations
- Original H5P prompts asking students to write in a response document remain in the original content. The new HTML checkpoints are additional, not substitutes.
- The website asks students to affirm that they watched a video; it cannot verify video attention or completion.
- Local progress is saved in the browser only. Switching devices may require repeating the original content. Sheet scores persist.
- No identity verification: codes can be guessed, reused, or impersonated. Avoid storing student names or sensitive data.
- Responses are scored in Apps Script; `questions.json` also contains draft correct answers for student-side display logic and is public. For higher-stakes assessment, move all answer keys to Apps Script and return scores from the server; this prototype is appropriate for low-stakes classroom mastery only.
- Google Apps Script web apps can encounter cross-origin or redirect restrictions depending on deployment and browser. Test from the actual GitHub Pages URL; if blocked, adjust the transport before student use.
- Checkpoints are graded 2 points each; final mastery is 4/5 (80%), unlimited attempts. Grading of checkpoint points and mastery is separate.
