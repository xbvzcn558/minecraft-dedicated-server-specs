# minecraft dedicated server hosting: bare-metal specs, real prices, and how much RAM your player count actually needs

People who search for dedicated server hosting for Minecraft usually fall into one of three camps. Either a shared Minecraft plan has started choking on your player count, you're building a public network that keeps attracting DDoS attacks, or you're done paying per gigabyte and want a whole machine to yourself. All three are valid reasons. All three have different price tags attached.

This guide walks through what "dedicated" actually changes for a Minecraft world, how to size RAM and CPU for your player count, and the full current dedicated lineup from Sharktech — a bare-metal provider that explicitly lists Minecraft among the games it hosts and puts always-on DDoS protection on every server. You'll also see where a dedicated box is genuinely worth it, and where a much cheaper option does the same job.

## What "dedicated" actually buys you for a Minecraft server

A managed Minecraft host rents you a slice of a big machine: a fixed RAM allocation, a friendly panel with one-click Paper installs and modpack loaders, and someone else handling the OS. It's the right call for most small servers, and it costs roughly $1–2.50 per GB of RAM across the budget end of the market.

A dedicated server is the whole physical box. No neighbors competing for CPU during peak hours, no oversold cores, direct hardware access, and you pick the operating system. The catch is everything after that is on you: the Java install, the server jar, the backups, the firewall, the monitoring. Nobody clicks "install Forge" for you.

A VPS sits in between — reserved resources on shared hardware, full root access, usually much cheaper than bare metal. We'll come back to that, because for a lot of Minecraft projects it's the sweet spot.

Home hosting deserves a quick mention since it comes up in every community thread. It works, people genuinely do it, and if you have a spare machine and decent upload it's nearly free. What breaks it is scale: residential connections fold under even small floods, and public servers get attacked. One of Sharktech's own game-hosting customers describes routine 3–8 Gbit attacks absorbed without the servers skipping a beat — that's the level of traffic that ends a home-hosted project in an evening.

Worth knowing: Minecraft's actual bandwidth appetite is small. A survival server with dozens of players uses a trickle. A 10 Gbps port and 300 TB of monthly transfer aren't there for player traffic — they're headroom for attack absorption and for whatever else you decide to run next to the game.

## How much server Minecraft actually needs

RAM gets all the attention in Minecraft hosting ads, and the sizing rules of thumb hold up across guides and community threads:

| Server type | Typical players | RAM that holds up |
| --- | --- | --- |
| Vanilla survival | 2–10 | 2–4 GB |
| Plugins, light modding | 10–25 | 4–6 GB |
| Medium modpacks | 25–50 | 8–16 GB |
| Heavy packs (ATM-class), public networks | 50+ | 16 GB and up |

A commonly cited rule: 4 GB covers most servers, including modpacks with up to 35–40 mods, for roughly 25 players. Beyond that, every mod, every plugin, and every concurrent player adds pressure.

The spec that matters more than hosts advertise is single-core clock speed. Minecraft's main server loop is largely single-threaded — player actions, world ticking, and entity behavior pile onto one core. A community admin running heavy modpacks put it plainly: the smoothest experiences come from hosts with high single-core clocks, not just lots of RAM. Core count starts paying off when you run many servers at once — a proxy, multiple game worlds, a database, a website — but one big survival server wants speed, not width.

That distinction drives every recommendation below.

## Where Sharktech fits into this

Sharktech has been in the infrastructure business since 2003 and built its reputation specifically on DDoS-protected hosting — protection isn't an upsell here, it's the founding product. For Minecraft that matters more than it might seem, because public servers are among the most attacked things on the internet.

The specifics that matter for a Minecraft deployment:

- **Always-on DDoS protection** on every server, 60 Gbps / 48 Mpps of basic mitigation included, with a 100 Gbps option at order time
- **Five data centers**: Los Angeles, Las Vegas, Denver, Chicago, and Amsterdam — pick whichever is closest to your players
- **99.99% uptime guarantee** on dedicated servers, with a hardware management panel for power control, remote console, and bandwidth graphs
- **24/7 support** and free setup on every configuration
- **Their own network** (AS46844), peered at major internet exchanges, which also helps their filtering respond closer to the source of attacks

The honest caveat: Sharktech is an infrastructure provider, not a Minecraft specialist. There's no one-click modpack installer, no Multicraft panel bundled in. You get serious hardware on a protected network, and you bring your own stack. For some readers that's a dealbreaker; for others it's exactly the point.

## The full dedicated lineup: every current build and price

These are all eight configurations currently listed on the bare-metal pricing page, with the exact specs and monthly prices shown at order time. Every build includes free setup, a 10 Gbps port, 300 TB/month of transfer, five usable IPv4 addresses (/29), and the included 60 Gbps DDoS protection. RAM is upgradeable to 1 TB on most builds, and ports scale to 40 or 100 Gbps.

