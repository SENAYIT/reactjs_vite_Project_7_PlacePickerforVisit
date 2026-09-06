# 📍 PlacePicker

PlacePicker is a simple React application that allows users to create a personal collection of places they would like to visit or have visited.

The application uses the browser's Geolocation API to sort available places based on the user's current location. Selected places are stored in localStorage, allowing them to remain available even after refreshing the page.

## ✨ Features

* 📍 Sorts available places by distance from the user's current location
* 🗺️ Select places to add them to a personal collection
* 💾 Saves selected places using localStorage
* 🗑️ Remove places from the selected collection
* ⚠️ Confirmation modal before removing a place
* ⏱️ Automatically confirms deletion after 3 seconds
* 📊 Displays a progress bar during the confirmation countdown
* 🧩 Uses reusable React components
* 🌀 Uses React Portals for the modal
* 🧹 Properly cleans up timers and intervals

## 🛠️ Technologies Used

* React
* JavaScript (ES6+)
* JSX
* React Hooks

  * useState
  * useEffect
  * useRef
  * useCallback
* Browser Geolocation API
* LocalStorage API
* React Portals
* HTML5 Dialog
* CSS
* Vite

## 📂 Project Structure

```text
src/
├── assets/
│   └── logo.png
│
├── components/
│   ├── DeleteConfirmation.jsx
│   ├── Modal.jsx
│   ├── Places.jsx
│   └── ProgressBar.jsx
│
├── App.jsx
├── data.js
├── loc.js
├── index.css
└── main.jsx
```

## ⚙️ How It Works

### 1. Load Available Places

The application imports a list of available places from `data.js`.

```js
import { AVAILABLE_PLACES } from './data.js';
```

### 2. Detect User Location

The browser's Geolocation API is used to get the user's current latitude and longitude.

```js
navigator.geolocation.getCurrentPosition((position) => {
  ...
});
```

The places are then sorted based on their distance from the user's location.

### 3. Select a Place

When a user selects a place, it is added to the personal collection.

The application also prevents the same place from being selected more than once.

### 4. Save Data

Selected place IDs are stored in localStorage:

```js
localStorage.setItem(
  'selectedPlaces',
  JSON.stringify([id, ...storedIds])
);
```

When the application starts, the stored IDs are retrieved and used to restore the selected places.

### 5. Remove a Place

When a user clicks a selected place, a confirmation modal is displayed.

The user can either:

* Cancel the deletion
* Confirm the deletion
* Wait for the 3-second timer to automatically confirm

### 6. Modal and Portal

The confirmation dialog uses the HTML `<dialog>` element and React's `createPortal()` to render the modal into a separate DOM element.

## 🧠 What I Learned

Through this project, I practiced:

* Managing state with `useState`
* Handling side effects with `useEffect`
* Using `useRef` for mutable values
* Using `useCallback` for stable callback functions
* Working with browser APIs
* Using Geolocation
* Persisting data with localStorage
* Creating reusable React components
* Passing data and functions through props
* Using React Portals
* Working with HTML dialogs
* Managing timers with `setTimeout`
* Managing intervals with `setInterval`
* Cleaning up timers and intervals
* Working with JavaScript array methods such as `map`, `filter`, `find`, and `some`

## 🚀 Getting Started

### Prerequisites

Make sure you have Node.js installed on your computer.

### Installation

Clone the repository:

```bash
git clone https://github.com/SENAYIT/reactjs_vite_Project_7_PlacePickerforVisit.git
```

Navigate to the project directory:

```bash
cd reactjs_vite_Project_7_PlacePickerforVisit
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Open the local development URL provided by Vite in your browser.

## 📌 Future Improvements

Possible improvements for the project include:

* Add search functionality for places
* Add categories for different types of destinations
* Add a map view
* Add more detailed information about each place
* Add authentication and user accounts
* Store places in a backend database instead of localStorage
* Add responsive design improvements
* Add animations and transitions

## 👩‍💻 Author

**Senayit Awoke**

Frontend Developer | Computer Engineering Graduate

### Connect With Me

* GitHub: https://github.com/SENAYIT


---

⭐ If you find this project useful, feel free to give it a star!
