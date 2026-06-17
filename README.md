# Card Maximiser 🇸🇬

**Which Singapore credit card should carry your spending?**

A single-page tool that runs your *real* statements through each card's *actual* earning rules — caps, minimums, exclusions and all — so instead of a generic "best card" listicle, you see what each card would have earned on **your** spending, in miles or cashback.

Everything runs in your browser. No accounts, no servers, no API keys. Your statements never leave your device.

---

## What it does

1. **Pick up to 4 cards** from a built-in catalogue of 15 popular Singapore cards.
2. **See them side by side** — a plain-language table of how each one earns.
3. **Drop in up to 10 PDF statements** — they're read locally and sorted into spending categories you can edit.
4. **Get the verdict** — miles or cashback per card, ranked, with a toggle for how much a mile is actually worth to you, plus a "what those miles can buy" view of real Singapore Airlines trips.

No statements handy? Hit **Try with example data** to see the whole flow with figures for a typical Singaporean (~S$2,000/month).

---

## Supported cards

| Miles | Cashback |
|---|---|
| DBS Altitude Visa | OCBC 365 |
| HSBC Revolution | Citi Cash Back |
| Citi PremierMiles | UOB One *(simplified)* |
| UOB PRVI Miles | UOB Absolute Cashback |
| HSBC TravelOne | Amex True Cashback |
| Standard Chartered Journey | Standard Chartered Simply Cash |
| UOB KrisFlyer *(needs S$1k/yr SIA spend)* | |
| DBS Woman's World | |
| Citi Rewards | |

Card terms were verified against issuer and miles-tracking sources in **mid-2026**. They change often, so treat this as a strong decision aid, not gospel — and re-check the catalogue every few months.

---

## How a mile is valued

A mile is only worth what you redeem it for, so the results use one of three settings:

| Setting | Value per mile | When it applies |
|---|---|---|
| Cash out | ~0.8¢ | KrisPay / statement rebate |
| Economy flights | ~1.5¢ | typical Saver economy redemption |
| Business flights | ~3¢ | premium-cabin sweet spot |

Cashback is guaranteed dollars; miles are only "worth it" above roughly 0.9¢, which the tool spells out as you switch settings.

---

## Privacy

- PDF statements are parsed **entirely in your browser** using [PDF.js](https://mozilla.github.io/pdf.js/).
- Nothing is uploaded, logged, or sent anywhere — there is no backend.
- The only external requests are to a CDN for the PDF.js library and Google Fonts.

---

## Running it

It's one file (`index.html`) with no build step. To use it:

**Locally** — just open `index.html` in any modern browser.

**GitHub Pages**
1. Put `index.html` in the root of a repo.
2. Repo → **Settings** → **Pages** → *Deploy from a branch* → `main` / `root`.
3. Your tool goes live at `https://<your-username>.github.io/<your-repo>/`.

**Netlify** — drag the folder containing `index.html` onto the Netlify dashboard. Done.

---

## Adding or editing a card

Every card lives in one clearly-commented `CATALOG`
