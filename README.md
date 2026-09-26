# 🏥 MedicineBridge

**Understand Your Prescription. Find Your Medicine.**

<div align="center">
  <img src="WhatsApp Image 2026-09-27 at 00.52.35.jpeg" alt="MedicineBridge Homepage" width="800"/> 
</div>
<br/>

## 🚨 The Problem We're Solving
We’ve all been there—staring at a doctor’s handwritten prescription and having absolutely no idea what it says. Patients are often left completely reliant on their local pharmacist to decipher the handwriting, which can sometimes lead to confusion or errors. On top of that, many people simply aren't aware of affordable generic alternatives or the locations of government-subsidized pharmacies like Jan Aushadhi Kendras. This lack of transparency means people end up paying significantly more for their healthcare than they need to.

## 💡 Our Solution
Enter **MedicineBridge**. We built this AI-powered web app to put the power back in the patient's hands. By snapping a quick photo of a prescription, users can instantly translate doctor-speak into plain language, discover affordable generic alternatives, and get turn-by-turn directions to the cheapest local pharmacies. 

## ✨ What It Can Do
*   **Snap & Upload:** Easily upload or drag-and-drop photos of handwritten prescriptions.
*   **AI Medicine Extraction:** Our AI acts as a digital pharmacist, reading the handwriting to identify medicine names, dosages, and quantities.
*   **Clear Medical Info:** Get a jargon-free breakdown of exactly what the medicine is and who manufactures it.
*   **Smart Price Comparison:** See how the price stacks up across standard local pharmacies, online retailers, and affordable Jan Aushadhi Kendras.
*   **Local Pharmacy Finder:** Automatically locate the nearest medicine sources using your device's GPS, complete with distance estimates and Google Maps routing.
*   **Bilingual Accessibility:** Fully switchable between English and Hindi, ensuring language isn't a barrier to healthcare access.
*   **Manual Search Mode:** Don't have a prescription? You can manually type and search for any medicine.
*   **Personal Dashboard:** Keep track of your recent prescription uploads and saved medicines in one place.

## 🔄 How the Magic Works
1.  **Upload:** Drop in a clear photo of your prescription.
2.  **Analyze:** The AI scans the image and extracts the vital details.
3.  **Review:** You check the plain-text information and compare current market prices.
4.  **Locate:** We show you exactly where to buy it nearby.

## 🏗️ Under the Hood (Tech Stack)
*   **Frontend:** Built with React 18 and TypeScript for a snappy, type-safe experience.
*   **Build Tool:** Vite, keeping our development cycle lightning fast.
*   **Styling:** Tailwind CSS to ensure the app looks great on both phones and desktops.
*   **State & Navigation:** Standard React Hooks and Context API (powering our seamless English/Hindi toggling).
*   **Mapping:** HTML5 Geolocation hooked into Google Maps routing.

## 🧠 Powered by Gemini AI
MedicineBridge's core ability to read prescriptions is powered by Google's Gemini AI. The app sends the prescription image to the AI, which returns structured data (medicine name, strength, form, etc.). Crucially, it also returns a `needs_verification` flag—meaning the AI knows when it's unsure and prompts the user to double-check. *(Note: For the hackathon demo environment, this endpoint currently simulates the AI processing with realistic mock data to ensure a smooth presentation).*

## 🗄️ Database Architecture
To keep things moving fast for the hackathon, we built a robust client-side relational mock database. Our data layer is fully decoupled using dedicated services, meaning swapping this out for Firebase, Supabase, or PostgreSQL in production will be a simple plug-and-play operation.

## 🛡️ Safety First (The "MedicineBridge Check")
We don't play around with patient safety. If our AI isn't 100% confident in what it's reading, it immediately flags the medicine with a prominent "Needs Verification" warning. We also include persistent disclaimers reminding users that while MedicineBridge is a helpful guide, it does not replace the professional advice of a qualified doctor.

## 🚀 Want to run it locally?

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/MedicineBridge.git](https://github.com/your-username/MedicineBridge.git)
   cd MedicineBridgeInstall the dependencies:

Bash
npm install
Set up your environment:
Create a .env file in the root directory (check the section below for what you need).

Spin up the server:

Bash
npm run dev
🔐 Environment Variables
To get the maps and AI working, create a .env file in the main folder and add your keys:

Code snippet
VITE_GEMINI_API_KEY=your_gemini_api_key_here
VITE_GOOGLE_MAPS_API_KEY=your_google_maps_api_key_here
🔭 Where We're Heading Next
Live Inventory: Hooking up to local pharmacy APIs so you know if a drug is actually in stock before you leave the house.

Cloud Backend: Migrating to Firebase for persistent user accounts and a cloud-synced prescription history.

Telemedicine Links: Direct integration with platforms like E-Sanjeevani.

More Languages: Expanding our translation engine to support Tamil, Telugu, Marathi, and more.

👥 Meet the Builders

ARYA SHARMA - AI & Vision Integration

ARYA SINGH - Frontend & UI/UX

ANTRA GARG - Backend & Data Architecture

AYATI TRIVEDI - Geolocation & Maps

⚠️ Disclaimer
MedicineBridge provides information and prescription-reading assistance only. Always verify medicines, dosage, and treatment decisions with a qualified doctor or pharmacist.
