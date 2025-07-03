# 📘 NPM Basics & Concepts

## ❓ What is npm?
**npm** originally stood for **Node Package Manager**, but it has outgrown that name.
It is a tool used to **install, manage, and share packages** (libraries, tools, etc.) in Node.js applications.

---

## 📦 What is `package.json`?
The **configuration file** for npm. It contains:

- Project metadata (name, version, etc.)
- List of dependencies and their version ranges
- Scripts (`npm start`, `npm test`, etc.)
- Other project configurations

---

## 📌 What is `package-lock.json`?
- Tracks the **exact version** of each installed package
- Includes **transitive dependencies** (dependencies of dependencies)
- Ensures **consistent installs** across machines

---

## 📁 What is `node_modules/`?
This is the folder where **npm stores all installed packages** and their dependencies.
It acts like a **local package database** used by your app.

---

## 🔁 What is a transitive dependency?
A **transitive dependency** is a dependency **used by another dependency**.

**Example:**
You install `Parcel` → Parcel uses `Babel` → Babel uses another package.
All of these are part of the transitive dependency chain.

---

## 🚀 What is Parcel?
Parcel is a **zero-configuration bundler**.
It helps bundle files like **HTML, CSS, JS**, and more, and **runs your app** efficiently.

Great for:
- Prototyping
- Simpler front-end apps

---

## 🔐 What is `sha512` under `integrity` in `package-lock.json`?
The `sha512` field is a **cryptographic hash** used to:

- Ensure the integrity of packages
- Verify no tampering occurred
- Lock in the **exact content and version** of the dependency

---

## 📂 Types of npm Dependencies

### 1. Regular (Production) Dependencies
- Needed at **runtime**
- Example: `react`, `express`

```bash
npm install package-name


2. Development Dependencies
Only needed during development

Example: parcel, eslint

npm install -D package-name


| Symbol | Example  | Meaning                                                               |
| ------ | -------- | --------------------------------------------------------------------- |
| `^`    | `^1.2.3` | Allows updates to **minor & patch** versions (e.g., `1.3.0`, `1.2.4`) |
| `~`    | `~1.2.3` | Allows updates to **patch only** (e.g., `1.2.4`, but not `1.3.0`)     |
