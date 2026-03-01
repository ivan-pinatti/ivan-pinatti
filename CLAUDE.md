# ivan-pinatti — Claude Project Memory

## What This Repo Is

GitHub profile README repo (`ivan-pinatti/ivan-pinatti`). Contains the public profile README and cryptocurrency donation assets.

## Key Files

| File | Purpose |
|------|---------|
| `README.md` | Profile page with social badges and crypto donation QR table |
| `docs/crypto/addresses.md` | Full address + QR table for all coins and tokens |
| `docs/crypto/qr-codes/*.png` | QR code images (one per coin/chain) |

## Crypto Donation Section

### Coin Order
README.md table columns: BTC, ETH, XMR, XRP, then alphabetical (ADA, ATOM, BCH, BNB, DOGE, KAVA, LTC, TRX), ZEC last.
Total: 13 coins.

### Multi-Token Addresses
Some addresses cover multiple tokens on the same network:
- ETH address (`0x7F49...`): ETH, USDT (ERC-20), USDC (ERC-20) — reuse `eth.png`
- BNB address (same `0x7F49...`): BNB, USDT (BEP-20), USDC (BEP-20) — reuse `bnb.png`
- TRX address (`TWaZDQ...`): TRX, USDT (TRC-20), USDC (TRC-20) — reuse `trx.png`

README.md shows one column per coin/chain (13 columns, `width="120"`).
addresses.md lists every token as a separate row (19 rows, `width="200"`), grouped by network.

### QR Code Assets
- All PNGs in `docs/crypto/qr-codes/` are standardised at **500x500 px**
- Generated via `https://api.qrserver.com/v1/create-qr-code/?size=500x500&data=<ADDRESS>`
- When adding a new coin, always download at 500x500 to match the rest

### HTML Display Widths
- `README.md` table: `width="120"` for all coins
- `docs/crypto/addresses.md` table: `width="200"` for all coins

### Image URL Patterns
- `README.md` uses **relative paths**: `docs/crypto/qr-codes/{coin}.png`
- `addresses.md` uses **raw GitHub URLs**: `https://raw.githubusercontent.com/ivan-pinatti/ivan-pinatti/main/docs/crypto/qr-codes/{coin}.png`

### Blockchain Labels (addresses.md columns)
Table has 4 columns: `| Currency | Network | Address | QR Code |`
Currency column: just the coin name, no network suffix.
Network column: blockchain or token standard.

| Coin | Network |
|------|---------|
| BTC | Bitcoin |
| ETH | ERC-20 |
| USDT (ERC-20) | ERC-20 |
| USDC (ERC-20) | ERC-20 |
| XMR | Monero |
| XRP | XRP Ledger |
| ADA | Cardano |
| ATOM | Cosmos Hub |
| BCH | Bitcoin Cash |
| BNB | BEP-20 |
| USDT (BEP-20) | BEP-20 |
| USDC (BEP-20) | BEP-20 |
| DOGE | Dogecoin |
| KAVA | Kava |
| LTC | Litecoin |
| TRX | TRC-20 |
| USDT (TRC-20) | TRC-20 |
| USDC (TRC-20) | TRC-20 |
| ZEC | Zcash |

## User Preferences

- Do NOT add "Co-Authored-By: Claude" to commit messages (ever)
- Use conventional commits format (e.g. "feat: ...", "fix: ...", "chore: ...")
- No em-dashes in prose; use commas or parentheses instead
