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