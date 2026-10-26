# MedicineBridge

MedicineBridge is a bilingual (English/Hindi) web application for understanding prescriptions and finding affordable medicine sources. It gives users a guided way to upload a prescription, review extracted medicines, compare prices, and locate nearby pharmacies or Jan Aushadhi centres.

> **Important:** This repository currently contains a frontend demo. Prescription analysis, medicine availability, and price data are simulated with local demo data. Always verify medicines, dosage, and availability with a qualified healthcare professional or pharmacist.

## Features

- Upload a prescription image and review structured medicine results.
- Search the demo medicine catalogue.
- Compare available prices for a selected medicine.
- Find nearby medicine sources using browser geolocation when permitted.
- View saved prescription activity in the dashboard.
- Switch the interface between English and Hindi.
- Responsive layout for desktop and mobile screens.

## Tech Stack

- React 18 and TypeScript
- Vite
- Tailwind CSS
- Firebase Hosting configuration
- `lucide-react` for icons

## Getting Started

### Prerequisites

- Node.js 18 or newer
- npm 9 or newer

### Installation

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Vite will print the local URL, usually `http://localhost:5173`.

## Available Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Vite development server. |
| `npm run build` | Type-check and create a production build in `dist/`. |
| `npm run typecheck` | Run TypeScript without emitting files. |
| `npm run lint` | Run ESLint across the project. |
| `npm run preview` | Serve the production build locally. |

## Environment Variables

Firebase configuration placeholders are provided in `.env.example`. To use them locally, copy the file to `.env.local` and provide the appropriate values:

```bash
VITE_FIREBASE_API_KEY=
VITE_FIREBASE_AUTH_DOMAIN=
VITE_FIREBASE_PROJECT_ID=
VITE_FIREBASE_STORAGE_BUCKET=
VITE_FIREBASE_MESSAGING_SENDER_ID=
VITE_FIREBASE_APP_ID=
```

The current demo does not read these values yet. Do not commit `.env`, `.env.local`, or any other file containing credentials.

## Project Structure

```text
src/
	components/   Shared UI such as the navbar, footer, and medicine cards
	context/      Language context and English/Hindi translations
	data/         Local demo medicine, prescription, and source data
	pages/        Home, upload, search, comparison, nearby, and dashboard views
	services/     Prescription analysis, medicine, and map service boundaries
	App.tsx       Client-side page state and top-level composition
```

## Firebase Hosting

The project is configured as a single-page application in `firebase.json`. Build the app and deploy the generated `dist/` directory with the Firebase CLI:

```bash
npm run build
npx firebase login
npx firebase deploy --only hosting
```

The selected Firebase project is defined in `.firebaserc`. Confirm that it points to the intended project before deploying.

## Current Limitations

- Prescription OCR/AI is represented by a simulated Gemini integration.
- Search results, pricing, and source availability come from local demo data.
- Firebase authentication and persistence are not wired into the UI.
- Map links and browser geolocation are available, but live pharmacy inventory is not.

## Development Notes

Before opening a pull request, run:

```bash
npm run lint
npm run typecheck
npm run build
```
