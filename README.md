# Itch.io Embed Game

This project is for embedding an itch.io game.

## Change Log

- Created `index.html` to embed the "STONE" game from itch.io.
- **2023-10-27:**
  - Renamed `index.html.html` to `index.html` for correctness.
  - Investigated an issue where the `iframe` was blocked by `itch.io`.
  - Added `referrerpolicy="no-referrer"` to the `iframe` as a potential fix.
- **2023-10-27 (Update):**
  - Confirmed the "STONE" game does not allow embedding.
  - Switched to "Celeste Classic" as an example game that allows embedding.
- **2023-10-27 (Final Test):**
  - Confirmed `itch.io` platform has strict embedding policies, blocking even Celeste Classic on Vercel.
  - Switched to "Pac-Man" from `ClassicReload.com` to successfully test the `iframe` functionality.
- **2023-10-27 (Root Cause Analysis):**
  - Analyzed the Vercel deployment and confirmed servers are sending `X-Frame-Options: SAMEORIGIN`.
  - Switched to the open-source "2048" game, which has no embedding restrictions, as a final working solution. 