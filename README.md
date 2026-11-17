# RackNerd vs Contabo: which is cheaper at 1, 2 and 4 GB, when does Contabo win, and what does renewal actually cost? (full plan table + 3-year totals)

At 1 GB, 2 GB and 4 GB of RAM, RackNerd is the cheaper of the two: $1.83, $3.00 and $5.00 per month on annual prepay, and those annual plans are listed as renewing at the same price. At 8 GB the answer flips. Contabo's entry Cloud VPS 4 gives you 8 GB of RAM and 4 vCPU for $5.28/mo, against $10.00/mo for RackNerd's 8 GB plan.

The $5.28 has two conditions attached. It requires a 2-year commitment, and it renews at $6.60/mo, 25% above the headline. RackNerd's batch prices stay flat on renewal. What follows is priced out: all five RackNerd plans, the crossover at every RAM size, median cost per GB and per vCPU, a three-year total for both entry points, third-party performance grades, and the things RackNerd doesn't sell at all.

> **Most readers should take the 4 GB KVM VPS at $60/year.** 3 vCPU, 4 GB RAM, 60 GB SSD, 7 TB of monthly traffic, $5.00/mo equivalent, renewal at $60. That covers a blog, a small app, a Docker host with a few containers, or a WireGuard endpoint with room to spare.
> 👉 [Get the 4 GB KVM VPS at $60/year](https://bit.ly/RacKnerd)

## RackNerd's five plans, priced end to end

RackNerd runs KVM, is based in Orange County, California, and has been selling VPS since 2019. The five plans below are the current lineup, priced as annual prepay with the monthly equivalent shown alongside.

| Plan | vCPU | RAM | SSD | Traffic | Price |
| --- | --- | --- | --- | --- | --- |
| [ 1 GB KVM VPS](https://bit.ly/RacKnerd) | 1 | 1 GB | SSD | 3 TB | $1.83/mo |
| [ 2 GB KVM VPS](https://bit.ly/RacKnerd) | 2 | 2 GB | 35 GB | 5 TB | $3.00/mo ($36/yr) |
| [ 4 GB KVM VPS](https://bit.ly/RacKnerd) | 3 | 4 GB | 60 GB | 7 TB | $5.00/mo ($60/yr) |
| [ 6 GB KVM VPS](https://bit.ly/RacKnerd) | 6 | 6 GB | 100 GB | 12 TB | $7.50/mo ($90/yr) |
| [ 8 GB KVM VPS](https://bit.ly/RacKnerd) | 7 | 8 GB | 150 GB | 20 TB | $10.00/mo ($120/yr) |

Prices checked November 13, 2026. RackNerd rotates promotional batches and restocks them in waves, so the disk size and traffic cap on the $1.83 plan change from one batch to the next.

Storage is labelled SSD across the standard line. RackNerd also sells an AMD Ryzen NVMe line with faster disk and stronger single-thread CPU, at the cost of less disk space on the small plans. Neither line goes above 8 GB of RAM or 7 vCPU.

👉 [See all five RackNerd plans and current prices](https://bit.ly/RacKnerd)

## The price crossover sits at 8 GB

Contabo's cheapest plan already includes 8 GB of RAM. That single fact drives most of this comparison: at every size below 8 GB you are comparing RackNerd's small plans against a Contabo plan that is bigger than what you asked for.

| RAM you need | Contabo | RackNerd | Cheaper |
| --- | --- | --- | --- |
| 1 GB+ | $5.28/mo (Cloud VPS 4: 8 GB, 4 vCPU) | $1.83/mo (1 GB, 1 vCPU) | RackNerd, 65% less |
| 2 GB+ | $5.28/mo | $3.00/mo (2 GB, 2 vCPU) | RackNerd |
| 4 GB+ | $5.28/mo | $5.00/mo (4 GB, 3 vCPU) | RackNerd, 5% less |
| 8 GB+ | $5.28/mo | $10.00/mo (8 GB, 7 vCPU) | Contabo, 47% less |
| 16 GB+ | $13.44/mo (Cloud VPS 8: 24 GB, 8 vCPU) | No plan this size | Contabo |
| 32 GB+ | $24.00/mo (Cloud VPS 12: 48 GB, 12 vCPU) | No plan this size | Contabo |

Contabo's lineup reaches 96 GB RAM and 24 vCPU across 17 plans. RackNerd stops at 8 GB and 7 vCPU across 5. If your workload is measured in tens of gigabytes of RAM, the decision is already made and the rest of this page is about confirming the price.

## Per-GB and per-vCPU: two different shapes

Median cost per GB of RAM lands close on both sides: $1.19 at Contabo, $1.25 at RackNerd. The gap that matters is per core. RackNerd's median is $1.50 per vCPU; Contabo's is $4.20.

RackNerd packs cores into small machines (7 vCPU on an 8 GB plan), which suits web servers, build agents, small databases and anything that responds to parallelism more than to memory. Contabo goes the other way, stacking RAM on each core (96 GB over 24 vCPU), which suits Nextcloud, Plex, game servers, JVM applications and self-hosted stacks that sit idle on CPU and eat memory.

The practical version: match the shape, not just the price. A 2 GB box with 2 cores handles a WordPress site fine. It will not handle a media library with thumbnail generation.

## Renewal, terms, and the real three-year bill

Contabo's $5.28 is a first-term price on a 24-month contract: $126.72 up front, then $6.60/mo on renewal. Year three costs $79.20, which puts the three-year total at $205.92.

RackNerd's 4 GB plan is $60/year and renews at $60. Three years costs $180, and you are never more than 12 months from walking away.

That comparison cuts both ways. If 4 GB is enough for you, RackNerd is about $26 cheaper over three years than Contabo's entry plan and doesn't lock you in for 24 months. If you actually need 8 GB, the same math runs the other direction: RackNerd's 8 GB plan is $120/year, or $360 over three years, against Contabo's $205.92. Paying $10/mo for memory Contabo gives away at $5.28 is the expensive mistake in this comparison.

👉 [Lock in the $60/year 4 GB plan with annual billing](https://bit.ly/RacKnerd)

## What the benchmarks actually say

vpsbenchmarks runs standardized trials and grades each plan from A to F. Both providers' budget tiers land in the middle of that scale, and neither is flattered by the results.

| Plan (tested) | Web | Raw CPU | Stability | Disk IO | Network |
| --- | --- | --- | --- | --- | --- |
| Contabo Cloud VPS Plus 4, 4 cores / 8 GB, Jul 2026 | B | B | C | D | D |
| RackNerd Ryzen 2 vCores / 4 GB, Dec 2025 | B | D | D | C | E |
| Contabo Cloud VDS S, 6 cores / 24 GB, Oct 2026 | C | C | B | C | E |
| Contabo Cloud VPS 18, 18 cores / 96 GB, Sep 2026 | E | B | F | E | D |

Read the network column first. RackNerd's tested plan scored E; Contabo's small plan scored D. Disk IO came in at C and D respectively. These are cheap boxes with shared everything, and the grades say so. Contabo's 96 GB flagship scored an F on stability, which is worth knowing before you consolidate six services onto one large instance.

RackNerd's sample is a single plan tested in December 2025, so treat its row as a data point rather than a verdict on the whole lineup. Provisioning time was measured at roughly 60 seconds for Contabo across three attempts and 110 seconds for RackNerd in one attempt, which is too thin a sample to argue about.

## Who should not buy RackNerd

Four situations where Contabo is the better fit, stated plainly:

**You need more than 8 GB of RAM.** RackNerd has no answer above 8 GB / 7 vCPU. Contabo goes to 96 GB and 24 vCPU.

**You need servers in Asia-Pacific.** Contabo lists locations in Singapore, Japan, Australia and India on top of the US, UK and Germany. RackNerd's footprint is the United States, the Netherlands and France.

**You want the provider to handle backups or DDoS filtering.** Contabo includes always-on network-level DDoS protection and sells a daily automatic backup add-on, plus up to three snapshots. RackNerd offers no backup product and no DDoS protection. If you go with RackNerd, budget an hour to wire restic or borg into cheap object storage; that is your backup plan.

**You need NVMe printed on the spec sheet.** RackNerd's standard line is SSD (the Ryzen line is NVMe). Contabo lists NVMe across its Cloud VPS plans.

## Five details that bite after checkout

**Two separate logins.** RackNerd splits billing from server management. Invoices, payment methods and tickets live in the client area; reboots, OS reinstalls, the HTML5 VNC console, one-click apps, the network firewall and root password resets live in ctrl, the control panel attached to the VPS. New users lose time hunting for the reboot button in the wrong place.

**PTR records.** Set the reverse DNS entry before you point a mail server at the IP. Receiving providers check it, and a missing PTR is the usual reason self-hosted mail gets rejected. It's handled from the control panel, or by ticket if the option isn't exposed on your plan.

**The refund window is short.** RackNerd's terms list a 3-day money-back window on eligible first orders. Confirm the current wording on the billing page before paying, and don't count on it applying to renewals or to add-on services.

**Free IPv6 is location-limited.** Up to 100 IPv6 addresses are available on request in the Los Angeles and France locations. Other locations are still being brought online for IPv6, so don't assume your chosen datacenter supports it.

**Upgrades exist but plan for them.** ctrl includes an upgrade action, which is cheaper than guessing high at signup. If you're between the 2 GB at $36/year and the 4 GB at $60/year, the $24 gap buys double the RAM and an extra core.

👉 [Compare the 2 GB and 4 GB plans side by side](https://bit.ly/RacKnerd)

## FAQ

**Is a $1.83/month VPS actually usable?**
For a DNS resolver, a monitoring agent, a VPN endpoint, a static site or a small bot, yes. The benchmark grades put RackNerd's web performance at B, so ordinary web serving is fine. What the cheap tiers don't have is network headroom or disk throughput for sustained heavy workloads, and that applies to both providers at this price.

**Can I pay RackNerd monthly instead of annually?**
The $1.83, $3.00 and $5.00 figures are annual-prepay equivalents. RackNerd's standard KVM line is also sold month to month at higher monthly rates, which makes sense if you want to test a location for a few weeks before committing to a year.

**Can I move to a bigger plan later?**
Yes, the control panel includes an upgrade option. Take a snapshot of your own data first if you're resizing storage, since disk changes are the step where people lose files.

**Which RackNerd location should I pick for visitors in Asia?**
Los Angeles. DC-02 and DC-03 sit at the main transpacific landing point on the US west coast, which is why they're the default recommendation for Asia-Pacific traffic. For European visitors, Amsterdam and the France location are the closer picks.

## How to decide in one minute

Under 4 GB of RAM: RackNerd's 4 GB plan at $60/year, or the 2 GB at $36/year if it's a single small service. Renewal stays at $60, the term is 12 months, and the yearly commitment is the only real risk.

8 GB or more, or you need Singapore, Japan, Australia or India, or you want provider-run backups and DDoS protection: Contabo's Cloud VPS 4 at $5.28/mo. Go in knowing you're signing for 24 months at $126.72 and renewing at $6.60/mo.

Before you pay, check three things on the order page: the renewal price shown on the invoice, the datacenter you selected, and the refund terms for your specific plan. Promotional batches sell out and restock, so the plan you saw yesterday may not be the plan on sale today.

👉 [Start with the 4 GB KVM VPS at $60/year](https://bit.ly/RacKnerd)
