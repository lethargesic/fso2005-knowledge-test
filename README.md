# FSO 2005 Knowledge Test

An interactive web app and Android app for testing your knowledge of the **Regulatory Reform (Fire Safety) Order 2005** (RRFSO 2005) — the main fire safety legislation for non-domestic premises in England and Wales.

## Features

- **100 questions** covering all parts of the FSO 2005
- **Dashboard** front page showing your progress, accuracy, and learning areas
- **Two quiz modes**: general knowledge (all questions) or section-specific
- **Priority Learning**: questions you get wrong appear prominently on the dashboard
- **Flagged for Review**: highlight questions you want to revisit, even if you got them right
- **Article tooltips**: hover over any Article reference to see a plain-English summary
- **Progress persistence**: your progress is saved in the browser (localStorage) / app


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

## Web Usage

1. Download `index.html`
2. Open it in any web browser
3. Start quizzing!

No server or installation needed — it's a single self-contained HTML file.

## Android App

The app is built as a native Android app using [Capacitor](https://capacitorjs.com/) (WebView wrapper).

### Build from source

Prerequisites:
- Java JDK 21+
- Android SDK (Platform 36, Build-Tools 36.0.0)
- Node.js 18+

```bash
# Install dependencies
npm install

# Copy web assets to Android
npx cap copy android

# Build debug APK
cd android && ./gradlew assembleDebug

# Build release APK (requires keystore)
cd android && ./gradlew assembleRelease
```

APKs are output to `android/app/build/outputs/apk/`.

### Install on your phone

1. Enable "Install from unknown sources" in Android Settings
2. Transfer the `app-debug.apk` to your phone
3. Open the APK file to install

### Play Store deployment

To upload to the Google Play Store:
1. Create a [Google Play Developer account](https://play.google.com/console) ($25 one-time fee)
2. Build a release APK or App Bundle (`./gradlew bundleRelease`)
3. Upload the `.aab` file at https://play.google.com/console
4. Fill in the store listing (description, screenshots, etc.)

## Question Generation

Questions were generated using a local LLM (Ollama, gemma4:26b) based on the actual legislation text from [legislation.gov.uk](https://www.legislation.gov.uk/uksi/2005/1541/contents). Each question references the specific Article it's based on.

## Sources

- [The Regulatory Reform (Fire Safety) Order 2005](https://www.legislation.gov.uk/uksi/2005/1541/contents) — full text from legislation.gov.uk
- [Fire safety: guidance for those with legal duties](https://www.gov.uk/government/collections/fire-safety-legislation-guidance-for-those-with-legal-duties) — GOV.UK guidance

## Tech Stack

- **Web**: Single self-contained HTML file (no dependencies)
- **Android**: Capacitor 8 (WebView wrapper)
- **Questions**: Generated via Ollama (gemma4:26b) from legislation.gov.uk source text

## License

MIT
