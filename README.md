# best scraping api: How to Compare Real Credit Costs, Trials and Refund Rules Before You Subscribe

Searching for the best scraping api usually means one thing: you need pages from sites that don't want to be scraped, and you don't want to babysit proxies. The honest answer up front — there's no single winner. Bright Data leads independent success-rate benchmarks, self-hosted tools like Crawl4AI cost nothing if you can tolerate the ops work, and for most developers who want one API endpoint that handles IP rotation, JavaScript rendering and CAPTCHA solving without infrastructure headaches, **ScraperAPI** is a solid middle-ground pick: a free tier, a 7-day trial, and per-request credit costs you can calculate before spending anything. This guide walks through its current plans, what a "credit" actually buys you on different sites, and the refund and billing rules most comparison articles leave out.

> **Quick take:** start with the free tier — 1,000 credits per month, plus a 7-day trial with 5,000 credits, no credit card required. Paid plans start at **$49/mo for 100,000 credits** (Hobby), and annual billing saves 10%. If you scrape standard pages, that's roughly 100,000 requests; heavy targets like Google or LinkedIn burn credits much faster, so read the credit table below before picking a tier. 👉 [Claim the 7-day free trial — 5,000 credits, no credit card required](https://www.scraperapi.com/?fp_ref=coupons)

## What "best" actually depends on

A scraping API has one job: send a URL, return usable HTML or JSON. The difference between providers is how reliably they do it on hostile sites and how much it costs you per page. In 2026, Cloudflare, DataDome, PerimeterX and Kasada sit in front of a huge share of the commercial web, and a plain request with a cheap datacenter proxy rarely survives. That's why every serious scraping API bundles proxy rotation, JS rendering and anti-bot handling into the request.

Three things should drive your choice:

1. **Success rate on your actual targets.** Scrape.do runs an open-source benchmark that tested 16 providers against the 7 hardest domains in its repository (Amazon, Indeed, GitHub, Zillow, Capterra, Google, X), counting a request as successful only when the returned HTML contained validated content — a 200 with a challenge page counts as a failure. Keep in mind the benchmark is published by a competitor, but its methodology and code are public. Bright Data topped it with a 98.87% average success rate; the full top-tier results are worth a look before you commit.
2. **What a credit really costs.** Almost every provider bills in "credits" or "requests," but the exchange rate between a credit and an actual page varies wildly by target. Most comparison articles quote plan prices and stop there. I'll do the math below.
3. **What happens when things go wrong.** Failed requests, credits burning out mid-month, refund policy — these show up in FAQs and docs, not on the pricing page.

Here's how the benchmark's leaders and the services covered in this article stacked up on the hardest targets (average success rate / average response time / typical cost per 1,000 requests):

| Provider | Success rate | Avg response | Cost per 1K |
| --- | --- | --- | --- |
| Bright Data | 98.87% | 12.7s | $1.50 |
| Scrape.do | 98.61% | 5.5s | $0.60 |
| Apify | 97.14% | 14.2s | $5.48 |
| ScrapingBee | 96.62% | 13.7s | $1.77 |
| ScraperAPI | 72.57% | 5.6s | $4.25 |

That last row deserves a straight conversation. On these seven specific heavily-protected domains, ScraperAPI's average success rate trails the leaders by a wide margin. Two caveats before you read it as a verdict: the benchmark covers the hardest 16% of the web by design, and it's published by Scrape.do, which sells a competing service. But it does tell you something useful — if your targets are exactly these kinds of fortress sites (Google SERPs, LinkedIn, heavily protected e-commerce), you should verify on your own URLs before committing to any annual plan, and every provider here has a free way to do exactly that.

## ScraperAPI's full plan lineup

ScraperAPI currently offers a free plan plus seven paid tiers. All paid plans include the same core features: JavaScript rendering, premium residential and mobile IPs, JSON auto-parsing, rotating proxies, custom headers, CAPTCHA and anti-bot detection, custom sessions, desktop and mobile user agents, automatic retries, unlimited bandwidth, and a 99.9% uptime guarantee. What separates tiers is credit volume, concurrency, and geotargeting scope.

