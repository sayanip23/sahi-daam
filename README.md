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
Deck formula:

**Floor = (Product cost + Packaging + Shipping + GST on shipping + Ad spend + Target profit) ÷ parcels that stay sold**

- Out of 100 parcels dispatched, the ones that stay sold = delivered − customer returns (e.g. 100 → 82 → 65).
- Product cost counts every piece sold plus returned pieces that can't be resold.
- Shipping = forward shipping on delivered parcels + return shipping on customer returns (RTO carries no shipping charge).
- GST on shipping = 18% of that shipping.
- Ad spend per order = cost per click ÷ share of clicks that buy (₹2 ÷ 5% = ₹40). Not available to non-GST sellers.
- Target profit is set by the seller per order (₹20 in the demo).
- GST-registered sellers add their product GST on top.

**Break-even** is the same formula with target profit = ₹0: below it, the seller loses money.

Worked example, ₹185 cotton kurti: (12,996 + 1,500 + 7,965 + 1,434 + 0 + 1,300) ÷ 65 = **₹388 floor**; break-even ₹368.

## Run locally
No build step. Open `index.html` in a browser.
