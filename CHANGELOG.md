# Changelog

Newest first.

## 10 Sep 2026

- Upgraded the phone app to Expo 54 and React 19.
- Fixed a type error in the phone app's tests.

## 9 Sep 2026

- Renamed the app from Cadence to Cafe Ride. It has a new logo too, a coffee cup with a bike wheel
  in the crema, plus a matching app icon.
- Updated the landing page and the rest of the app to use the new name.
- Group rides can now have a start, a coffee stop and a finish on the map.
- Fixed a batch of bugs I found running the app on my phone.
- Rides recorded with no signal now upload once you're back online. The app also checks with the
  server instead of assuming an upload worked.
- You can open a ride before it has finished uploading.
- Rides remember which group ride they were part of.
- Distance is now worked out the same way everywhere.
- The group rides tab shows rides you can join.

## 8 Sep 2026

- Got the app running on a real Android phone. It now asks for Bluetooth permission and shows your
  sensor readings before you start.
- Rides now stream into the group ride you've joined.
- You can rename and delete rides, on the web and on the phone.
- New look across the web and the phone, mostly drawings and handwriting instead of plain boxes.
- On the group map, each rider's numbers now sit next to them, the rider on the front gets a marker,
  and the gaps between riders are drawn on the road.
- Rider names were hard to read in some colours. They're readable now.
- You can open your own ride for others to join, not just join someone else's. The ride screen shows
  when your ride is being shared.

## 5 Sep 2026

- Added my own map style, used by both the web app and the phone.
- Group rides and replays are drawn on the map.
- The phone shows the group map too.

## 4 Sep 2026

- You can watch a group ride live on the phone.
- Riders who start late now show up in the live view.
- The simulator can play out a whole group ride, so I can test it without other riders.
- The Android build works on Windows now.
- Added support for a real PostgreSQL database.
- Cleaned up a lot of the internals, mostly merging duplicate code into one place. Nothing changes
  for users, there's just less to go wrong.
- Fixed a share link showing elevation when it shouldn't have.
- Wrote setup notes for moving to another machine.

## 3 Sep 2026

- Rides on the web are drawn on a map, with a fallback when the map can't load.
- Turned the project docs into PDFs.
- Rides left running are now closed automatically, and share links are harder to guess.
- Fixed three things that stopped the Android app from building.

## 2 Sep 2026

The first version:

- The phone connects to Bluetooth sensors and GPS, records with the screen off, and streams to a
  private link that updates as you ride.
- Group rides with a live map, who's on the front, a replay and highlights.
- Clubs, profile pictures, and a choice of what you share with a group.
- Importing FIT and GPX files.
- Signing in on the web and the phone.
- The chalk design, shared by the web and the phone.
- A way to preview the phone screens on my desktop.
- Better error handling. The web app no longer goes blank on an error, and riders can send a bug
  report that shows exactly what's in it.
- Docs on the architecture and the data model.
