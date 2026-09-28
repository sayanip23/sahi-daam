# Sahi Daam (सही दाम)

**Team Fab3** (Shashank Katiyar, Uday Meena, Sayani Patra): Meesho DICE Challenge 3.0, Prototype Phase.

Sahi Daam is a pricing co-pilot for new-to-online sellers. It adds three things to the Supplier Panel:
a **profit floor** ("Below ₹388, you lose money"), a **price band** showing where orders actually land,
and an **autopilot** that tests prices inside the seller's range and sends one WhatsApp nudge a week.

> Concept prototype. Not an official Meesho product. All seller, market and rate data is simulated.

## Live demo
- `index.html`: Supplier Panel–style prototype (teal = what Sahi Daam adds)
- `story.html`: story view of the three engines and Sunita's first 100 days

## 2-minute demo path
1. **Catalog Upload**: Meesho Price ₹249 → floor ₹388, loses ₹132 per kept order → "Use ₹399".
2. **Price Recommendation**: 2 of 4 recommended prices are below the floor; open the ✎ slider on the palazzo set.
3. **Quality Dashboard**: returns add ₹33 to the floor; a size chart beats a price cut.
4. **Sahi Daam Autopilot**: tap the WhatsApp buttons through Day 0 → festive week; switch EN / हिं.

## How the floor is computed
Per 100 dispatched parcels: kept = delivered − customer returns.
floor = (packing + forward shipping on delivered + return shipping + goods consumed incl. unsellable returns + ads) ÷ kept × (1 + GST).
RTO parcels are not charged shipping, only the goods lost. With the deck's Ramesh inputs this gives ₹345.

## Run locally
No build step. Open `index.html` in a browser.
