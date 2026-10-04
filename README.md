# proxy provider: how to compare billing models before you pay, and which 9Proxy package fits your workload

Search "proxy provider" and you get a wall of near-identical comparison posts. Big numbers, five stars, a verdict. What almost none of them tell you is what your second invoice will look like — and that is the part that decides whether you keep paying.

So here's the useful version. Below is what actually separates one provider from another, how the three common billing models change your costs, and where 9Proxy sits when you check its published numbers against the same criteria.

## Advertised success rates are not the deciding factor

Provider pages quote 95–99% success rates. Independent, continuous benchmarking tells a different story: on sites that actively block bots, residential proxies typically return real pages somewhere between 55% and 75% on a given day — the gap comes partly from what counts as "success" (a CAPTCHA served with HTTP 200 often gets counted as a win on vendor dashboards).

That's not a reason to distrust any single provider. It's a reason to stop treating a headline success rate as a purchase criterion. Providers in the same tier perform similarly on average, and daily rankings shuffle. What stays stable is the commercial structure: how you're billed, how long an IP lasts, what happens when one dies, and how much work it takes to target a specific city.

## The billing model matters more than the network does

Residential providers sell three shapes of product, and picking the wrong one is where budgets quietly die.

**Per gigabyte.** You buy a block of traffic and every request draws it down. This suits rotation-heavy work where each request pulls down very little: SERP checks, price sampling, ad verification, API polling. It punishes you the moment you scrape JavaScript-heavy pages, because page weight — something you don't control — becomes your cost driver. A project pulling 100,000 pages of 2–5 MB each burns through several hundred GB a month, and vendors generally price entry GB packs at a steep rate before volume discounts kick in.

**Per IP with unlimited bandwidth.** You buy a fixed number of residential IPs. Each one carries as much traffic as you can push through it while it's alive. This is the right shape when bandwidth use is unpredictable or heavy, and it's the model agencies and multi-account operators tend to prefer, because cost is fixed per identity rather than per request.

**Bundles.** A package that includes both IPs and a traffic allowance, sold at less than the two bought separately. Useful when a single project needs sticky sessions for some tasks and wide rotation for others.

