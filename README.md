# The Traitors: At-Home Edition

A single `index.html`. No server, no accounts. Claudia's device runs the game and every phone connects to it directly (WebRTC via PeerJS).

## Put it online (GitHub Pages, about 2 minutes)
1. Create a new public repo, e.g. `traitors`, and upload `index.html`.
2. Go to Settings → Pages → Source: *Deploy from a branch* → `main` / root → Save.
3. Wait about a minute. Your game is at `https://<your-username>.github.io/traitors/`.

## Running the night
1. **Claudia** opens the site and taps **Host a new game as Claudia**. A laptop or tablet that stays plugged in, with the screen on, is best, because it *is* the server.
2. Players scan the QR code (or you share the link) and type their names.
3. Tap names to make them Traitors, or hit **Random**. Then press **Reveal roles to phones**.
4. Loop through the tabs: **Mission** → **Round Table** → **Night** → (dawn reveal) → repeat → **Endgame**.

| Phase | Players' phones | Claudia |
|---|---|---|
| Role reveal | "Do not react… 3 2 1" → TRAITOR / FAITHFUL; Traitors see each other | picks Traitors |
| Mission | rules, goals, prize fund, plus a *hold for private briefing* button for everyone (only Traitors get secret orders) | picks a preset or writes one, ticks goals to add money |
| Round Table | vote buttons, then who-voted-for-whom | opens, locks and reveals votes, then banishes → role reveal on every phone |
| Night | black screen, "close your eyes" (ghosts may watch) | picks murder and/or recruit |
| Dawn | "Do not react… 3 2 1" → *X was murdered* / *No one* / **RECRUITED** | — |
| Endgame | winners, prize fund, everyone's true colours | auto or manual winner |

Players can always **press and hold** to see their role privately.

## Reloading / dropped phones
- Phones remember who they are. Reopen the link and you're straight back in.
- If Claudia's page reloads, the game state is saved and phones reconnect on their own within a few seconds.
- Mistakes: on Claudia's player list, tap a role badge to change it silently, or ☠/↺ to kill/revive.

## Wi-Fi notes
- Everyone needs internet briefly to make the connection (a free public PeerJS server introduces the phones). After that the traffic goes device to device, and the same home Wi-Fi works best.
- Local testing: run `python3 -m http.server 8000` in this folder, then open `http://<your-computer-IP>:8000` (not `localhost`) on the host device and the phones.
- You can test alone with multiple browser tabs or windows. Open each player in a private window so they get separate identities.

## Next version ideas
Seer/Saboteur roles, shields, a TV "big screen" view, sound effects.
