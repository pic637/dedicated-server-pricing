# Rent a Dedicated Server: What the Monthly Price Really Buys, Why "From €4.74" and "From $35.75" Aren't the Same Number, and How Fast the Machine Actually Arrives

A usable dedicated server starts at roughly **$36 to $43 a month** for an older Xeon with 8 to 16 GB of RAM, and around **$0.09 an hour** if you bill hourly. A preconfigured machine is usually online in about 12 minutes, a custom build in about a day, and the operating system install itself takes 20 to 30 minutes. Remote console access (IPMI) and basic DDoS filtering now sit in the base price at most hosts rather than showing up as add-ons.

The word "from" is where the trouble starts. Depending on which host you read, the advertised entry price assumes a 12-month lock-in, a 36-month lock-in, an hourly meter running 730 hours a month, or a lowest-spec box that is currently sold out. Below is what each pricing model actually means, what a real configuration costs at each term, how much prepaying a year saves once you do the arithmetic, and which costs tend to appear after you have already committed.

> **The short version.** If you are leaving a VPS because you need the whole machine (game servers, CI runners, scraping, a client environment you have to hand over), budget **$60 to $120 a month** for a current single-socket box with 64 GB of RAM and SSD storage, or **$115 to $185 a month** if you need 20+ cores and 128 to 256 GB. Stay monthly until the workload has proven itself, then take a 6- or 12-month term, which typically removes 6% to 15%. 👉 [See Spin Servers' current server list and prices](https://bit.ly/Spinservers)

## What a monthly dedicated server costs right now

The table below is one US host's published list (Dedicated.com), reproduced because it is the most complete set of real configuration-plus-price pairs available to compare against. Its cheapest listed configuration is **$35.75/month**, and every configuration includes IPMI, a /29 IPv4 block (5 usable addresses), DDoS filtering on every port, and no setup fee on any term.

| Configuration | Monthly | 3 months | 6 months | 12 months |
| --- | --- | --- | --- | --- |
| Xeon Gold 6140, 256 GB DDR4, 2×2 TB SSD, 10 Gbps, 100 TB | $183.99 | $535.41 (−3%) | $1,037.70 (−6%) | $1,942.93 (−12%) — sold out |
| Dual Xeon E5-2640 v4, 128 GB DDR4, 2×2 TB SSD | $134.99 | $392.82 (−3%) | $749.19 (−8%) | $1,376.90 (−15%) |
| Dual Xeon E5-2630 v4, 64 GB DDR4, 2×1 TB SSD | $114.99 | $334.62 (−3%) | $648.54 (−6%) | $1,214.29 (−12%) — sold out |
| Xeon E5-1650 v3/v4, 64 GB DDR4, 1×1 TB SSD | $63.99 | $186.21 (−3%) | $360.90 (−6%) | $675.73 (−12%) — sold out |
| Xeon E3-1271 v3, 32 GB DDR3, 2×256 GB SSD | $55.99 | $162.93 (−3%) | $315.78 (−6%) | $591.25 (−12%) — sold out |
| Xeon E3-1230 v2, 8 GB DDR3, 2×2 TB HDD | $42.99 | $125.10 (−3%) | $242.46 (−6%) | $453.97 (−12%) |

Two things jump out. The gap between the cheapest box ($42.99) and a 36-core, 256 GB box ($183.99) is about four times the price for roughly eight times the compute, so the mid-range is usually the worst value per core unless you specifically need a single-socket machine. And several of the configurations listed are marked sold out, including the flagship. A price list is not an inventory list.

## Why the "from" figures can't be compared directly

| Provider | Headline "from" price | What that number actually assumes |
| --- | --- | --- |
| Scaleway Dedibox | €4.74/month | 12-month commitment on the Start line; Pro (€29.74) and Core (€110.49) require **36 months** |
| Cherry Servers | ~$0.091/hour | Hourly on-demand rate; fixed terms advertised up to 50% off |
| HOSTKEY | ~€25/month | Lowest listed build; the company itself puts the average at ~€100/month and high-performance builds at €600+ |
| Dedicated.com | $35.75/month | Monthly term on the cheapest listed configuration, no setup fee |

Put them on one basis and the picture changes. €4.74 a month is €56.88 for the year, but you have signed for the year and the Pro and Core tiers want three years. The $0.091 hourly rate sounds almost free until you multiply it by 730 hours: **about $66 a month** if the server runs continuously, which is more expensive than a $42.99 monthly box with better hardware. Hourly billing is a tool for short-lived work, not a discount.

The other trap is comparing currency without noticing it. A €25 build and a $35.75 build are not far apart in real terms, but the European one may sit in a market where rents run higher for reasons covered below.

## How much does prepaying actually save?

Take the Gold 6140. Twelve monthly payments come to $2,207.88; the 12-month prepay is $1,942.93, so you save **$264.95**, or 12%. The 6-month prepay saves $66.24 and the 3-month prepay saves $16.56, which is under 9% of a single month's fee and rarely worth the commitment on its own.

The discount is not a fixed schedule, either. The same host lists some configurations at −3%/−6%/−12% and others at −3%/−8%/−15% (the dual E5-2640 v4 is one of the 15% ones). You cannot assume the term discount you saw on one page applies to the box you want.

Then there is the stock problem. The configuration with the clearest prepay math on that list is sold out everywhere. Discounts attach to hardware that is in the rack and available, and the boxes with the deepest discounts are often the ones being retired.

One more consideration before you wire a year of rent: not every host publishes a refund window. Cherry Servers offers a 15-day money-back guarantee provided the terms of service have not been breached; for others, the refund policy has to be asked for. Get the answer in writing before prepaying anything longer than a quarter.

## Delivery time depends on stock, not on the host's marketing

Verified numbers from three providers:

- **Cherry Servers:** preconfigured servers average 12 minutes to deploy; custom builds take about 24 hours; a Windows Server install adds roughly 30 minutes.
- **Dedicated.com:** deployment begins immediately after payment, OS installation takes about 20 minutes, and credentials arrive by email automatically.
- **HOSTKEY:** turnkey configurations can be online a few minutes after payment clears.

Anything marked out of stock simply cannot be ordered, and some hosts let you leave an email for restock notification on a specific location. If you have a launch date, pick from in-stock configurations and accept a slightly worse spec sheet. If you need an unusual combination of CPU, RAM and disk, plan for a day or more, not 12 minutes.

## The same specs cost 10–15% more in Europe

HOSTKEY puts the European premium at **10% to 15% over comparable US rentals**, and attributes it to power costs, environmental regulation and tax. That is a useful number because it is one of the few quantified regional comparisons published by a host that sells in both markets.

The latency side matters more than the price side for most workloads. US locations in Texas and Virginia serve a global audience reasonably well but add delay for European visitors; a Frankfurt or Amsterdam box is the obvious pick for EU traffic. Verified footprints: Cherry Servers runs Lithuania, the Netherlands, Germany, Sweden, the US and Singapore; HOSTKEY runs the EU, the US and Turkey; Dedicated.com lists Atlanta, Chicago, Dallas, Los Angeles, Montreal, New York and Seattle.

Pick the continent first, then the city, then the price. Doing it in the other order is how people end up with a cheap box 150 ms away from their users.

## The costs that appear after the headline price

**Management.** HOSTKEY states plainly that all of its servers are unmanaged and that administration is a paid extra. The same is true at most budget hosts even when it isn't stated as clearly. If you cannot harden a Linux install, configure a firewall and recover a broken bootloader, price in either a management plan or your own time.

**Control panels.** cPanel and ISPmanager style panels are billed as options at HOSTKEY, not bundled. A $60 server can become a $90 server once a panel is added.

**Windows licensing.** Scaleway notes that choosing Linux avoids the Windows licence fee. If your application needs Windows Server, check whether the licence is included in the monthly price or added on top, because the difference can run to tens of dollars a month.

**Extra IPv4 addresses.** A /29 with 5 usable addresses is included at Dedicated.com. Need more, or need a second block for SSL or mail separation, and it becomes a line item.

**Traffic overage.** Allowances vary widely: 100 TB on the configurations above, 50 TB on some builds, 1–10 Gbps unmetered ports at HOSTKEY with outgoing limits set by the chosen traffic plan. Ask for the per-TB overage rate before you move a video or backup workload onto a metered box.

## Which configuration fits which job

- **A project that might not last the month.** Bill hourly (Cherry Servers from about $0.091/hour) or take a monthly term you can walk away from. Do not sign a year to save 12% on something you may abandon in six weeks.
- **One steady application, under 64 GB of RAM.** The $55 to $70 band covers web stacks, small databases, game servers and VPN endpoints. This is where a 12-month term makes sense once traffic is predictable.
- **Containers, multiple VMs, or a database over 100 GB.** 20+ cores and 128 to 256 GB, at $115 to $185 a month. Check that the storage is SSD or NVMe rather than HDD before comparing prices.
- **Storage-heavy work (backups, media archives).** High-capacity HDD builds, or a dedicated storage line such as Scaleway's Store range from €29.99/month.
- **GPU inference.** A different budget class entirely: Scaleway's GPU line starts at €1,274.99/month, and that figure assumes a 36-month commitment.

## Before you order, from any host including Spin Servers

The checklist that separates a good rental from an expensive lesson:

1. **Is it managed or unmanaged?** Ask explicitly. "Fully managed" and "24/7 support" are not the same thing; support usually covers hardware and network, not your application.
2. **What is the traffic allowance and the overage rate?**
3. **Is IPMI or KVM access included?** Without it, a failed boot means opening a ticket and waiting.
4. **Which billing terms get a discount, and does that discount apply to this specific configuration?**
5. **What is the refund or cancellation window?** Get it before prepaying.
6. **Is the configuration in stock at the location you want?** A sold-out flagship is not a plan.

Spin Servers publishes its own live configuration list, which is the only place where its current prices, locations and included features are authoritative. Inventory in this market turns over weekly, so check the current list against the benchmarks above rather than working from a spec sheet someone quoted last quarter. 👉 [Check Spin Servers' available configurations and pricing](https://bit.ly/Spinservers)

## FAQ

**Is hourly or monthly billing cheaper?**
Monthly, if the server runs continuously. At $0.091/hour a server costs about $66 a month on demand; a comparable monthly configuration is often under $50. Hourly wins only when the machine lives for days, not months.

**How fast will I get the server?**
Preconfigured stock in about 12 minutes at Cherry Servers, immediate deployment plus a 20-minute OS install at Dedicated.com, minutes after payment at HOSTKEY. Custom builds run to about 24 hours.

**Is DDoS protection included?**
Basic filtering is standard at the hosts checked: every port at Dedicated.com, all plans at Cherry Servers, and free basic protection in Europe at HOSTKEY. If you are a regular target, ask about scrubbing capacity and layer-7 coverage, which usually costs extra.

**Can I run Windows Server?**
Yes at Cherry Servers (2019/2022, installed in about 30 minutes), HOSTKEY (2012–2019, plus ESXi), and Scaleway lists Windows among its installable systems. Confirm whether the licence is included in the monthly price.

**Do I get remote console access?**
IPMI is included at Dedicated.com and HOSTKEY, with iDRAC and KVM options. Elsewhere, confirm it before ordering, because it changes how quickly you can recover from a bad kernel update at 2 a.m.

**What about refunds?**
Cherry Servers offers 15 days, conditional on the terms of service not being breached. Other hosts vary, and some publish nothing. Ask, and keep the reply.

## The decision, in one pass

Short-lived or experimental work goes hourly. Stable production with a known workload takes the 12-month term once you have confirmed the discount applies to your specific configuration and the box is in stock. Anything above 128 GB of RAM should be bought on measured need, not on the assumption that headroom is free. And whatever the price sheet says, add the management cost, the panel cost and the licence cost before you compare two hosts, because that is where a $60 server and an $85 server turn out to be the same price.

When you have your shortlist, put the same six questions to each host and compare the twelve-month totals rather than the monthly headline. 👉 [Start with Spin Servers' current lineup and terms](https://bit.ly/Spinservers)
