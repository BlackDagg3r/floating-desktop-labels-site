# Trip companion (VPS → ATL → EZE, Sept 4–5, 2026)

Single-file, phone-first web page used as a live travel companion. Not linked from the
product site; kept here so it is versioned and deployable at `/trip-companion/`.

What it does
- Countdown strip driven by itinerary times you enter (saved in localStorage).
- Guide mode: `watchPosition` geofences for VPS, ATL (concourse detection by longitude,
  with a one-tap calibration offset), EZE Terminal A, and the Riccheri highway out of EZE.
- Clock + position rules: "start moving" and "you'll miss boarding" alerts when boarding is
  near and the phone is on the wrong concourse or stationary.
- EZE arrival step tracker, Argentina entry/customs/money/transport knowledge base,
  ATE-ANAC strike status, checklists, and iOS Shortcuts recipes for background geofences.
- "Ask the assistant" uses the claude.ai artifact `sample` capability with the embedded
  knowledge base plus current zone/countdown as context.

Known limits
- Safari only tracks location while the page is in the foreground; background alerts come
  from the iOS Shortcuts automations and Google Calendar reminders described on the page.
- ATL concourse longitudes are approximate; calibrate once at any gate sign.
