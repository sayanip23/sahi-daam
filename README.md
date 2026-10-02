# Sahi Daam (सही दाम)

**Team Fab3** (Shashank Katiyar, Uday Meena, Sayani Patra): Meesho DICE Challenge 3.0, Prototype Phase.

**Live demo:** https://sayanip23.github.io/sahi-daam/

Sahi Daam is a pricing co-pilot for new-to-online sellers, built into the Supplier Panel they already use.
It answers "Will I make money at this price?", not just "What are others charging?":
a **profit floor**, a **demand-weighted price band**, and an **autopilot** that watches six signals and sends one WhatsApp nudge a week.

> Concept prototype. Not an official Meesho product. All seller, market and rate data is simulated. Teal = what Sahi Daam adds to the Supplier Panel.

## Demo sellers (from our research)
- **Rekha**, 47, Kanpur: kurti seller, not GST registered (no ads, sells within her state). Priced from her shop (₹350), then went below it (₹320) and loses ₹8 an order without knowing it.
- **Imran**, 32, Kanpur: electronics seller, GST registered, runs Meesho Ads. Ads eat his margin and rivals undercut him weekly.

## 2-minute demo path
1. **Choose a demo seller**, then open **Catalog Upload**. It follows Meesho's current form (category → Product, Size and Inventory → Product Details → quality check), including the Wrong/Defective Returns Price. The teal box shows the lowest safe price under Meesho Price, the no-loss price, money kept per order, how many returns the price can handle, and a suggested starting price. A second hint shows the lowest safe price for the Wrong/Defective Returns Price.
2. **Price Recommendation**: pick a catalog on the left. Overview shows Meesho's “Increase in Orders / Sales” next to Sahi Daam's “Change in your profit”; the teal “Lowest safe price” column warns before you Accept; View Comparison shows competitors.
3. **Quality Dashboard**: Meesho’s account health cards, rating trend and return-reasons pie (tap a reason). Teal: what returns cost per order, “if you fix this reason” numbers, a returns slider with a profit chart, and profit per 1,000 viewers.
4. **Sahi Daam Autopilot**: set your rules (money to keep per order, highest price, ask first or do it for me), then tap the green WhatsApp buttons through each seller's journey (EN / हिं).

## How the numbers are computed (as in the deck, slide 6)
**Floor = (Product cost + Packaging + Shipping + GST on shipping + Ad spend + Target profit) ÷ parcels that stay sold**

Inputs (deck slides 4 and 6): catalogue shipping charge ₹56, paid by the customer; the seller pays **18% GST on it** for every delivered parcel. Return shipping ₹160 per customer return. **No charge on RTO** (Meesho's stated policy). About **1 in 10** returns can't be resold. Packing ₹5 per parcel. Ads = cost per click ÷ conversion (₹2 ÷ 5% = ₹40). TCS and TDS are refunded, so they are left out.

- **Lowest safe price (floor)**, the five-line napkin: (stock that stays sold + packing and GST on shipping paid on every parcel + failure cost: return shipping and damaged returns + ads + target profit) ÷ parcels that stay sold. For GST-registered sellers (Imran, 18%), product GST is added on top.
- **No-loss price, real profit per order and max return rate** (the three numbers she never sees) follow the slide's P&L: sales and product cost on every delivered order, minus damaged returns, packing, GST on shipping, return shipping, ads and product GST. Max return rate = the rate at which returns and RTO (each per 100 parcels) wipe out the profit.

**Check: the engine reproduces slide 6 exactly** (₹100 kurti listed at ₹140, 15 RTO + 15 returns): napkin ₹7,000 + ₹1,357 + ₹2,550 = ₹10,907 ÷ 70 = **floor ₹155**; P&L ₹11,900 − ₹8,500 − ₹857 − ₹500 − ₹2,400 − ₹150 − ₹567 = **−₹1,073 per 100 orders (−₹10.73 per order)**; **break-even ₹153**; **max return rate 9.4%**.

**Demo sellers:** Rekha's ₹275 kurti listed at ₹320 loses ₹8 per order (no-loss ₹330, lowest safe price ₹364). Imran's ₹385 earbuds listed at ₹549 lose ₹11 per order (no-loss ₹563, lowest safe price ₹606).

## Mentor feedback built in (1 Oct)
- **Who bears shipping:** Catalog Upload shows what the customer pays at checkout (price + forward shipping) and what the seller pays (return charges and 18% GST on the delivery charge).
- **Launching at a thin margin:** Catalog Upload lists competitors to check, and ways to lower the floor through cost before raising the price.
- **Quality and profit:** Quality Dashboard shows how fixing the top return reason changes floor, orders and profit per 1,000 views.

## Run locally
No build step. Open `index.html` in a browser.
