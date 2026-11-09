# Cedar Connect

## Overview

Cedar Connect brings both sides of a rental marketplace into one app. Guests can browse homes and apartments, open a listing, and make a reservation. Hosts can publish rentals, add photos, and review their own listings. The project connects those workflows through a React interface backed by Firebase Authentication and Firestore.

## How it’s built

- **Guest and host flows.** Dedicated screens cover listing details, reservations, account settings, and rental management.
- **Frontend structure.** The app separates forms, listing cards, and page containers, with an auth context and route guards for account features.
- **Data layer.** [Firebase services](src/config/fireBaseServices.js) handle access to users, listings, and rental records. Firebase Storage handles listing photos. [App routes](src/App.jsx) show how the screens fit together.

## Run or explore locally

From the repository root, run `npm install` and `npm run dev`. The source also imports `react-router-dom`, which is missing from the package manifest. Install it locally with `npm install --no-save react-router-dom@6` before starting Vite. To exercise sign-in and reservations with your own Firebase project, configure Authentication, Firestore, and Storage in [the Firebase setup](src/config/fireBaseConfig.js).
