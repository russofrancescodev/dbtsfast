# dbtsfast

Independent glucose monitoring prototype, built with Expo for iOS and Android.

## What this is
A demonstration prototype to show a new user experience for glucose monitoring:
- Fast, guided activation flow (5 minutes of user interaction in the demo)
- Dashboard refreshing every 20 seconds in the demo
- Clearer trends, time in range, and smarter alarms

## What this is NOT
- This is NOT a medical device.
- It does NOT use Dexcom APIs, accounts, or official apps.
- All data in the prototype is SIMULATED for demonstration purposes.
- It must NOT be used on real patients or for treatment decisions, including insulin dosing.
- A real reduction in sensor warm-up time would require validation and sensor changes by the sensor manufacturer, plus clinical and regulatory approval.

## Architecture
- One Expo project for iOS and Android.
- Abstract data layer (IDataSource): the UI only talks to this interface.
- MockSensorSimulator: generates realistic simulated glucose data locally, offline.
- RealSensorAdapter: empty, documented interface that a sensor manufacturer could implement later, without changing the UI.

## Status
Initial setup only. The full Expo app code is not yet in this repository.
