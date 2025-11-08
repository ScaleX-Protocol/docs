# **ScaleX \- Unified CLOB DEX-Lending Protocol**

# **A. Problem Statement**

1\.  **Capital Inefficiency**

A trader deposits $100,000 on an order book CEX/DEX. Even when not placing orders, those funds can ONLY be used for trading, they earn zero yield. To earn any returns, traders must manually move assets to separate funding/lending accounts, creating friction and lost opportunities. Meanwhile, billions in liquidity sit idle in order books waiting to be executed, these active limit orders could be earning yield but currently generate zero returns. In DeFi today, millions of traders watch both their trading capital and active orders sit completely unproductive.

### **2\. Risk of Borrowing Liquidations**

When traders borrow against their collateral, lending protocols force liquidation during market drops. Users watch helplessly as their collateral gets sold at crash prices, unable to protect themselves by strategically converting to stable assets beforehand.

### **4\. Loan Repayment at Expensive Cost**

When traders borrow ETH and immediately sell to USDT, they must manually repay the ETH loan later at market rates. They miss opportunities to automatically repay when ETH prices drop, losing the chance to reduce borrowing costs during market dips.

### **3\. No Borrowing Power Against Trading Portfolio**

Even when traders deposit funds on CEX/DEX platforms, they can’t borrow against those balances. Their trading portfolio has zero borrowing power, forcing them to deposit additional collateral separately just to access leverage for other strategies.

### **5\. Fragmented Experience**

Traders must juggle multiple DeFi protocols, one for trading, another for lending/borrowing. This creates complexity, high gas costs, and poor capital management across disconnected systems.

**6\. Inefficient Order Execution**

When traders place limit orders, they must already hold the exact asset to be sold or bought. This forces idle capital to remain locked even before an order executes. Users cannot place orders that exceed their available asset balance, even if their portfolio value can support it. As a result, trading capital stays unproductive until orders are filled.

**The result:** Traders lose significant returns to inefficiency, slippage, untapped borrowing power, and missed repayment opportunities across DeFi.

---

# **B. Existing Solution**

## **1\. Binance / Bybit \- Dual Investment**

**Mechanism:** A structured product that combines yield generation with options-like behavior, allowing users to earn returns or accumulate/sell assets at preferred prices.

In essence, it functions as both a **yield product** and a **conditional limit order**, users can deposit assets to earn fixed yield *while simultaneously setting a desired buy or sell price*. If the market reaches the target (strike) price at settlement, the system automatically executes the conversion at that level.

**Process:**

1. User deposits an asset and selects a target (strike) price.  
2. If the target is reached, the asset converts to stablecoins at a premium.  
3. If not, the user earns a fixed yield for the duration.

**Purpose:** Allows users to earn in either direction — ideal for range-bound markets or passive strategies.

**Disadvantage:**

* Includes a fixed settlement price and expiry date, limiting flexibility.  
* Cannot adjust or exit positions mid-term without penalty.  
* Yield depends heavily on market volatility.

## **2\. Fidelity \- Margin Loans**

**Mechanism:** Traditional brokerage margin loan where users borrow against portfolio assets to increase leverage.

**Process:**

1. Users pledge eligible securities as collateral.  
2. Fidelity lends cash based on a percentage of asset value.  
3. Interest is charged daily until repayment.

**Purpose:**  Provides liquidity for investors without selling existing holdings.

**Disadvantage:**

While these tools streamline certain aspects of trading and borrowing, they still leave users exposed to inefficiencies like forced borrowing, idle capital, or rigid repayment logic.

* Zero Yield on Idle Capital and Active Positions  
* Crypto Assets Not Supported  
* Non-Retail Accessibility Issues  
* Fixed interest rates that adjust slowly with market conditions.  
* No on-chain transparency or automation.  
* Limited repayment flexibility; requires manual management

---

## **3\. OKX \- Auto-Borrow & Auto-Repay**

**Mechanism:** Automatically borrows assets when an order exceeds available balance of the required asset, and repays when the position closes or profit is realized.

**Process:**

1. Users place an order larger than their available funds.  
2. The system borrows the shortfall from the margin pool instantly.  
3. When the position closes, the borrowed amount is automatically repaid using the user’s balance or profit.

