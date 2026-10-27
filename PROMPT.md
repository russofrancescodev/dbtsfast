# Prompt for building the app with Claude

Create an independent glucose monitoring prototype with Expo and React Native, for iOS and Android in a single project. Do NOT depend on Dexcom, do NOT use Dexcom APIs, accounts, or official apps. This is a demonstration prototype to present to Dexcom, with simulated data, NOT a medical device and NOT for use on real patients or for treatment decisions.

Goals to demonstrate:
1. Guided activation flow in 5 minutes of user interaction in the demo.
2. Dashboard refreshing every 20 seconds in the demo, showing only simulated values with their timestamp.
3. Clearer trends, time in range, and smarter alarms.

Architecture: abstract IDataSource interface, MockSensorSimulator generating realistic simulated data locally, and an empty documented RealSensorAdapter that a manufacturer could implement later without changing the UI.

Include: onboarding, dashboard with large current value and trend arrow, 3h/6h/12h/24h charts, time in range, alarms (urgent low <54, low <70, high >180, signal loss, sensor expiring), history and events (meals, insulin, exercise, notes), daily/weekly/monthly PDF reports, presentation mode with DEMO watermark and guided scenarios.

Stack: Expo SDK, React Native, TypeScript, Expo Router, Zustand, expo-sqlite, expo-secure-store, expo-notifications (Development Build, not only Expo Go), EAS Build.

Safety: show a permanent DEMO notice in the app. Do not reverse engineer sensor Bluetooth protocols, do not modify sensor firmware, do not bypass safety controls, and do not claim a real sensor warm-up reduction.