If you want to see how those three shapes are actually priced side by side, 👉 [check 9Proxy's live package pricing](https://bit.ly/9-Proxy) before you read the rest — the numbers make the trade-offs concrete.

## What to check before you pay any provider

Six things decide whether a provider fits, and only two of them are usually printed on a landing page.

- **Targeting depth.** Country-level is table stakes. City, state, ZIP and ISP-level targeting is what ad verification, localized SERP work and geo-accurate price checks actually require. If the provider only advertises "90+ countries" without mentioning city or ISP filters, assume country-level only.
- **Session control.** Rotating per request, sticky for a set window, or both. Sticky sessions capped at ten minutes are useless for account work that needs to hold for hours.
- **Protocol support.** HTTP, HTTPS and SOCKS5. SOCKS5 matters if you're feeding anti-detect browsers, proxychains or custom scripts. Accept CONNECT-only or SOCKS5 endpoints — a proxy that terminates TLS will ruin a browser fingerprint.
- **IP lifetime expectations.** Residential IPs come from real devices, so they go offline. A provider that promises a 24-hour IP and delivers three hours isn't lying to you; a provider that refuses to replace the dead ones is a problem.
- **Replacement terms.** This is where cheap providers get expensive. Read the exact window and conditions under which a dead IP is swapped at no cost.
- **Balance mechanics.** Wallet-style credit that doesn't expire is different from a monthly subscription that bills whether you use it or not. Neither is wrong — but they behave very differently in months where your workload drops.

> Uptime claims and pool size are the two numbers providers compete on hardest and that buyers can verify least. Treat both as marketing until you've run your own targets through the network.

## Where 9Proxy sits on those checks

9Proxy is a residential-only provider — no datacenter or static ISP line as of writing — advertising 20M+ residential IPs across 90+ countries, with targeting down to country, state, city, ISP and ZIP code. It supports HTTP, HTTPS and SOCKS5. Uptime is quoted at 99.95%, and a third-party directory, ProxyLook, lists a 97% success rate with an average response time around 1,300 ms and a 3.9/5 rating. Those are directory and vendor figures, not someone's reproducible benchmark, so calibrate accordingly.

The company's distinguishing decision is financial, not technical: it sells packages from a wallet balance rather than a subscription. Unused IP packages don't expire until an IP is actually forwarded, and traffic packages carry a 180-day validity (unlimited on the enterprise tiers). There's no recurring charge sitting there in a slow month.

A few operational details worth knowing:

- **Today List.** If an IP you forwarded earlier comes back online within 24 hours and you forward it again, it doesn't deduct a new IP from your balance. On recurring jobs hitting similar targets, the company estimates this cuts IP consumption meaningfully.
- **Replacement policy.** If an IP fails to connect, 9Proxy's published policy is an immediate replacement after the system confirms it's offline — framed internally as a "60-second" window.
- **IP lifetime.** Typically a few hours up to around 24 hours per IP. That's normal for genuine residential devices, and it's why the per-GB model exists alongside it.
- **Tooling.** A desktop app for Windows, macOS and Linux handles IP-based access (local port forwarding, optional proxy authentication, port binding, connection testing). The GB-based product works straight from the dashboard with username/password or IP whitelisting, so no install. There's also Proxy2Web for browser-based use, ProxyHub for mobile device management, and a public API for balance, usage and share-code management.
- **Teams and resellers.** Sub-accounts and share codes let you split IPs across people or clients without handing over the main login.
- **Support.** 24/7 via Telegram, email and tickets.
- **Payments.** Cards, crypto (USDT, BTC, ETH, LTC, DOGE and others), Alipay, Apple Pay and Google Pay are all listed. Crypto payments have historically carried bonus incentives, and some payment methods carry an extra 5% bonus or discount.

One honest caveat: 9Proxy raised prices on its IP-based and bundle packages on June 1, 2026 — its first adjustment since launch — while leaving GB-based prices untouched. If you're comparing against an older review, the per-IP numbers you're looking at are probably out of date.

## 9Proxy's full package list

Everything currently published, including the tiers most reviews skip:

| Package | Type | What you get | Price | Validity |
| --- | --- | --- | --- | --- |
| 100 IPs | IP-based | 100 residential IPs, unlimited bandwidth per IP | $24 ($0.24/IP) | Unused IPs never expire |
| 500 IPs | IP-based | 500 residential IPs, unlimited bandwidth | $72 ($0.144/IP) | Unused IPs never expire |
| 1,000 + 500 bonus IPs | IP-based | 1,500 residential IPs, unlimited bandwidth | $126 ($0.084/IP) | Unused IPs never expire |
| 2,500 IPs | IP-based | 2,500 residential IPs, unlimited bandwidth | $210 ($0.084/IP) | Unused IPs never expire |
| 5,000 IPs | IP-based | 5,000 residential IPs, unlimited bandwidth | $360 ($0.072/IP) | Unused IPs never expire |
| 15,000 IPs | IP-based | 15,000 residential IPs, unlimited bandwidth | $720 ($0.048/IP) | Unused IPs never expire |
| 25,000 IPs | IP-based | 25,000 residential IPs, unlimited bandwidth | $863 ($0.035/IP) | Unused IPs never expire |
| 50,000 IPs | IP-based | 50,000 residential IPs, unlimited bandwidth | $1,438 ($0.029/IP) | Unused IPs never expire |
| 100,000 IPs | Business IP | 100,000 residential IPs, unlimited bandwidth | $2,300 ($0.023/IP) | Unused IPs never expire |
| 200,000 IPs | Business IP | 200,000 residential IPs, unlimited bandwidth | $4,140 ($0.021/IP) | Unused IPs never expire |
| 500,000 IPs | Business IP | 500,000 residential IPs, unlimited bandwidth | $8,625 ($0.018/IP) | Unused IPs never expire |
| 5 GB | GB-based | Unlimited endpoints, rotating or sticky | $15 ($3.00/GB) | 180 days |
| 50 + 5 GB bonus | GB-based | Unlimited endpoints, rotating or sticky | $105 ($2.10/GB) | 180 days |
| 100 GB | GB-based | Unlimited endpoints, rotating or sticky | $150 ($1.50/GB) | 180 days |
| 200 GB | GB-based | Unlimited endpoints, rotating or sticky | $200 ($1.00/GB) | 180 days |
| 1,000 GB | GB-based | Unlimited endpoints, rotating or sticky | $800 ($0.80/GB) | 180 days |
| 2,000 GB | GB-based | Unlimited endpoints, rotating or sticky | $1,500 ($0.75/GB) | 180 days |
| 3,000 GB | Enterprise GB | Unlimited endpoints, unlimited validity | $2,160 ($0.72/GB) | No expiry |
| 6,000 GB | Enterprise GB | Unlimited endpoints, unlimited validity | $4,200 ($0.70/GB) | No expiry |
| 10,000 GB | Enterprise GB | Unlimited endpoints, unlimited validity | $6,800 ($0.68/GB) | No expiry |
| Starter Bundle | Bundle | 100 IPs + 5 GB | $30 | Traffic valid 180 days |
| Popular Bundle | Bundle | 1,500 IPs + 50 GB | $180 | Traffic valid 180 days |
| Pro Bundle | Bundle | 5,000 IPs + 500 GB | $720 | Traffic valid 180 days |

Purchase links for every tier sit behind the same entry point: 👉 [open the 9Proxy pricing page and pick a package](https://bit.ly/9-Proxy).

## Which tier fits which job

The per-IP ladder drops fast, and the interesting decisions happen at the bottom and the middle.

**Proof of concept or a one-off check.** 100 IPs at $24. You get unlimited traffic, so you can hammer a low-rotation test without watching a meter. If it turns out your job is actually rotation-heavy and light on data, move to the 5 GB or 55 GB pack instead.

**Solo operator, light multi-accounting, a few scraping targets.** 500 IPs at $72. That's enough separate identities for a handful of profiles per platform without paying agency rates.

**Small team, several concurrent projects.** The 1,000 + 500 bonus tier at $126 is the price-per-IP break point — $0.084 against $0.144 at the 500 tier, for less than double the money.

**Agency or reseller managing clients.** 5,000 IPs at $360 covers a real portfolio at $0.072 per IP. Past that, 15,000 and 25,000 tiers exist for people who already know they need them; the 50,000 tier at $0.029 per IP is a volume play, not a starting point.

**Bursty, rotation-heavy work.** SERP monitoring, ad verification and e-commerce price checks belong on GB packs. The 55 GB tier at $2.10/GB is where most people should start, and the 180-day window means you aren't racing a monthly clock.

**Always-on infrastructure.** Above roughly 3,000 GB a month, the enterprise tiers make more sense than stacking 2,000 GB packs, purely because the validity constraint disappears.

**Mixed workloads.** The bundles are the only place 9Proxy discounts the two products against each other — the Pro Bundle throws in 5,000 IPs and 500 GB together. If your project genuinely needs both sticky identities and high-throughput rotation, price the bundle before pricing the parts.

## Limits worth knowing before you buy

A few things the marketing pages gloss over:

- **IP-based access needs the desktop app.** Per 9Proxy's own documentation, the per-IP product authenticates through the app's local port forwarding. The GB product is the one you can run straight from the dashboard with user/pass or whitelisting. If you can't install software on the machine, that decides your model for you.
- **Region density is uneven.** Any 20M-IP network spread across 90+ countries will have thin spots. If you need a specific small market at volume, confirm availability before buying a large pack.
- **Streaming isn't the use case.** Major streaming platforms aggressively block residential ranges, and reviewers have flagged that as a weak spot. If your goal is unblocking Netflix, this is the wrong category of tool.
- **The cheapest tiers aren't reseller tiers.** Wholesale rates and dedicated support come at volume; you won't get agency economics on a 100-IP purchase.
- **Promotions rotate and expire.** 9Proxy runs periodic percentage discounts (an 8% New Year promotion on regular IP and GB packages, a 9% follow-up coupon on repeat GB orders), but these are date-bound and shouldn't be treated as permanently live. What does appear in the company's published affiliate terms is a 5% discount for referred users — 👉 [the invite link applies it at sign-up](https://bit.ly/9-Proxy).

## How to test without burning money

1. Buy small. Either the 5 GB pack or the 100-IP tier. Both are cheap enough to treat as a trial.
2. Run your actual targets, not a demo endpoint. Success rate on google.com tells you nothing about success rate on the site that keeps blocking you.
3. Measure cost per successful response, not cost per GB. A cheaper provider that fails twice as often is more expensive.
4. Use the Today List deliberately. On recurring jobs, note how many of yesterday's IPs return — that number is your effective discount.
5. Stress the sticky sessions. If you need a session to hold for hours, verify it does before scaling.
6. Check how a dead IP gets replaced. Deliberately let connections drop and see how the replacement flow behaves in practice.

Regarding free access: 9Proxy's own forum posts describe a limited trial for new users that depends on availability, and the allocation has changed over time. Rather than trusting a blog post about it, ask support directly when you sign up.

## Quick answers

**Is 9Proxy a subscription?** No. It's balance-based — you buy IP or traffic packages and draw them down. Unused IPs don't expire before activation, and GB packs hold for 180 days.

**Per-IP or per-GB?** Per-IP when bandwidth is heavy or unpredictable and you need stable sessions. Per-GB when you need wide rotation and each request is small.

**Does it work with anti-detect browsers?** Yes, via HTTP/HTTPS and SOCKS5, which is what tools like Multilogin, Dolphin Anty and AdsPower expect. Reviewers and users mention this pairing specifically.

**How fast is it?** A directory listing puts average response time near 1.3 seconds with a 97% success rate — usable for batch work, not for latency-sensitive real-time jobs.

**Can a team share one account?** Yes, through share codes and sub-accounts.

## The short version

When you're comparing proxy providers, ignore the pool-size arms race and price your own workload against three models. If your bandwidth is heavy or unpredictable, the per-IP model with unlimited traffic is the one that protects your budget — and at $0.084 per IP on the 1,500-IP tier, 9Proxy is priced below most of the field. If your work is rotation-heavy and light on data, start on the 55 GB pack, use the 180-day window properly, and lean on the Today List to stretch it.

The rest — 20M+ IPs, 90+ countries, SOCKS5, a replacement policy with teeth — is table stakes in this category. 👉 [Run your own targets through the network](https://bit.ly/9-Proxy) before you commit to a volume tier, and let the numbers on your invoice decide.
