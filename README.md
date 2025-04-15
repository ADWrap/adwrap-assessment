# adwrap-assessment
**Full-stack assessment for ADWrap** – build a proposal creation feature using a media selection system (**billboards** & **streetpoles**). Includes sample data and expectations.

---

# ADWrap Proposal Creation – Full-Stack Assessment

Welcome to the ADWrap technical assessment. This task is designed to evaluate skills in full-stack development using real-world concepts from our platform.

---

## 🧭 Summary of What You’ll Do

- Use provided **mock data** as a reference.
- **Create your own media items** via backend logic (with workspace-scoped counts).
- Build a **proposal creation feature** using selected media.
- _(Optionally)_ Implement the **frontend UI** using our Figma design.

---

## 🎯 Objective

Build a **proposal creation feature** that allows users to select media items (**billboards** and **street poles**), and preview before "sending".

---

## 📐 What You'll Be Working With

Each **media item** can be:
- A **Static Billboard** with multiple `staticMediaFaces`
- A **Street Pole** with one or more `routes`

Sample JSON data is included in `/mock-data/`:
- **Media Items**

Additionally, each media item belongs to a **workspace**. When creating new items, counts (e.g., IDs) should be **independent per workspace** — e.g. each workspace starts counting media items from `1`.

---

## 🧱 Backend Notes – Database Setup (Optional but Recommended)

If you choose to use a database (e.g., **Postgres**), please do the following:

- **Create tables** for:
  - `mediaItems`
  - `staticMediaFaces`
  - `routes`
  - `workspaces`

- Ensure that:
  - Media items are scoped to a **workspace**.
  - Each **workspace has independent item counts** (e.g., `BB-1`, `SP-1`, etc.).
  - You can **seed your database** with custom media items instead of using the mock JSON.

> This helps simulate a more realistic and backend-driven flow.

---

## 🎨 Figma Designs

View the full design prototype here: [**Figma Link**](https://www.figma.com/design/5cvz0q0X4J4OombQ8hRwjr/Dev-Assessment?t=fwNbs9rQ7BnMrZsI-0)

> Please reference these screens when implementing the proposal feature.  
> **Note**: Feel free not to include details like **filters**, **pagination**, and **search** on the media items table as seen in the designs.

---

## 🛠️ Requirements

1. **Media Selection UI**
   - Display a list of media items in a table format.
   - Each item has expandable rows showing:
     - `staticMediaFaces` (for billboards)
     - `routes` (for streetpoles)

2. **Selection Logic**
   - Selecting a media item selects all its child faces/routes.
   - Selecting a child (face/route) selects the parent, but not other siblings.

3. **Proposal Preview**
   - Show a visual preview of selected media.

4. **Backend Task**
   - Create a **new media item** via API.
   - Ensure **counts like `Id` are per-workspace** (e.g., `SP-1`, `SP-2`, etc., only within that workspace).
   - You may define and create your own **database tables** if needed.

---

## 🌐 Frontend Task (Encouraged)

If you’re comfortable with frontend development, we encourage you to implement the **UI and selection logic** based on the Figma design.

---

## 🧪 Bonus (Nice-to-Haves)

- **Responsive layout**
- **Clean component and state management**

---

## 🔧 Stack Expectations

Use the stack you're most comfortable with. If undecided, we recommend:

- **Frontend**: `Next.js + Tailwind + ShadCN`
- **Backend**: `Node.js + Express`
- **State**: `Redux Toolkit` or local state
- **Data**: `Postgres` or Use the provided **JSON** as mock data. Feel free to replicate if necessary.

---

## 🧪 How to Submit

1. **Fork** this repo (or clone and create a private one).
2. **Complete the task**.
3. **Share your GitHub link or ZIP file** with us via email.

---

## ⏱️ Estimated Time

We recommend spending **no more than 3–6 days** total. You’re not expected to build everything — focus on **clean, thoughtful implementation**.

---

## 🙌 Questions?

If you’re stuck or unsure about any part of the task, feel free to reach out.

Good luck, and have fun!  
**– Team ADWrap**
