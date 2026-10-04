# Sahi Daam (सही दाम)

**Team Fab3** (Shashank Katiyar, Uday Meena, Sayani Patra): Meesho DICE Challenge 3.0, Prototype Phase.

**Live demo:** https://sayanip23.github.io/sahi-daam/

Sahi Daam is a pricing co-pilot for new-to-online sellers, built into the Supplier Panel they already use.
Meesho's Price Recommendation keeps a seller *competitive*. Sahi Daam also answers **"Will I make money at this price?"**:
a **lowest safe price** for every catalog, a warning before a seller accepts a price that loses money, and an **autopilot** that watches six signals and sends one WhatsApp tip a week.

> Concept prototype. Not an official Meesho product. All seller, market and rate data is simulated. Teal = what Sahi Daam adds to the Supplier Panel.

## Demo sellers (from our research)
- **Rekha**, 47, Kanpur: kurti seller, not GST registered (no ads, sells within her state). Her ₹100 cotton kurti is listed at ₹140, below its ₹155 lowest safe price, so she loses ₹15 an order without knowing it.
- **Imran**, 32, Kanpur: electronics seller, GST registered, runs Meesho Ads. His ₹375 earbuds are listed at ₹549, below their ₹571 lowest safe price, so he loses ₹22 an order, and rivals undercut him every week.

## 2-minute demo path
1. **Choose a demo seller**, then open **Catalog Upload**. It follows Meesho's current form (category → Product, Size and Inventory → Product Details → quality check), including the Wrong/Defective Returns Price. The teal box shows the lowest safe price, profit per order, similar listings, how many returns the price can handle, and a suggested starting price. Drag the slider to see where your price stands.
2. **Price Recommendation**: pick a catalog on the left. Overview shows Meesho's "Increase in Orders / Sales" next to Sahi Daam's "Change in your profit". The teal "Lowest safe price" column warns before you Accept. The ✎ button opens Meesho's Edit Price box with the safe price marked on the slider. View Comparison shows competitors.
3. **Quality Dashboard**: pick a catalog from the dropdown. Meesho's account health cards, rating trend and return reasons (tap a reason). Teal: **What returns cost you** in ₹ per order, what fixing the tapped reason is worth, and a returns slider with a chart.
4. **Sahi Daam Autopilot**: set your rules (highest price to try, ask first or do it for me), then tap the green WhatsApp buttons through each seller's journey (EN / हिं).

## How the numbers are computed (deck, slide 6)
**Lowest safe price = (product cost + packing + GST on shipping + return shipping and unsellable returns + ads) ÷ parcels that stay sold**

Inputs: catalogue shipping charge ₹56, paid by the customer; the seller pays **18% GST on it** for every delivered parcel. Return shipping ₹160 per customer return (GST included). **No charge on RTO** (Meesho's stated policy). About **1 in 10** returns can't be resold. Packing ₹5 per parcel. Ads = cost per click ÷ share of clicks that buy (₹2 ÷ 5% = ₹40). TCS and TDS are refunded, so they are left out. For GST-registered sellers (Imran, 18%), product GST is added on top.

**Check against slide 6** (₹100 kurti, 15 RTO + 15 returns per 100 parcels): ₹7,000 + ₹1,357 + ₹2,550 = ₹10,907 ÷ 70 parcels that stay sold = **lowest safe price ₹155**.

**Profit per order = listed price − lowest safe price.** Nothing else is added or taken away, so at ₹140 Rekha loses ₹15 per order. When a price is above similar listings, Sahi Daam warns that it can mean fewer orders.

**Max return rate** = the share of returns and RTO (each per 100 parcels) at which profit per order reaches ₹0. At ₹140 Rekha can afford about 10.7 of each; she has 15.

All of Rekha's kurtis use the same packing (₹5) and shipping (₹56 delivery, ₹160 return). Similar cotton kurtis sell at ₹149–₹199, and Sahi Daam suggests starting at ₹189.

## What else the prototype shows
- **Who pays shipping:** Catalog Upload shows what the customer pays at checkout (price + delivery charge) and what the seller pays (return charges and 18% GST on the delivery charge).
- **Cut costs before raising the price:** Catalog Upload lists competitors to check, and ways to lower the lowest safe price through cost.
- **Quality and profit:** Quality Dashboard shows how fixing the top return reason changes the lowest safe price and profit per order.

## Run locally
No build step. Open `index.html` in a browser.