**Purpose:** Simplifies margin trading and reduces idle debt by automating borrowing and repayment.

**Disadvantage:**

* Interest accrues immediately upon borrowing, even if orders aren’t filled.  
* Users have no control over repayment logic, leading to potential unwanted size reduction.  
* Requires centralized custody; funds must remain in the platform’s margin system.

## **4\. Glow Finance \- Margin & Yield Engine**

**Mechanism:**

An on-chain, non-custodial margin and yield protocol that lets users deposit assets to simultaneously **earn yield** and **utilize them as collateral for trading or restaking** within the same environment. It effectively combines lending, borrowing, and trading functions, allowing users to earn on idle capital while deploying leverage.

Borrowed assets are restricted to **internal protocol usage only** — users cannot withdraw or use them externally, ensuring all positions remain contained within Glow’s smart-contract system.

**Process:**

1. Users deposit eligible assets (e.g., SOL, USDC) into a margin account; the assets immediately start earning yield and serve as collateral.  
2. The protocol enables borrowing of other supported assets against the collateral, which can then be used for in-protocol actions such as trading, liquidity provision, or restaking (e.g., converting borrowed SOL into glowSOL to earn staking rewards).  
3. When the user’s position is closed or collateral is withdrawn, the borrowed amount must be repaid; the system automatically calculates health factors and may trigger liquidation if thresholds are breached.

**Purpose:**

Maximizes **capital efficiency** by merging yield generation and leverage into a unified on-chain framework, ideal for users who want to **earn while trading** without moving funds between protocols.

**Disadvantages:**

* **Internal-only usage:** Borrowed funds cannot be transferred or used outside the Glow ecosystem.  
* **Liquidation risk:** Margin positions are subject to collateral ratio thresholds.

---

# **C. Our Solution**

**World’s first integrated CLOB \+ Lending Protocol**

Unlocking capital efficiency through a revolutionary flywheel:

**“Trade your assets while they earn yield automatically”**

## **Why Order Book DEX is the Perfect Match for Lending Protocol**

**This creates a self-reinforcing flywheel effect** where idle trading capital generates yield, higher yields attract more liquidity, better liquidity improves trading conditions, and increased trading volume drives more borrowing demand \- creating an unstoppable cycle of growth.

![][image1]

**Phase 1 : Yield Opportunity Attracts Deposits**

Traders are drawn to the platform by its yield-bearing mechanism, depositing assets into the pool even before orders are filled

**Phase 2 : Low Utilization Attracts Borrowers**

When utilization is low, borrowing is attractive, drawing in traders who want leverage and liquidity

**Phase 3 : Borrowing Raises Utilization**

Borrow activity increases utilization of the lending pool, activating higher interest accrual

**Phase 4 : Interest Pays Lenders**

Borrowers pay interest, which is distributed as yield to lenders whose capital powers the system

**Phase 5 : Active Repay and Reborrow Cycle Enhances Depth**

Borrowers continuously execute repay and reborrow actions to maintain or increase positions, adding dynamic liquidity depth to the orderbook and stabilizing market flow.

**Order Book DEX Users Gain:**

* **Yield on Idle Capital**: All trading balances AND active orders automatically earn interest while waiting for execution

* **Borrowing Power**: Trading portfolio gains borrowing capacity for leverage strategies

* **Capital Efficiency**: Every dollar works 24/7 \- trading \+ earning simultaneously

### **Lending Protocol Users Gain:**

* **Trading Capabilities**: Use lent assets to place limit orders and actively manage positions

* **Strategic Liquidation Protection**: Place protective orders to prevent liquidation losses

* **Smart Loan Repayment**: Automatically repay loans at lower costs using limit orders

* **Enhanced Returns**: Combine passive yield with active trading opportunities

---

# **D. Technical Innovation**

### **Key Breakthroughs:**

* **Red-Black Tree Order Book**: O(log n) price discovery

* **Synthetic Token System**: 1:1 pegged yield-bearing tokens

* **Auto-Lending Protocol**: Native interest rate curves

* **Unified Interface**: Trade \+ lend in one platform

