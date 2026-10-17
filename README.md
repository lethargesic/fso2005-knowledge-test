# FSO 2005 Knowledge Test

An interactive web app for testing your knowledge of the **Regulatory Reform (Fire Safety) Order 2005** (RRFSO 2005) — the main fire safety legislation for non-domestic premises in England and Wales.

## Features

- **100 questions** covering all parts of the FSO 2005
- **Dashboard** front page showing your progress, accuracy, and learning areas
- **Two quiz modes**: general knowledge (all questions) or section-specific
- **Priority Learning**: questions you get wrong appear prominently on the dashboard
- **Flagged for Review**: highlight questions you want to revisit, even if you got them right
- **Article tooltips**: hover over any Article reference to see a plain-English summary
- **Progress persistence**: your progress is saved in the browser (localStorage)
- **Brand styling**: uses the Irwell Valley Homes colour scheme and Helvetica Neue font

## Sections Covered

| Section | Questions |
|---------|-----------|
| Part 1 - General | 15 |
| Part 2 - Fire Safety Duties | 38 |
| Part 3 - Enforcement | 18 |
| Part 4 - Offences and Appeals | 15 |
| Schedule 1 - Principles of Prevention | 6 |
| General Knowledge | 8 |
| **Total** | **100** |

## Usage

1. Download `index.html`
2. Open it in any web browser
3. Start quizzing!

No server or installation needed — it's a single self-contained HTML file.

## Question Generation

Questions were generated using a local LLM (Ollama, gemma4:26b) based on the actual legislation text from [legislation.gov.uk](https://www.legislation.gov.uk/uksi/2005/1541/contents). Each question references the specific Article it's based on.

## Sources

- [The Regulatory Reform (Fire Safety) Order 2005](https://www.legislation.gov.uk/uksi/2005/1541/contents) — full text from legislation.gov.uk
- [Fire safety: guidance for those with legal duties](https://www.gov.uk/government/collections/fire-safety-legislation-guidance-for-those-with-legal-duties) — GOV.UK guidance

## License

MIT
