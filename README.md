# Sahi Daam (सही दाम)

**Team Fab3** (Shashank Katiyar, Uday Meena, Sayani Patra): Meesho DICE Challenge 3.0, Prototype Phase.

**Live demo:** https://sayanip23.github.io/sahi-daam/

Sahi Daam is a pricing co-pilot for new-to-online sellers, built into the Supplier Panel they already use.
It answers "Will I make money at this price?", not just "What are others charging?":
a **profit floor**, a **demand-weighted price band**, and an **autopilot** that watches six signals and sends one WhatsApp nudge a week.

> Concept prototype. Not an official Meesho product. All seller, market and rate data is simulated. Teal = what Sahi Daam adds to the Supplier Panel.

## Demo sellers (from our research)
- **Rekha**, 47, Kanpur: kurti seller, not GST registered (no ads, sells within her state). Priced from her shop, then went below it.
- **Imran**, 32, Kanpur: electronics seller, GST registered, runs Meesho Ads. Ads eat his margin and rivals undercut him weekly.

## 2-minute demo path
1. **Choose a demo seller**, then open **Catalog Upload**. The floor appears under Meesho Price, with the three numbers a seller never sees: break-even price, real profit per kept order, and the highest return rate the price survives. The decision rule picks a launch price.
2. **Price Recommendation**: Meesho's recommended price is checked against each catalog's floor.
3. **Quality Dashboard**: return reasons turned into rupees on the floor.
4. **Sahi Daam Autopilot**: tap the WhatsApp buttons through each seller's journey; switch EN / हिं.

## How the floor is computed
Per 100 dispatched parcels: kept = delivered − customer returns.
floor = (packing + forward shipping on delivered + return shipping + goods consumed incl. unsellable returns + ads) ÷ kept × (1 + GST).
Ad cost per order = cost per click ÷ share of clicks that buy. RTO parcels are not charged shipping, only the goods lost.
With the deck's ₹185 cotton kurti inputs this gives ₹345.

## Run locally
No build step. Open `index.html` in a browser.
