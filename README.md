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
1. **Choose a demo seller**, then open **Catalog Upload**. It follows Meesho's current form (category → Product, Size and Inventory → Product Details → quality check), including the Wrong/Defective Returns Price. The teal box shows the lowest safe price under Meesho Price, the no-loss price, money kept per order, how many returns the price can handle, and a suggested starting price. A second hint shows the lowest safe price for the Wrong/Defective Returns Price.
2. **Price Recommendation**: pick a catalog on the left. Overview shows Meesho's “Increase in Orders / Sales” next to Sahi Daam's “Change in your profit”; the teal “Lowest safe price” column warns before you Accept; View Comparison shows competitors.
3. **Quality Dashboard**: Meesho’s account health cards, rating trend and return-reasons pie (tap a reason). Teal: what returns cost per order, “if you fix this reason” numbers, a returns slider with a profit chart, and profit per 1,000 viewers.
4. **Sahi Daam Autopilot**: set your rules (money to keep per order, highest price, ask first or do it for me), then tap the green WhatsApp buttons through each seller's journey (EN / हिं).

## How the floor is computed
Deck formula:

**Floor = (Product cost + Packaging + Shipping + GST on shipping + Ad spend + Target profit) ÷ parcels that stay sold**

- Out of 100 parcels dispatched, the ones that stay sold = delivered − customer returns (e.g. 100 → 82 → 65).
- Product cost counts every piece sold plus customer returns that can't be resold. RTO parcels always come back to the seller (mentor).
- Shipping = return shipping on customer returns + forward and return shipping on RTO parcels (mentor: RTO is not free). Forward shipping on delivered orders is paid by the customer, so it is not in the floor (mentor).
- GST on shipping = 18% of that shipping. TDS and TCS are left out because they are refundable (mentor).
- Ad spend per order = cost per click ÷ share of clicks that buy (₹2 ÷ 5% = ₹40). Not available to non-GST sellers.
- Target profit is set by the seller per order (₹20 in the demo).
- GST-registered sellers add their product GST on top.

**Break-even** is the same formula with target profit = ₹0: below it, the seller loses money.

Worked example, ₹185 cotton kurti: (12,497 + 1,500 + 4,975 + 895 + 0 + 1,300) ÷ 65 = **₹326 floor**; break-even ₹306.

## Mentor feedback built in (1 Oct)
- **Who bears shipping:** Catalog Upload shows what the customer pays at checkout (price + forward shipping) and what the seller pays (returns and RTO).
- **Launching at a thin margin:** Catalog Upload lists competitors to check, and ways to lower the floor through cost before raising the price.
- **Quality and profit:** Quality Dashboard shows how fixing the top return reason changes floor, orders and profit per 1,000 views.

## Run locally
No build step. Open `index.html` in a browser.
