### Module 4: After-Hours Earnings Catalyst Engine (Pre-Open Execution Spec)
**Parent Universe:** Filtered Nifty LargeMidcap 250 Baseline  
**Objective:** Capture next-day institutional earnings gap-ups and intraday momentum rallies at the 9:15 AM open based on verified quarterly financial filings released after market hours (post-3:30 PM IST) or on weekends.

--------------------------------------------------------------------------------

#### 1. Execution Workflow & Daily Trigger Sequence
Whenever a daily signal scan is requested, the agent executes in two sequential layers:
1. **Layer 1 (Core Engine — Master Spec v2.1):** Scans the Nifty LargeMidcap 250 baseline using Option A (`>1.25x` Vol / `>50%` Del for 1A; `>1.5x` Vol / `>55%` Del for 1B/1C) and audits active inventory via the Two-Path Exit Engine.
2. **Layer 2 (Module 4 Overlay — Earnings Catalyst Check):** Scans all Nifty LargeMidcap 250 companies that filed quarterly earnings after the previous market close (or over the weekend) to flag `[PRE-OPEN EARNINGS BUY]` opportunities for the upcoming 9:15 AM open.

--------------------------------------------------------------------------------

#### 2. The Factual Earnings Gate (All 3 Must Pass)
A stock qualifies only when its official NSE/BSE quarterly result filing confirms:
* **Top & Bottom-Line Velocity:** Quarterly Net Profit (PAT) growth **> +25% YoY** AND Revenue growth **> +18% YoY**.
* **Margin & Balance Sheet Integrity:** Operating EBITDA margin expands YoY (or beats consensus estimates) while maintaining **Net Debt-to-EBITDA < 1.5x** (or Net NPA < 0.8% for Financials).
* **Forward Visibility (Catalyst Confirmation):** Positive management commentary, order-book expansion, or capacity ramp-up with no major regulatory/one-off distortions.

--------------------------------------------------------------------------------

#### 3. Pre-Rally Technical Guardrails (Checked Before 9:00 AM Open)
* **Overheat Protection:** Prior session's closing **14-Day RSI must be < 65** (prevents buying into an already exhausted pre-earnings run-up).
* **Valuation Override:** For verified `> +25%` YoY PAT beats, the standard `FCF-Adjusted PEG < 1.00` ceiling is temporarily waived so high-multiple market leaders can trigger.

--------------------------------------------------------------------------------

#### 4. Next-Morning Pre-Open Execution Rules (9:00 AM – 9:20 AM IST)
* **9:08 AM Pre-Open Equilibrium Check:**
  * **Sweet Spot (`+1.5%` to `+5.0%` gap):** Place a **Limit Buy Order at `+0.5%` above the 9:08 AM pre-open price** (hard ceiling at **+5.5% above prior close**).
  * **Excessive Gap (`> +6.0%` gap):** **SKIP / NO ENTRY.** Do not chase vertical morning spikes where intraday upside is already priced in.
* **Event Risk Stop-Loss:** Immediately place a **strict -4.0% stop-loss** below your actual fill price (or below the 9:15 AM opening-range low) to protect against "sell-the-news" fade traps.
