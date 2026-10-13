# Smart Intersection

An interactive simulation of a demand-responsive traffic signal that stays dark until a connected car or pedestrian is on the way, then serves only the direction with demand.

**Live site:** https://ludomelodia.github.io/smart-intersection/

It builds on two science-fair research projects by Ludovica Melodia:

- **A Traffic Light Model to Save Energy (2023).** An Arduino Uno WiFi Rev2 signal that turns on only while a phone is connected over Bluetooth Low Energy. Ten field trials gave an average connect distance of 9.87 m and disconnect distance of 13.35 m.
- **A Model for Smarter Urban Intersections (2024).** Two Arduinos communicating over MQTT. A GPS module reports speed, and the signal tells walkers from drivers using a 5 mph (2.2352 m/s) cutoff, serving whichever arrives first.

## What the simulation shows

- Pick a start time, run length (1 minute to 24 hours), street type and speed (real time up to 600×).
- Watch live signal draw, cumulative energy against an always-on signal, and the share of each interval the signal was lit.
- **Ideal connected signal** (default): every road user shares position and speed, so the signal wakes about 7 s before a car reaches the stop line and the car arrives on green.
- **Measured prototype**: uses the trial results instead (9.87 m Bluetooth range, fixed green, measured GPS speed noise).

Energy counts lamp power only (eight LED heads, 6 to 22 W each). Traffic volumes are illustrative daily curves, not counts from a real intersection.

## Running it

It is a single static page with no build step. Open `index.html` in a browser.
