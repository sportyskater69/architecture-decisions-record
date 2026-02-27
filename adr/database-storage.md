# Architecture Decision Record: Database Storage Strategy

## [Title]
Database Storage Strategy for "Anti Cooked" Mobile App

## [Status]
Accepted

## [Context]
We are building "Anti Cooked," a React Native student planner app for iOS and Android. To keep students on track, we need a reliable way to store their schedules, tasks, and deadlines. While offline local storage was initially on the radar, literally everyone has internet access 24/7 these days. Trying to build out local storage and manage complex data synchronization is totally unnecessary for our target audience and would just drag out the project timeline.

## [Decision]
We are implementing a **Remote Database** (e.g., Firebase Cloud Firestore, Supabase, or AWS) and entirely skipping offline/local database storage. All user data will be stored in the cloud, and the app will require an active internet connection to fetch, push, and update planner tasks.

## [Consequences]
* **What becomes easier :** Development speed goes way up. We don't have to build complex synchronization logic, resolve data conflicts, or worry about encrypting a local database. Plus, if a user switches phones or logs in on a different device, their data is instantly right there.
* **What becomes more difficult :** The app strictly requires an internet connection to function. If a student is totally off the grid, they can't access their planner. We will also need to build in some solid error handling and loading states for weak network vibes so the app doesn't just crash when the Wi-Fi drops.