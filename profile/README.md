<p align="center">
  <img src="https://raw.githubusercontent.com/nathansouz4/trackash-selfhosted/main/public/favicon.svg" alt="Trackash" width="96" height="96">
</p>

<h1 align="center">Trackash</h1>

<p align="center">
  Open-source personal finance dashboard for Brazil: bank accounts, credit cards and investments
  in one place,<br>with the analysis the bank apps don't give you.
</p>

<p align="center">
  <a href="https://github.com/nathansouz4/trackash-selfhosted/blob/main/LICENSE"><img alt="License: AGPL v3" src="https://img.shields.io/badge/license-AGPL--3.0-047857"></a>
  <img alt="Open Finance via Pluggy" src="https://img.shields.io/badge/Open%20Finance-Pluggy-047857">
  <img alt="Self-hosted" src="https://img.shields.io/badge/self--hosted-yes-555555">
</p>

---

Trackash reads your bank accounts, credit cards and investments through Open Finance
([Pluggy](https://pluggy.ai), read-only) and shows what the bank apps don't show together:

- **Cash flow**: every inflow and outflow by month, including Pix and bank debits, with no double
  counting of transfers between your own accounts.
- **Credit cards**: the open bill computed from unbilled transactions, closed bills, installment
  plans and future commitments.
- **Investments**: time-weighted return, volatility, concentration, a portfolio health radar, and
  stock/FII average cost and income from the B3 statement.
- **Privacy mode**: one click blurs every amount on screen.

The interface is in Brazilian Portuguese. The code and docs are in English.

## Get started

Trackash runs on your own computer, with your own Pluggy credentials (free for personal use via
[Meu Pluggy](https://meu.pluggy.ai)). Everything stays in a local SQLite file: there is no
Trackash server, no account and no cloud database.

```bash
git clone https://github.com/nathansouz4/trackash-selfhosted.git
cd trackash-selfhosted
npm ci
npm run dev       # http://localhost:3000
```

A step-by-step setup in the app takes it from there. The full guide is in
[docs/SETUP.md](https://github.com/nathansouz4/trackash-selfhosted/blob/main/docs/SETUP.md).

| Repository                                                                    | What it is                                         |
| ----------------------------------------------------------------------------- | -------------------------------------------------- |
| [trackash-selfhosted](https://github.com/nathansouz4/trackash-selfhosted)     | The open-source edition you run on your machine.   |

## Principles

- **Your data stays with you.** Data moves only between your computer and Pluggy.
- **Read-only.** Trackash never moves money. It keeps no CPF/CNPJ and only the last 4 digits of
  account numbers.
- **Security first.** Strict CSP, CSRF protection, `no-store` caching, and the app answers only on
  `localhost`.

Built with TanStack Start (React 19), Tailwind v4 + shadcn/ui, Recharts and SQLite.

> [!IMPORTANT]
> Trackash is a personal tool, **not investment advice**, and is not affiliated with Pluggy, B3 or
> any bank.
