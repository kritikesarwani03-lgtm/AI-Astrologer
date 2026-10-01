# 🔮 AI Astrologer

A personalized astrology-inspired personality analysis web app with a context-aware AI chat assistant. Enter your birth details, get a zodiac-based personality profile, and ask follow-up questions about yourself.

> **Disclaimer:** All insights are astrology-inspired and meant for entertainment and self-reflection. They are not a scientific psychological assessment.

**Live demo:** _add your GitHub Pages link here_
(example: `https://your-username.github.io/ai-astrologer/`)

---

## Features

- **Birth details form:** name, date of birth (required), birth time and birth place (optional).
- **Zodiac calculation:** finds your sun sign from your date of birth, covering all 12 signs including the year-end Capricorn range.
- **Personality profile:** shows personality traits, strengths, areas to improve and career tendencies.
- **AI chat assistant:** ask questions like "What are my strengths?" or "What career might suit me?" and get answers based on your profile.
- **Dual-mode responses:** uses a live AI model when available, and automatically falls back to a built-in rule-based engine, so the chat always works.
- **Saved locally:** your profile and chat history are stored in the browser (`localStorage`), so you don't re-enter details after a refresh.
- **Dark theme and responsive layout:** works on desktop and mobile screens.
- **No backend needed:** a single `index.html` file with no installation or database.

## Tech Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | CSS3 (custom properties, flexbox, grid) |
| Logic | Vanilla JavaScript (ES6+) |
| Storage | Browser `localStorage` |
| AI | Optional live AI, with a rule-based fallback |

## Project Structure

```
ai-astrologer/
├── index.html     # HTML, CSS and JavaScript in one file
└── README.md
```

## How to Run

**Option 1: open directly**
1. Download `index.html`.
2. Double-click it to open in any modern browser.

**Option 2: VS Code Live Server**
1. Open the folder in VS Code and install the **Live Server** extension.
2. Right-click `index.html` and choose **Open with Live Server**.

**Option 3: host it online (GitHub Pages)**
1. Upload `index.html` to a public GitHub repository.
2. Go to **Settings → Pages**, choose branch `main` and folder `/ (root)`, then save.
3. Your site will be available at `https://<username>.github.io/<repo-name>/`.

## How It Works

1. **Input:** the user fills in the birth details form.
2. **Zodiac engine:** `getZodiac()` compares the date of birth against a table of 12 sign end-dates.
3. **Profile generation:** the matching sign's traits, strengths, improvement areas and career notes are displayed.
4. **Chat:** the user's question is combined with the profile as context.
   - If a live AI is available, the profile and the last 6 messages are sent as context.
   - Otherwise `simulateAnswer()` picks a response by matching keywords such as career, strengths, relationships or personality.
5. **Persistence:** the profile and chat history are saved to `localStorage`.

## Zodiac Date Ranges Used

| Sign | Dates | Sign | Dates |
|---|---|---|---|
| Capricorn | Dec 22 – Jan 19 | Cancer | Jun 21 – Jul 22 |
| Aquarius | Jan 20 – Feb 18 | Leo | Jul 23 – Aug 22 |
| Pisces | Feb 19 – Mar 20 | Virgo | Aug 23 – Sep 22 |
| Aries | Mar 21 – Apr 19 | Libra | Sep 23 – Oct 22 |
| Taurus | Apr 20 – May 20 | Scorpio | Oct 23 – Nov 21 |
| Gemini | May 21 – Jun 20 | Sagittarius | Nov 22 – Dec 21 |

## Limitations

- Data is saved only in the user's browser, so it does not sync across devices.
- The rule-based chat has limited phrasing compared with a live AI.
- Only the sun sign is used. Birth time and place are collected but not used for rising sign or house calculations.
- Earlier chat messages are saved but not redrawn on screen after a page refresh.

## Future Enhancements

- Backend and database (for example Node.js and MongoDB) for accounts and cross-device sync.
- Rising sign, moon sign and planetary position calculations using birth time and place.
- Downloadable PDF profile report.
- Chat history panel that restores earlier conversations.
- Multi-language support.

## Author

**Pranjal Vishnoi**
Roll No: 2500910100139 | Section: CSE-2
Department of Computer Science and Engineering
JSS Academy of Technical Education, Noida
Faculty Mentor: Ms. Akanksha

_Developed as a III Semester Internship / Mini Project._
