
# JD Frameworks – Project Dashboard Platform

## 📚 Project Overview

**JD Frameworks** is a dashboard web application designed for seamless department and project management within large organizations (such as government or educational institutions). The platform helps visualize cross-department collaboration, track project progress, manage team members, requests, and analyze performance using interactive charts.

This project is developed as a college project. It is fully functional in its current form using realistic mock data, even without any backend connection!


## ✨ Features

- **Dashboard:** Visual overview of key statistics, including department success rates, inter-department collaboration charts, and project statuses.
- **Department Management:** View and analyze collaboration between various departments.
- **Team Management:** See and manage the list of team members (easily extensible).
- **Requests:** Users can create, view, and (if they are the creator) delete their own requests.
- **Profile & Settings:** Each user can manage their profile and customize basic settings.
- **Landing Page:** Dynamic landing page that adapts based on login status.
- **Notifications (coming soon):** Notifications feature is planned for a future update.

All data is **persisted locally using your browser's localStorage** for requests and uses in-memory mock data for charts and analysis.


## 🛠️ Technologies Used

- **Frontend:** React + TypeScript + Vite
- **UI Kit:** shadcn/ui, Tailwind CSS
- **Routing:** react-router-dom
- **Charts:** recharts
- **State Management & Data Fetching:** @tanstack/react-query (future-proofing)
- **Persistent Storage:** browser localStorage for requests, static files for sample data

No backend is required to use or demo the platform!


## 🗂️ Where is the Data Stored?

### Home Tab & Analytics

- **Source:** All analytics charts and summary data (collaboration, interactions, project rates) are defined in `src/data/collaboration-data.ts`.
- **How it Works:** This data is hardcoded and realistic, so the demo works out-of-the-box.
- **Custom Backend:** If you later connect a real backend (such as a SQLite API), you should replace this mock data with API calls.

### Requests & User Interactions

- **Source:** User-created requests are stored in `localStorage`, so all create/delete actions are retained on your browser.


## ⛔ Note for Your Project Submission

You do **NOT** need to connect a backend for this college project. All demo and interaction data comes from static files or local browser storage – simply clone and run!


---

## 💡 (Optional) How To Connect SQLite Backend

**You only need this if you want real backend data! The project works fine with mock data for college submissions.**

### 1. Set Up SQLite + Express Backend

- Install dependencies:
  ```sh
  npm install sqlite3 express cors
  ```
- Create an `Express` server (see example in `src/data/collaboration-data.ts` for guidance).
- Build API endpoints to read/write data from SQLite (projects, departments, requests, etc).

### 2. Update Database Schema

- Write your schema using the example provided in `src/data/collaboration-data.ts` (inside comments).

### 3. Connect Frontend to Backend

- Replace mock data/statics in files like `src/data/collaboration-data.ts` with `fetch`/`axios` API calls to your backend endpoints.
- Adapt localStorage request logic (in `RequestForm.tsx` and wherever requests are displayed) to POST/GET requests to your server for persistent storage.

### 4. Testing

- Start your backend server (e.g., `node backend/server.js`).
- Update frontend code to use your backend URL (instead of static data).
- Confirm data shows up live from your API.

For college submissions, demo works fully without this step!


---

## 👩‍💻 Running The Project Locally

Just follow these simple steps:

```sh
# Step 1: Clone the repository using the project's Git URL.
git clone <YOUR_GIT_URL>

# Step 2: Navigate to the project directory.
cd <YOUR_PROJECT_NAME>

# Step 3: Install the necessary dependencies.
npm install

# Step 4: Start the development server.
npm run dev
```

Open `http://localhost:5173` (or the port Vite shows) in your browser to use the app.

---

## 📝 Important Files & Comments

- Analytics & charts mock data:  
  `src/data/collaboration-data.ts` (fully commented, includes SQLite backend example)
- Departments list:  
  `src/data/departments.ts`
- Team members:  
  `src/data/team.ts`
- Request logic & demo:  
  `src/components/dashboard/RequestForm.tsx` (comments show how localStorage works)
- All code is commented for smoother understanding and future integrations!

---

## 🗣️ Contact

For help, suggestions, or contributions, feel free to contact [Lovable support](https://lovable.dev) or post on [Lovable Discord](https://discord.gg/7TzaT2ehE9).

---

**This project is intended for educational/demo purposes.**  
Leave the mock data as is for your college submission, or follow the steps above to add real backend integration in the future!