### **Revolutionary Integration Features:**

#### ***1\. Ultimate Capital Efficiency***

Real Case: Active Trader Portfolio

Traditional Order Book Experience:  
\- $50K in limit orders waiting for fills  
\- $50K sitting idle earning zero yield  
\- Trading gains only when orders execute  
\- Capital completely unproductive while waiting

Our Solution:  
\- Same $50K in limit orders for trading  
\- $50K automatically lent out earning yield  
\- Earn yield while waiting for trades to execute  
\- Capital works 24/7, never sits idle

**Result**: Every dollar earns yield while waiting for trading opportunities\*\*

#### ***2\. Order Book ADL and Liquidation Protection***

**Traditional liquidations:** Forced sells at market prices → Reducing profitable position, Devastating slippage losses

**Our solution:**

* Pre-position limit orders at strategic liquidation prices

* **Zero-slippage liquidations** when positions approach liquidation

* Users keep their assets, **avoid forced selling during crashes**

* **Protect against cascading liquidations** in volatile markets

* **Eliminates insurance fund and ADL** mechanism entirely

#### ***3\. Smart Loan Repayment System***

**Traditional repayment:** Buy tokens at market rates → Overpay for debt

**Our solution:**

* **Place** **passive limit orders** to buy back debt tokens

* **Automatically repay loans** when orders fill at optimal prices

* **Strategic debt repayment** during market dips

* **No manual intervention** required

Real Case: Active Trader Portfolio

Traditional Order Book Experience:  
\- $50K in limit orders waiting for fills  
\- $50K sitting idle earning zero yield  
\- Trading gains only when orders execute  
\- Capital completely unproductive while waiting

Our Solution:  
\- Same $50K in limit orders for trading  
\- $50K automatically lent out earning yield  
\- Earn yield while waiting for trades to execute  
\- Capital works 24/7, never sits idle

**Result**: Every dollar earns yield while waiting for trading opportunities

#### ***4\. Dynamic Risk Management***

* **Real-time position monitoring** via order book data

* **Predictive liquidation warnings** using price level analysis

* **Automated collateral adjustments** based on market depth

* **Smart order routing** to minimize liquidation risk

* **Driven by real trade** rather than pooled liquidity

---

# **E. Business Model**

### **Revenue Streams:**

1. **Trading Fees**: 0.1% on CLOB transactions

2. **Lending Interest**: 2-8% spread on borrowed funds

### **Market Opportunity:**

* **First-mover advantage** in order book \+ lending integration

* **Massive untapped market** for integrated trading \+ lending

* **Growing demand** for capital-efficient DeFi solutions

* **Clear path to significant market share** in trader-focused DeFi

---

# **F. Target Users**

### **Primary: Sophisticated Traders**

* Need **leverage** for strategies

* Want **price improvement** over AMMs

* Value **passive yield** on idle capital

### **Secondary: Yield Seekers**

* Want **higher APYs** than standalone lending

* Prefer **self-custody** over CEX lending

* Like **composability** with trading

### **Tertiary: DeFi Borrowers & Leveraged Traders**

* Need **competitive borrowing rates** for leverage

* Want **automated loan repayment** at optimal prices

* Value **liquidation protection** through strategic orders

* Seek **single collateral source** for both trading and borrowing

* Appreciate “**real market price”** rather than “impulsive move/manipulative” price

### **Quaternary: Passive Investors & HODLers**

* Want **yield on long-term holdings** without selling

* Need **borrowing power** against existing assets

* Value **capital protection** during market volatility

* Prefer **automated risk management** for their positions

### **Quinary: Institutional DeFi**

* Need **capital efficiency** for treasury management

* Want **single platform** for multiple strategies

* Value **transparent risk management**

---

# **F. Competitive Advantage**

### **vs Standalone Order Book DEX (dYdX, Vertex)**

* ✅ **Built-in yield generation** on idle trading capital

* ✅ **Zero-slippage liquidations** via order book protection

* ✅ **Smart loan repayment** automation

* ✅ **4x higher capital efficiency**

* ✅ **Dual revenue streams** vs single trading fees

### **vs Standalone Lending Protocols (Aave, Compound)**

