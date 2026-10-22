# VKT Cart Lock

English | [中文](languages/README_zh.md) | [Deutsch](languages/README_de.md) | [Español](languages/README_es.md) | [日本語](languages/README_ja.md) | [Français](languages/README_fr.md)

**A hard cooling-off lock for your cart.** Click checkout and the timer starts. Checkout stays blocked until the timer ends, then opens on its own.

Also known as **冷静锁** in Chinese.

> Chromium · Manifest V3 · 6 languages · No tracking · Local-first

---

## Why VKT Cart Lock?

Most "impulse buying" tools leave the door open: snooze, skip, unlock early. VKT Cart Lock does not. The point is to protect the decision you already made from the version of you who is staring at a checkout button at midnight.

- **No skip, no snooze, no early unlock.** Uninstalling the extension is the only way around it.
- **The timer keeps running off the page.** Close the tab, restart the browser, come back tomorrow: the lock is still there.
- **Expiry is silent by default.** Checkout simply opens again. Premium can add one final confirmation.
- **A completed purchase starts a new lock.** Buying does not reset the habit.
- **Local first.** Timers, settings, messages and statistics stay in your browser. No analytics, no ads, no browsing history leaves the device.

---

## Features

### Free

| Feature | Description |
|---------|-------------|
| Hard checkout lock | Clicks, checkout links, form submits and checkout pages are intercepted |
| 24 site presets + generic matching | Hand-tuned rules for major stores, plus text and selector fallbacks everywhere else |
| Cooldown presets | 1 hour, 6 hours, 24 hours or 72 hours |
| Site-wide timers | One active lock per site, started by the first checkout click |
| Custom messages | Up to 20 lines, with fixed, rotating or random display |
| Three sounds | Thud, chime or soft, plus a mute switch |
| Small-order exemption | Let essentials under a chosen amount pass |
| Allowlist and force-lock sites | Skip a trusted shop, or force the guard onto a small independent store |
| Sale quiet period | Black Friday, Prime Day and Double 11 automatically extend the cooldown to 72 hours |
| Password-protected settings | A 4–8 character PIN gates the settings page |
| Emotion tags | Tag the moment — late night, sale, angry, bored, just want it |
| Misblock feedback | Mark a false positive and exclude that element next time |
| Badge countdown | The toolbar icon shows hours or minutes left |
| Ledger basics | Total checkouts blocked and the amount held, including the current month |

### Premium

| Feature | Description |
|---------|-------------|
| Custom cooldowns | Anywhere from 10 minutes to 30 days |
| Item-scoped timers | One lock per product instead of per site |
| Add-to-cart start | Start the timer when an item enters the cart |
| Unlimited messages | Bounded only by the cross-device sync budget (roughly 60 lines) |
| Quiet hours | No sound during chosen hours; the lock still works |
| Confirm after expiry | One final "I still want it" click after the timer ends |
| Cross-device sync | Settings and timers follow your Chrome / Edge account |
| 12-month reports | Monthly trend, site ranking and emotion breakdown |
| CSV export | Take the history into a spreadsheet |
| JSON backup | Full export and import of settings, messages, timers and statistics |

Premium activation is optional. Everything above the Premium line works without an account or a license key.

---

## How It Works

1. **First checkout click.** The guard intercepts the click, starts the timer and shows the lock screen. The order is not submitted.
2. **Every attempt after that.** The checkout stays blocked, and the overlay counts down the remaining time.
3. **The timer is authoritative.** It lives in extension storage, not in the tab. Closing the page, reopening the shop or restarting the browser does not shorten it.
4. **When time is up.** The lock releases silently and checkout is allowed again. Premium users can require one confirmation click first.
5. **After a purchase.** A completed order starts a fresh cooldown, so the next purchase goes through the same pause.

The guard works only in the page. It never hooks network requests and never touches payment iframes or payment-provider pages (Stripe, PayPal, Adyen, checkout.com, Braintree and similar hosts are excluded).

---

## Install

1. Open `chrome://extensions/` in Chrome or `edge://extensions/` in Edge.
2. Turn on **Developer mode**.
3. Click **Load unpacked** and select this folder.
4. Pin the extension to the toolbar.

For a packaged build, use the zip in `publish/` or load the folder manually during development.

---

## Usage

- **Set a cooldown.** Open the extension options and choose a preset, or a custom duration with Premium.
- **Write your own line.** The lock screen can show your words instead of the built-in quotes. Rotating mode keeps it from becoming wallpaper.
- **Add rules.** Allowlist a grocery site, force the lock on a small shop, or exempt orders below a set amount.
- **Watch the badge.** The toolbar countdown is the quiet reminder that the lock is still on.
- **Review the ledger.** The dashboard shows what was blocked, what it would have cost, which sites and moods trigger the most checkouts, and a 12-month trend.
- **Back up (Premium).** Use JSON export before changing machines. Sync restores settings and timers, but local statistics do not travel.

Uninstalling the extension clears its local data. If Premium sync is enabled, messages and settings return after reinstalling; statistics and local history do not.

---

## Supported Sites

Hand-tuned presets cover 24 stores, including Amazon, eBay, Etsy, Walmart, Target, Best Buy, Home Depot, Lowe's, Newegg, Wayfair, Mercari, AliExpress, Temu, Alibaba, DHgate, Shopee, Lazada, Rakuten, SHEIN, TikTok Shop, bol.com, Allegro, Otto and Cdiscount.

Any other store is covered by generic checkout-button text and selector matching. If a site changes its markup, the self-check note in the popup tells you the guard may need another look.

---

## Supported Browsers

| Browser | Status |
|---------|--------|
| Google Chrome | Fully supported |
| Microsoft Edge | Fully supported |
| Other Chromium-based browsers | Should work |

---

## Data and Privacy

- **Stored locally:** settings, timers, statistics, self-check notes, the optional settings PIN (salted SHA-256 hash only) and the Premium license record.
- **Synced (Premium, opt-in):** settings, custom messages and slim timer records through `chrome.storage.sync`. The settings PIN is never synced.
- **Sent to the license server:** only when activating, validating or deactivating Premium — the license key, a random installation ID, the plugin ID and basic browser metadata (browser version, language, timezone, user agent).
- **Not collected:** page content, browsing history, cart contents, payment details, keystrokes or analytics.

There is no account, no advertising and no data sale. Uninstalling the extension removes local data; server-side license records can be removed by deactivating the license first.

See [privacy-policy.html](privacy-policy.html) for the full policy.

---

## Permissions

| Permission | Why it is needed |
|------------|------------------|
| `storage` | Save settings, timers and statistics locally; sync them for Premium |
| `alarms` | Keep the countdown accurate and release locks on time |
| `notifications` | Show a local desktop notice when a new lock starts |
| `host_permissions: <all_urls>` | Detect a checkout button on any shop, since stores use arbitrary domains |
| `host_permissions: api.annmax1983.com` | Activate and validate an optional Premium license |

The content script runs in all frames so it can catch checkout buttons inside storefront widgets, but payment-provider hosts are explicitly excluded.

---

## Languages

English, 简体中文, 日本語, Deutsch, Español and Français. The interface, built-in quotes and store descriptions are localized.

---

## License

VKT Cart Lock is a commercial extension. The Free tier is usable without a license. Premium features require an active license key from [annmax1983.com](https://www.annmax1983.com/).
