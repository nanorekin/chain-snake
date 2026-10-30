# Chain Snake

A free, single-file browser snake game with a crypto twist: every coin you collect adds a link to your chain, and every link shows a different ticker (XNO, BTC, ETH, LTC, XMR, SOL, ADA, DOGE, XRP, BNB, DOT, TRX, repeating). No build step, no backend, no fees.

## Play

- **Steer** with the arrow keys or WASD, swipes on the board, or the on-screen pad on phones. Space or P pauses. The game also pauses if you switch tabs.
- **Classic:** walls and your own chain are deadly.
- **Wrap:** walls wrap around, only your own chain is deadly.
- **Daily:** walls are deadly and the coins appear in the same order for everyone, new every day at 00:00 UTC. Collect 20 coins to clear it and keep your daily streak.
- **Nano bonus coin:** a glowing XNO coin appears every so often and fades after 8 seconds. It is worth 3 coins and gives 4 seconds of slow motion.
- **Speed** rises as you collect coins.
- **Ranks:** Paper Hands, Hodler (8 coins), Diamond Hands (16), Whale (25), Satoshi (40).

Everything is stored in the player's browser.

## Deploy on GitHub Pages

1. Create a new repository, for example `chain-snake`.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Open **Settings > Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. After a minute the game is live at `https://<your-username>.github.io/chain-snake/`.

## Donations

The tip card works the same way as in the other Feeless games:

- A `nano:` payment link with the chosen amount, shown as a QR code and an **Open in wallet** button.
- A **Copy address** button.
- An **I've sent it, check** button that asks public Nano nodes whether a matching payment arrived, and unlocks the supporter chain skins (Gold, Neon, Mint) on that browser.

To use a different wallet, change `NANO_ADDRESS` near the top of the script in `index.html`. If the public RPC endpoints in `RPCS` ever block browser requests, point them at your own proxy.

The supporter unlock is stored in `localStorage`, so it is a thank-you perk, not secure access control. Coin tickers and colours are used for fun and are not endorsements.

Add `?selftest` to the URL to expose a small `window.__cs` object for automated tests.
