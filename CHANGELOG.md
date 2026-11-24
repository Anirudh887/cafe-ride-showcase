# Changelog

What changed in Cafe Ride, newest first. Written from the private repository's history.

## 10 Sep 2026: Platform upgrade

- Moved the phone app to Expo 54 and React 19.
- Fixed typechecking in the phone app's tests.

## 9 Sep 2026: On a real phone, and a new name

- **Renamed the app Cafe Ride**, with its own mark: a cup of coffee with a bicycle wheel in the
  crema, and a launcher icon to match.
- The app now uses its name throughout: the sign-in front door, the "company" screens and arriving
  at a ride.
- **Group rides have a start, a coffee stop and a finish** on the map.
- Fixed problems found by running the app on a real Android phone.
- Rides recorded while offline now upload once the signal returns. The app no longer takes the
  phone's word that a ride was uploaded.
- A ride can be opened before it has left the phone, and remembers which group ride it was part of.
- Distance for a ride recorded on the phone is now measured the same way everywhere.
- From the group rides tab you can find a ride you could join.

## 8 Sep 2026: First rides on a device, and the chalk poster look

- The phone runs on a real Android device, asks for Bluetooth permission, and shows a paired
  sensor's reading before the ride starts.
- A ride streams live into the group ride you've joined.
- Rides can be renamed and deleted, on the web and the phone.
- **Redesigned the web and phone as a chalk poster.** Drawings and handwriting carry the interface,
  the road is the hero of a group ride, and empty states are drawn instead of grey text.
- On the group map, each rider's figures sit beside their dot, "on the front" gets its own mark,
  and the gaps between riders are chalked on the road.
- Rider names are readable in each rider's own colour.
- **Join Me:** open your own ride to company, not only join someone else's. The riding screen says
  when a ride is being shared.

## 5 Sep 2026: Maps

- One chalk-style basemap, self-hosted and shared by the web and the phone.
- Group and replay routes are drawn on the basemap.
- The phone shows the group map.

## 4 Sep 2026: Watching group rides live, and a structural tidy-up

- **Watch a group ride live on the phone**, over a WebSocket.
- Late starters now appear in a live group view.
- A simulator demo streams a whole group ride, so it can be watched without bikes.
- The Android build completes on Windows.
- Real PostgreSQL support, alongside the in-process development database.
- Large internal consolidation: one way to authenticate, one live event stream, one way for the web
  to reach the server, and one place the phone formats numbers and dates. Behaviour is unchanged,
  with far fewer places for bugs to hide.
- Fixed a share link's elevation following the wrong privacy channel.
- Handover docs for setting the project up on another machine.

## 3 Sep 2026: Basemap and reference docs

- The web draws rides on a self-hosted basemap and falls back when it's absent.
- Reference documents typeset as PDFs.
- Finished rides are closed automatically, and guessing a share link is made costly.
- Fixed three blockers found while building the first Android app package.

## 2 Sep 2026: First version

- **Live telemetry end to end:** the phone pairs Bluetooth sensors and GPS, records with the screen
  off, and streams to a private share link that updates as you ride.
- **Group riding:** a live map of the whole group, who is on the front, replay and highlights.
- Clubs, profile pictures, and riders choosing what they share with a group.
- FIT and GPX import.
- Sign-in on the web (cookie-based) and on the phone, with the same five sections in each.
- The chalk-on-road design system, shared by the phone and the web.
- Desktop preview of the phone screens.
- Error reporting: the web no longer shows a blank page on errors, and riders can file a report that
  shows exactly what it contains.
- Architecture, data-model and product write-ups.