* ✅ **Built-in user base** from trading activity

* ✅ **Natural capital sources** from idle balances

* ✅ **40% lower liquidation costs** (order book protection)

* ✅ **15-25% reduced borrowing costs** (smart repayment)

* ✅ **4x higher user returns** (capital efficiency)

### **vs CEX Platforms (Binance, FTX)**

* ✅ **Self-custody** \- users control assets

* ✅ **Transparent rates** \- on-chain calculations

* ✅ **No counterparty risk** \- smart contracts

* ✅ **Composable** \- DeFi ecosystem integration

* ✅ **Programmatic liquidation protection** (automated order placement)

* ✅ **Lower borrowing costs** (strategic order execution)

* ✅ **Organic trade** \- on order book & execution

* ✅ **Fixed position & size** \- ADL free

### **vs Standalone Lending (Aave, Compound)**

* ✅ **Built-in user base** from trading activity

* ✅ **Natural capital sources** from idle balances

* ✅ **Dual revenue streams** vs single source

* ✅ **Better retention** \- unified platform

* ✅ **40% lower liquidation costs** (order book protection)

* ✅ **15-25% reduced borrowing costs** (smart repayment)

* ✅ **4x higher user returns** (capital efficiency)

---

# **G. Vision**

**Building the future of capital-efficient DeFi:**

“Every dollar works harder \- trading while earning yield, protecting against losses, and optimizing costs”

[image1]: <data:image/png;base64,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0zHATWCSALfbbrv1Nttss5XG0PrNb37T+/zzz/OXLxy2AXe+rb766r0DDjig9+c//zl/Seewzj/72c/yh1cy6wB33nnn9Z555pn84bmywG4OWhVmub9Jo3gX9HQMcBOYJMCBGrcdd9yx//dnn33WW3fddYvCktqnpiJonHDCCTM9ybP+hx56aO+ggw7qHXPMMb1vfOMb/ZD7wx/+MH/5QKeddlrvpz/9af7w3Lzyyiu97bffvvfxxx/nT/UuuOCCYgrsD2UnSrYF6/HGG28Uf5999tn91/E93HLLLenLl41577777vnDxfdd9WcNYoBrDgOcyrz00ku9ffbZZy4tRwa46RjgJjBpgHv99deLWrjU008/3dtiiy1611133ZLHm+TNN98sCvSddtopf6oyxx9/fG+VVVZZ8tj//u//Fp/JZ4/b1zBCX13uvPPO4vPLmoIvv/zyovn8gw8+KP4eFOCeeOKJ4vEDDzyw+Puwww7rv45/11hjjfTly8Y8y4aNOOqooyr/rEEMcM1hgFOZBx98sLfOOusU5dOsGeCmY4CbACedSfrulAU40ETGybLJaOo97rjjZtbcy/pz0ii7uotAc9ttt+VPreQvf/lLUWP13HPPLXn8k08+6d14443F85N67bXXis8ep+Dadttte+utt17+cIF58P2zH9BsSY1jBM6Y4jNuuummoiYSaYCjho/auXfeeac/32lRS0iNXr4M6cm7qs8axQK7OcoCHMd97AdnnXVW78orryz2nXfffXfJ6wZh38/nWSeOKS62xnXIIYf0j41VV121qEmfVVk4Kc5D89i2lAVrrbVW77HHHsufqpzlwXQMcBOYJsCtueaaRbMUfbw4iUehkBYGTz31VL/mienkk09eMg9CANXZ8fzGG29c1KBwcFGwxOMPPfRQf37xGOGCeQSa67iqKsNzxx57bGntzO233178y2uYb9QqpbhRgxDy0Ucf5U+tJPp5RQ0WE+u50UYbFf+/5JJLlmyjl19+uZg3J5FBoYxl+s53vrNkfnfccUf+sn4zNtPvf//7lR6nwN5000173/72t5N3leP1nBzKsKw0VdI0Gd8F/46y9957F99tGWrIYtljIkSm2P433HBDsb2effbZ/uPsK6xbbJtxDNuX2CcjZMd2H7drgAX2fEQ4Y5iQQWUXrQr5fsn3k+5ja6+9dtFy8Pjj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>