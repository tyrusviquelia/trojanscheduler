# Privacy Policy — Trojan Schedule Helper

**Effective date:** August 14, 2026
**Developer:** Tyrus Viquelia — USC '28 (unofficial student project)

Trojan Schedule Helper is a browser extension that adds professor ratings, seat availability, schedule tools, and planning features to USC's public class-search and Web Registration pages. It is built to work entirely inside your own browser.

## The short version

The developer collects **nothing**. There are no analytics, no trackers, no developer-operated servers, and no accounts. Everything the extension knows lives in your own browser's extension storage, and the only network requests it makes are the ones needed to show you ratings and seat counts.

## What the extension stores (in your browser only)

Using Chrome's extension storage (`chrome.storage`), the extension saves:

- **Your settings** — which features are toggled on or off.
- **Your degree plan** — courses you import or add in the planner, your GE placeholder slots, and your unit-progress numbers.
- **Your captured schedule** — course codes, section numbers, meeting times, locations, units, and instructor names read from your own myCourseBin/WebReg pages while you view them. This powers schedule-conflict flags, the calendar export, and the rigor analyzer.
- **Your watchlist** — sections you chose to watch for open seats, plus their last-checked status.
- **A ratings cache** — public RateMyProfessors results, cached temporarily so pages load faster.

Settings and your degree plan may sync between your own devices through your browser's built-in sync (`storage.sync`), which is operated by your browser vendor under their privacy policy — not by the developer. Everything else stays on the device. Removing the extension deletes this data; the popup's "Clear cache" button clears the ratings cache on demand.

## Network requests the extension makes

The extension talks to exactly four services, each for one visible purpose:

1. **ratemyprofessors.com** — when a USC page you're viewing lists an instructor, the extension sends that instructor's name (and USC's school identifier) to RateMyProfessors' public API to fetch their public rating, difficulty, would-take-again percentage, and review tags. No information about you is included in these requests.
2. **classes.usc.edu** — the extension checks USC's public Schedule of Classes API for seat counts of sections on your watchlist (about every five minutes while your browser is open).
3. **catalogue.usc.edu** — the extension only adds an "Import into planner" button on catalogue pages you open yourself; the import reads the page content locally in your browser. 
4. **api.web3forms.com** — *optional, off by default.* If you enable email alerts, you paste your own Web3Forms access key, and when a watched seat opens the extension sends the alert (course code, section, and seat count) through Web3Forms to the inbox associated with **your** key, under Web3Forms' privacy policy. If you never enable email alerts, this service is never contacted.

Your USC pages are read through your own existing login session. The extension never sees, stores, or transmits your USC password, student ID, grades, or any personal records.

## What the developer never does

- No collection of personal information, browsing history, or usage analytics.
- No selling, sharing, or transferring of any data to anyone.
- No remote code — all code ships inside the extension package.
- No changes to this behavior without updating this policy and the store listing.

## Your choices

Every feature that stores or fetches data can be turned off in the popup. You can clear the ratings cache at any time, remove watched sections individually, and uninstalling the extension removes all stored data.

## Contact

Questions about this policy: **tyrus.viquelia1@gmail.com**

*Trojan Schedule Helper is not affiliated with, endorsed by, or supported by the University of Southern California, RateMyProfessors, or Web3Forms.*
