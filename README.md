# 🇲🇾 Car & Home Loan Calculator

A single-file HTML loan calculator for Malaysian **car** and **home** loans. Compare your normal repayment against paying a bit extra each month — and see how much interest and time you save.

## Open it

Just open [`car-loan-calculator.html`](car-loan-calculator.html) in any browser. No install, no internet, no dependencies.

```bash
open car-loan-calculator.html
```

## What it does

- **Three presets** — pick one, defaults fill in (tenure defaults to the legal max):
  - **Car · Reducing** — reducing-balance amortisation (max 9 years)
  - **Car · Flat Rate** — flat-rate hire purchase, how banks actually quote car loans (max 9 years)
  - **Home** — reducing-balance amortisation (max 35 years)
- **Normal vs With Extra** side by side: monthly payment, tenure, total interest, total paid.
- **You save**: interest saved (RM) and time saved (years/months) from your extra monthly payment.
- **Year-by-year balance** table showing the loan shrink faster with extra payments.

## The methods

- **Reducing balance** — interest is charged on the *remaining* balance each month. Extra payments cut principal, so they save both interest and time.
- **Flat rate** — interest is charged once on the *full* original amount and fixed for the whole tenure. Paying extra each month saves **nothing** (the calculator shows RM 0 saved on purpose). The only way to save is early settlement, where the bank rebates unearned interest via the **Rule of 78** — the year-by-year table shows the settlement figure.

> ⚠️ Flat and reducing rates aren't on the same scale. A ~2.9% flat rate ≈ ~5.4% reducing (effective). Compare **total interest**, not the rate number.

## Editing

Everything (HTML, CSS, JS, the loan math) lives in one file. Defaults and tenure caps are in the `PRESETS` object near the bottom of the `<script>`.
