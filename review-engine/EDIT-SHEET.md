# Review Engine v1.0 — Edit Sheet (read this first, not the code)

**What it is:** a one-file tool that helps a small business ask every customer for a Google review right after the job. The owner sets it up once (business name, Google review link, their name), then per job: type the customer's first name + mobile, tap once, and a ready-made request text opens in the phone's own Messages app. The owner presses send. Nothing is ever sent automatically.

**What each part does**
- Card 1 Setup — saves the business details on the device only (browser local storage).
- Card 2 Request — builds the text, opens Messages (sms: link), or copies the text.
- Numbers + Card 3 Log — every sent request is logged with date; a nudge (reminder) text is offered after ~2 days; owner marks reviews in by hand.
- Card 4 Templates — copy-paste replies for 5-star, 4-star, and low reviews (low-star template routes to a private make-it-right message).
- Card 5 QR — loads a QR maker online, on demand only, to print a counter card. Offline it says so.
- Phase 2 card — two grey buttons (automatic texting; auto-fetch of Google reviews). They are tappable and explain themselves; they do nothing else. They light up when the business joins the Answer Plan platform.
- First-run test panel — the standing Button Log walkthrough + in-app analysis; export is user-tap only. STRIP this panel (and its stored test data) from a client's final build after their test export is in hand; the removal rule is in Max Cave Rules, Part 1D.
- About card — the can't-do list lives in the app itself.

**What can change, and how**
- Wording of the request/nudge/templates: edit the text in the labelled spots (buildMsg + the three template blocks).
- Reminder delay: the `due()` function, currently 2 days.
- Prices/branding: the header and footer text.

**Can't do (honest):** send texts by itself; read Google reviews; work the QR offline; see whether a text arrived. All four are stated in the app.

**Files:** index.html (the app), review-engine-prelaunch-test.html (run BEFORE shipping to any client), icons + site.webmanifest (baked in per the icon rule).
