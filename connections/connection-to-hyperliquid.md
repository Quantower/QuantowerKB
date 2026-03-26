---
description: >-
  Master decentralized perpetuals trading by integrating the power of
  Hyperliquid L1 with the professional-grade analytics of Quantower.
---

# Connection to Hyperliquid

### Step 1: Generate Credentials on Hyperliquid

First, you need to authorize a "trading agent" that Quantower will use to sign transactions on your behalf.

1. Go to [app.hyperliquid.xyz](https://app.hyperliquid.xyz) and connect your primary wallet (MetaMask, Rabby, etc.).
2. Navigate to More (the three dots in the menu) → API.
3. Click Generate API Wallet.
4.  Crucial: The system will display a Private Key for this specific API Wallet.\
    &#xNAN;_&#x43;opy and save it immediately in a secure location._ It will not be shown again.

    <figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
5. Click Authorize API Wallet and sign the transaction in your primary wallet. This gives the API Wallet permission to execute trades.
6.  Copy your Main Account Address (your primary wallet address where your funds are located).<br>

    <figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

***

### Step 2: Configure the Connection in Quantower

1. Open Quantower and click on the Connections icon in the top panel).
2.  In the Connections Manager, find Hyperliquid in the list. (If it’s missing, ensure your Quantower is updated to the latest version).<br>

    <figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>
3. Fill in the following parameters:
   * Account Address: Paste your Main Wallet Address (the one holding the USDC).
   * API Secret / Private Key: Paste the Private Key of the API Wallet you generated in Step 1.

***

### Step 3: Connect and Verify

1. Click the Connect button next to Hyperliquid.
2. It takes a few minutes to connect while the data from all symbols is being loaded.
3. Open the [Crypro Balances](../informational-panels/crypto-balances.md) panel in Quantower to verify that your USDC balance is correctly displayed.
