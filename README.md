# SwingStakes — Multi-Page File Structure

## Files

| File | Description |
|------|-------------|
| `index.html` | Home page (quick start, join round) |
| `setup.html` | Round setup — all betting games configuration |
| `score.html` | Live score entry per hole |
| `board.html` | Leaderboard, settle-up, banker history |
| `rounds.html` | Saved past rounds |
| `events.html` | Tournaments / events management |
| `bets.html` | Bets reference guide (all games explained) |
| `stats.html` | Player stats & handicap tracking |
| `shared.css` | All styles (shared across every page) |
| `shared.js` | All app logic (shared across every page) |

## How it works

Each page is a standalone HTML file that loads `shared.css` and `shared.js`.
The navigation bar uses `<a href="...">` links between pages.
All game state is persisted via localStorage and Supabase, so switching pages doesn't lose data.

## Betting games (configured in setup.html)

- **Skins** — lowest score on a hole wins the skin
- **Nassau** — front 9 / back 9 / total with Huckle side bets
- **Stroke play** — total stroke pot
- **Banker** — rotating banker sets per-hole bets with presses
- **Vegas** — 2v2, combine scores into a 2-digit number
- **Dynamic Vegas** — Vegas with rotating partnerships each hole
- **6's (Round Robin)** — 4-player rotating team best ball
- **Captain (Wolf)** — captain picks partner or goes Lone Wolf
- **Match play** — individual 1v1
- **Team match play** — even teams, best ball per hole
- **Team low ball** — even teams, best ball total
- **Par 3 Greenie** — closest to pin on par 3s (with Buddy Fucker)
- **Junk** — Greenies, Sandies, Polies, Barkies, Snakes, Arnies, Chip-ins