| Build | CPU (as listed) | RAM | Storage | Price | Order |
| --- | --- | --- | --- | --- | --- |
| Dual Xeon E5-2695v4, 6× 2.5" bays | 36 × 2.1 GHz | 64 GB DDR4 | 2 TB NVMe M.2 + 6 open bays | **$259/mo** | [ Order this build](https://portal.sharktech.net/aff.php?aff=1611&pid=741) |
| Dual Xeon E5-2695v4, 6× 3.5" bays | 36 × 2.1 GHz | 64 GB DDR4 | 2 TB NVMe M.2 + 6 open bays | **$269/mo** | [ Talk to sales](https://bit.ly/SharKTech) |
| Dual Xeon Gold 6248, 3× 3.5" bays | 40 × 2.5 GHz | 128 GB DDR4 | 2 TB NVMe M.2 + 3 open bays | **$299/mo** | [ Order this build](https://portal.sharktech.net/aff.php?aff=1611&pid=660) |
| Dual Xeon Gold 6248, 6× 2.5" bays | 40 × 2.5 GHz | 128 GB DDR4 | 2 TB NVMe M.2 + 6 open bays | **$309/mo** | [ Order this build](https://portal.sharktech.net/aff.php?aff=1611&pid=636) |
| Dual Xeon Gold 6246, 3× 3.5" bays | 24 × 3.3 GHz | 128 GB DDR4 | 2 TB NVMe M.2 + 3 open bays | **$309/mo** | [ Order this build](https://portal.sharktech.net/aff.php?aff=1611&pid=814) |
| Dual Xeon Gold 6248, U.2 NVMe | 40 × 2.5 GHz | 128 GB DDR4 | 2 TB NVMe M.2 + 6 U.2 bays | **$329/mo** | [ Order this build](https://portal.sharktech.net/aff.php?aff=1611&pid=766) |
| AMD EPYC 7702P | 64 × 2 GHz | 128 GB DDR4 | 2 TB NVMe M.2 + 10 U.2 bays | **$499/mo** | [ Order this build](https://portal.sharktech.net/aff.php?aff=1611&pid=729) |
| Dual AMD EPYC 7702 | 128 × 2 GHz | 128 GB DDR4 | 2 TB NVMe M.2 + 10 U.2 bays | **$699/mo** | [ Talk to sales](https://bit.ly/SharKTech) |

Longer billing cycles knock the price down. On the $259 build, for example, quarterly billing comes to $738.15, semi-annual to $1,398.60, and annual to $2,641.80 — roughly 5%, 10%, and 15% off respectively. The same pattern applies across the lineup.

If none of these match what you had in mind, [👉 browse the full lineup and custom options](https://bit.ly/SharKTech) — the provider builds custom configurations on request, including GPU additions.

## Which build makes sense for which kind of server

Applying the single-thread logic from earlier, the picks sort themselves cleanly.

**One big survival or modded server:** the Dual Xeon Gold 6246 build at $309/mo. Its 3.3 GHz clocks are the fastest on the menu, which is what your tick rate actually cares about, and 128 GB of RAM means you'll never think about memory again. [👉 Configure the 6246 build here](https://portal.sharktech.net/aff.php?aff=1611&pid=814).

**A network — proxy, multiple worlds, database, website:** the Dual Xeon Gold 6248 with six drive bays at $309/mo, or the U.2 NVMe variant at $329/mo if you want faster storage for databases. Forty threads across two CPUs handle many parallel services comfortably, and you can virtualize the box to keep each piece isolated.

**Serious parallel workloads:** the EPYC builds. The single 7702P at $499/mo gives you 64 cores to slice into virtual machines — a sensible shape if you're hosting servers for several communities or running a hosting operation of your own.

**Tightest budget with dedicated hardware:** the Dual Xeon E5-2695v4 at $259/mo. Sixty-four GB of RAM is generous for the price, but be clear-eyed about the 2.1 GHz base clock — for a single vanilla server that's the weak spot. It shines more as a many-light-servers box than a one-big-world machine.

## Not ready for bare metal? The Smart VPS middle ground

If $259/mo made you wince, there's a middle path that keeps the protected network and drops the price dramatically. Sharktech's Smart VPS runs on triple-redundant Proxmox clusters with 40G interconnects, a 99.999% platform uptime target, and no VM downtime when hardware fails. You get a pool of reserved resources, and you can carve it into as many virtual machines as the pool allows — one big Minecraft server, or a dozen small ones spread across different cities.

| Tier | Xeon Gold cores | RAM | Monthly | Annual (per month) |
| --- | --- | --- | --- | --- |
| XS | 2 | 4 GB | $7.95 | $3.98 |
| S | 4 | 8 GB | $13.95 | $6.98 |
| M | 8 | 16 GB | $25.95 | $12.98 |
| L and up | 16 → beyond | 32 GB → beyond | scales with tier | 50% off monthly |

Annual billing cuts any tier in half — the XS works out to under $4/mo. The order form tops out with configurations reaching 128 cores and 256 GB, NVMe storage scaling to 2 TB, and transfer up to 300 TB. [👉 Check the Smart VPS tiers here](https://portal.sharktech.net/aff.php?aff=1611&pid=794).

Do the per-gigabyte math and the middle tiers land right in budget-host territory: the M tier works out to about $1.62/GB with root access, no player-slot limits, and 60 Gbps of DDoS protection included. The trade is that you're still on shared hardware, so a noisy neighbor can touch you in ways bare metal never will.

## What dedicated hosting costs next to managed Minecraft plans

Here's the comparison most listicles skip. A budget managed host charges roughly $1–2.50 per GB of RAM. At 128 GB — the standard allocation on most of Sharktech's dedicated builds — that pricing would run $128 to $320 per month, and you'd get a slice of a machine with a panel.

The $309 Gold 6246 build works out to about $2.42/GB, inside that same range, except the entire physical server is yours: 24 threads, 2 TB of NVMe, a 10 Gbps port, 300 TB of transfer, five IP addresses, and hardware-level access. Per gigabyte, dedicated hosting stops being expensive once your RAM needs get large. It's the small allocations where managed plans win outright.

So the honest decision rule:

- Under ~8 GB of RAM, a managed Minecraft host or the XS/S VPS tiers are cheaper and easier. Don't overbuy.
- 8–32 GB with one or two servers: the M or L VPS tiers hit the value sweet spot.
- 32 GB+ , multiple services, a public network, or a community that attracts attacks: bare metal earns its price.

## Fine print worth knowing before you order

A few things from the research that affect real money:

**No refunds, no trial.** All payments are nonrefundable, including setup and monthly charges. Billing disputes need raising within 30 days of the invoice, and favorable resolutions come back as account credit. Know what you're ordering before you order it.

**Delivery isn't instant.** Bare metal is provisioned in hours to a few days, not minutes — the provider states outright that sub-24-hour delivery can't be guaranteed, particularly for customized hardware. Plan your launch date accordingly.

**It's unmanaged by default.** You administer the machine. cPanel and DirectAdmin are available at extra cost, but those are web-hosting panels — for Minecraft you'd typically run your own stack, and community-standard options like Pterodactyl work fine on a box you fully control.

**Reputation is split by source, which is worth seeing plainly.** Trustpilot shows 3.5/5 across a small sample of 13 reviews that skew toward the extremes. HostAdvice's expert review scores the service 9.3/10 overall, praises transparent pricing and the management dashboard, and measured a support reply in under 40 minutes at 1 AM on a technical networking question. Small review volume cuts both ways — read both before committing.

**Watch for stale coupons.** A promotional pricing page with codes like v5LACHI and New2637v2 still floats around search results, but its own terms date the promotion to mid-2020. The genuinely current savings are the billing-cycle discounts — 5/10/15% on dedicated, 50% on annual VPS billing — which are visible on the order forms themselves.

## From bare metal to players online: the setup path

Once the machine is provisioned, getting a server live is a familiar sequence for anyone who's run one before:

1. **Pick your location at order time** — whichever data center is closest to most of your players. Latency is the difference between crisp and mushy block placement.
2. **Choose the OS.** Linux distributions like Ubuntu, Debian, and AlmaLinux are included; Windows Server carries extra cost and licensing.
3. **Install the JDK** matching your target Minecraft version once you have SSH access.
4. **Drop in your server jar** — Paper for performance-focused survival, Fabric or Forge for modded — and run it under a service manager or tmux so it survives your SSH session disconnecting.
5. **Open the default Java Edition port (25565)** in your firewall, or whatever custom port you choose.
6. **Point an A record** at one of your five IP addresses and hand players a clean hostname instead of numbers.
7. **Set up offsite backups immediately.** World files are irreplaceable in a way hardware isn't.
8. **Running several servers?** Consider a panel like Pterodactyl on the box to manage them from one interface — with full hardware access, nothing stops you.

Deployment time, support tickets, and the management panel all live in the same customer portal, so day-two operations are centralized even though the server itself is self-managed.

## Quick answers

**Is a dedicated server overkill for a friends-only survival world?**
Almost always, yes. Ten friends on vanilla need 2–4 GB and a good single core — the $7.95 VPS tier covers that with room to grow. Save the bare-metal budget for when you actually feel the ceiling.

**Can one dedicated box run multiple Minecraft servers?**
Comfortably. With 128 GB of RAM and 24–128 threads on most builds, you can run a proxy, several game worlds, a database, and a community site side by side — virtualized or as plain processes. That's the scenario where dedicated hardware stops looking expensive.

**Do I really need DDoS protection for a Minecraft server?**
If the server is public in any way, treat it as mandatory. Minecraft servers are frequent targets, and community threads are full of admins discovering this the hard way. Every Sharktech server ships with 60 Gbps of always-on mitigation, which removes the question entirely.

**What's the actual cheapest sensible entry point?**
The Smart VPS XS at $7.95/mo — or $3.98/mo equivalent on annual billing — with 4 GB of RAM, 2 Xeon Gold cores, NVMe storage, and the same protected network as the big iron. [👉 Start with the XS tier here](https://portal.sharktech.net/aff.php?aff=1611&pid=794) and scale up only when the players force you to.

The right size server is the smallest one your community has outgrown. Everything above that threshold is just future-proofing you're paying for today — and everything below it is lag you'll be apologizing for tomorrow.
