## 🚀 PlacePicker

**PlacePicker** is a location-aware React application that allows users to build and manage a personalized list of places they want to visit or have already visited.

---

## 🌍 Features

### 📍 Location-Based Sorting
Automatically detects the user's location and displays available places sorted by distance.

### ➕ Add Places
Easily add places to your personal collection with a single click.

### ❌ Remove Places with Confirmation
Prevent accidental deletions using a confirmation modal.

### 💾 Persistent Data Storage
Selected places are stored in the browser using `localStorage`, ensuring data is preserved across sessions.

### 🚫 Duplicate Prevention
Ensures the same place cannot be added multiple times.

---

## ⚙️ How It Works

1. The app retrieves the user’s current location using the **Geolocation API**.  
2. Available places are sorted dynamically based on proximity.  
3. Users can:
   - Select places to add to their list  
   - Remove places with confirmation  
4. All selected places are stored locally and reloaded on revisit.  

---

## 🧠 Tech Stack

- React (Hooks) – `useState`, `useEffect`, `useRef`, `useCallback`  
- JavaScript (ES6+)  
- Browser APIs – Geolocation API, Local Storage  

---

## 📌 Key Highlight

> A simple yet powerful app demonstrating how to combine **geolocation, state management, and persistent storage** to create a real-world user experience.