| Plan | Monthly | Annual (10% off) | Credits/mo | Concurrency | Geotargeting | Get it |
| --- | --- | --- | --- | --- | --- | --- |
| Free | $0 | $0 | 1,000 | 5 | — | [Sign up free](https://www.scraperapi.com/?fp_ref=coupons) |
| Hobby | $49 | $44.10/mo | 100,000 | 20 | US & EU only | [Start Hobby](https://www.scraperapi.com/?fp_ref=coupons) |
| Startup | $149 | $134.10/mo | 1,000,000 | 50 | US & EU only | [Start Startup](https://www.scraperapi.com/?fp_ref=coupons) |
| Business | $299 | $269.10/mo | 3,000,000 | 100 | All countries | [Start Business](https://www.scraperapi.com/?fp_ref=coupons) |
| Scaling | $475 | $427.50/mo | 5,000,000 | 200 | All countries | [Start Scaling](https://www.scraperapi.com/?fp_ref=coupons) |
| Professional | $975 | $877.50/mo | 10,500,000 | 300 | All countries | [Start Professional](https://www.scraperapi.com/?fp_ref=coupons) |
| Advanced | $1,975 | $1,777.50/mo | 21,500,000 | 500 | All countries | [Start Advanced](https://www.scraperapi.com/?fp_ref=coupons) |
| Enterprise | Custom | Custom | 22,000,000+ | 500+ | All countries | [Contact sales](https://www.scraperapi.com/?fp_ref=coupons) |

The Scaling plan is flagged as "Most popular" on the pricing page. One detail worth noticing: Hobby and Startup are geotargeting-limited to US and EU regions. If you need to scrape with IPs from specific countries — say, a German-localized Amazon page — you need Business or above, which is a bigger jump than the credit count alone suggests.

## What a credit actually buys you

This is the part most "best scraping api" roundups skip, and it changes your plan choice more than the sticker price does.

On ScraperAPI, a standard page costs 1 credit. But targets with dedicated pricing structures cost more:

| Target | Cost per request |
| --- | --- |
| Standard page | 1 credit |
| Amazon | 5 credits |
| Cloudflare / DataDome / PerimeterX protected sites | +10 credits when bypassed |
| Google and Bing (including subdomains) | 25 credits |
| LinkedIn | 30 credits |

Do the math on Hobby's 100,000 credits and the picture gets concrete: about 100,000 standard pages, but only 4,000 Google searches, roughly 3,300 LinkedIn requests, or 20,000 Amazon product pages in a month. An independent review estimates the same 100,000 credits covers around 3,000 heavily protected URLs per month once you stack JS rendering and premium proxies on top. None of this makes the plan bad — it just means the question "how many pages do I scrape?" needs a second question attached: "from which sites?"

Two tools keep this under control. The dashboard has a Domain Cost Estimator that shows the exact credit cost for any URL before you burn anything, and you can set a `max_cost` parameter per request so a single expensive scrape can't blow through your balance. Between those two, you can calculate your monthly bill before the first request fires — which matters more here than on competitors, because target-specific credit costs swing widely.

## When credits run out mid-month

ScraperAPI gives you three documented ways to handle a drained balance, and the difference matters for whether your pipeline dies on the 20th of the month:

- **Do nothing**, and scraping pauses until the next billing cycle.
- **Auto-upgrade** (opt-in, available on Hobby through Professional): your account moves up to the next tier automatically when credits run out, usually at a better per-credit price.
- **Pay-As-You-Go** (Scaling, Professional, Advanced, Enterprise): buy extra credits at a fixed, predictable rate without changing plans, capped by a monthly spending limit you set yourself.

Concurrency works differently. Exceed your thread limit and the API returns a 429 — the request is rejected, not queued, and you're not charged for it. Worth knowing if your scraper fires 300 parallel requests on a 20-thread Hobby plan.

## How ScraperAPI compares on price

To place the plans in context, here's the verified competition — information only, no links, since your decision should be based on fit rather than whoever's discount code is loudest:

- **ScrapingBee** starts cheaper: five monthly plans from $19/mo (75,000 credits, 25 concurrent) up to $599/mo (8,000,000 credits, 400 concurrent), with 1,000 free credits and no credit card to sign up. Its default request costs 5 credits because JavaScript rendering is on by default, so effective per-page pricing on that entry plan is close to $1.27 per 1,000 rendered pages. It also only charges for successful requests (200, 404, or 410 responses). On the benchmark above it scored 96.62% with a $1.77 per-1K average — a strong all-round showing, and its $19 entry tier undercuts ScraperAPI's $49 Hobby if your volume is small.
- **Bright Data** is the benchmark leader (98.87% average, 400M+ residential IPs) with pay-only-for-success pricing from $1.50 per 1,000 successful requests and no monthly commitment. For maximum success rates on the nastiest targets, it's the reference point.
- **Scrape.do** ran the benchmark and ranks second at 98.61% with the fastest average response among top scorers (5.5s). Its own comparison pages make aggressive claims about ScraperAPI's cost and speed — treat those as single-party marketing — but the underlying benchmark numbers are independently reproducible from its public repo.
- **Apify** operates a marketplace of 3,000+ pre-built scraper "Actors" with $5 of free monthly usage. Better if you'd rather run someone's finished scraper than write API calls.
- **Crawl4AI** is free and self-hosted if you're willing to run your own infrastructure and accept a lower success rate on protected sites.

One more data point on entry pricing: a third-party review notes ScraperAPI's $49 entry plan is higher than some pay-as-you-go rivals. That's a fair criticism if your monthly volume is a few thousand requests — though in that case the free tier plus trial might cover you entirely, and paid plans would be premature anyway.

## Trial, discount and refund rules — the fine print that saves money

ScraperAPI's terms are unusually clean, and they're documented in the official billing FAQ:

- **Free trial:** 7 days with 5,000 credits on signup, no credit card required. After the trial, the free plan continues at 1,000 credits per month with up to 5 concurrent connections.
- **Refund:** a 7-day no-questions-asked refund policy. Unhappy for any reason, contact support and they process the refund.
- **Cancellation:** anytime from the dashboard, with no cancellation charge.
- **Annual discount:** 10% off across all paid tiers — Hobby drops from $49 to $44.10/mo, Scaling from $475 to $427.50/mo.
- **Promo code:** independent review roundups list `START10` for 10% off the first month of any paid plan. The same sources warn that the 28–65% discount codes floating around coupon aggregators mostly don't exist — that tracks with how these affiliate pages usually work.

These rules lower the real risk of trying it close to zero: trial for a week at scale, refund within 7 days if it doesn't fit, cancel whenever. 👉 [Start the 7-day trial with 5,000 free credits and test it on your own targets](https://www.scraperapi.com/?fp_ref=coupons)

## What users report

Feedback aggregated from Capterra and GetApp reviews is mostly positive on three points: quick integration, effective IP rotation against blocks, and responsive support. Reviews describe the service as handling the tedious infrastructure work — proxy rotation, CAPTCHAs, rendering — so developers can focus on the data. Long-term users report staying satisfied.

The recurring complaints are just as useful: Facebook and Instagram are hard for every tool in this category, not just this one; premium targets consume credits faster than newcomers expect; and the way JS rendering multiplies credit consumption takes time to internalize. That last point is exactly why the credit table above matters more than the plan prices.

## FAQ

**How many credits does one request cost on ScraperAPI?**
A standard page is 1 credit. Amazon costs 5, Google and Bing cost 25, LinkedIn costs 30, and sites behind Cloudflare, DataDome or PerimeterX add 10 credits per bypassed request. Check any URL's exact cost with the Domain Cost Estimator in your dashboard before scraping.

**What happens if I run out of credits before renewal?**
By default scraping pauses until your next cycle. You can enable Auto-Upgrade (Hobby through Professional) to jump to the next tier automatically, or — on Scaling and above — use Pay-As-You-Go with a monthly spending cap to keep going at a fixed rate.

**Does ScraperAPI offer refunds?**
Yes. The official policy is a 7-day no-questions-asked refund; contact support to process it. Cancellation is free and available anytime from the dashboard.

**Is there a free trial without a credit card?**
Yes — 7 days with 5,000 credits on signup, no card required. Afterwards you keep a free plan with 1,000 credits per month, limited to 5 concurrent connections.

**Is ScraperAPI good enough for heavily protected sites?**
It handles anti-bot bypassing on all paid plans, and independent reviews confirm it works on protected targets. On the hardest benchmark domains (Google, LinkedIn, X) its measured success rate trails leaders like Bright Data and ScrapingBee, so if those exact targets dominate your workload, run the free trial against your own URL list before committing to a year.

## So which plan should you pick?

Match the tier to your target mix, not just your page count:

- **Testing or small side projects** → the free tier plus the 7-day trial. Don't pay until you've confirmed your targets scrape at an acceptable rate, because that's what determines your credit burn.
- **Standard pages in volume, US/EU targets only** → Hobby at $49/mo ($44.10 on annual). 100,000 credits covers 100k simple requests.
- **Google SERP, LinkedIn, or heavily protected e-commerce targets** → budget at least 25–30 credits per request, which usually pushes you to Startup ($149/mo) or Business ($299/mo, where full country geotargeting unlocks). If those sites consistently fail during your trial, the benchmark leaders in this category are the better match — test before you commit either way.
- **Production pipelines with spiky traffic** → Scaling ($475/mo). It's the "Most popular" tier for a reason: 5M credits, 200 threads, and Pay-As-You-Go means a traffic spike doesn't kill the job.
- **Absolute maximum success rate on hostile sites, big budget** → Bright Data's benchmark numbers lead that category, and enterprise buyers should evaluate both before committing.

Before you subscribe, run your two or three highest-volume target URLs through the Domain Cost Estimator and multiply by your monthly volume — that one calculation predicts your bill better than any comparison chart. When you're ready, 👉 [compare all ScraperAPI plans and start your free trial](https://www.scraperapi.com/?fp_ref=coupons).
