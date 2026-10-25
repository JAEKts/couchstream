# CouchStream

Streaming services for SteamOS, set up in one go.

CouchStream is a setup app for SteamOS. You run it once in Desktop Mode: it makes sure Google
Chrome is installed, then adds the streaming services you pick to your Steam library. Back in
Gaming Mode, each service launches full screen from your library, ready for a controller.

It is built and tested on the Steam Machine first, then the Steam Deck.

## Status

Early development: there is nothing to install yet. The first step is testing, on real
hardware, that Steam's add-to-library mechanism and Chrome's protected-video playback behave
as expected. The app is built only after those tests pass.

## How it will work

1. Open CouchStream in Desktop Mode.
2. If Chrome is not installed, CouchStream opens Discover on Chrome's page.
3. Pick your services.
4. CouchStream adds one launcher per service to your Steam library, through the same
   mechanism as SteamOS's own "Add to Steam" menu.
5. Return to Gaming Mode, launch a service from your library, and sign in once with the
   on-screen keyboard (Steam + X).

## What it does not do

- It never signs in to services for you or handles your passwords.
- It has no telemetry.
- It does not get around DRM. Video plays through Chrome's own DRM support, which Chrome
  downloads itself, so picture quality is whatever each service allows Chrome on Linux. For
  Netflix, that is up to 1080p.
- It does not use Steam's remote-debugging port or edit Steam's files.

## Requirements

- SteamOS on a Steam Machine or Steam Deck
- An internet connection
- A subscription to each service you add

## Permissions

CouchStream will ship as a Flatpak (`io.github.JAEKts.CouchStream`). Every permission it asks
for will be listed here, with the reason, before the first release.

## Licence

MIT. See [LICENSE](LICENSE).

## Trademarks

CouchStream is an independent project. It is not affiliated with or endorsed by Valve,
Google, or any streaming service. Product and service names are trademarks of their owners
and are used only to identify them.
