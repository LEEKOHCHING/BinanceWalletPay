# Binance Wallet Pay (NOT Binance Pay)
A standardized Payment QR Code protocol built on the BNB Chain </br></br>
**1. Background**
   
BSC offers a low-cost, high-speed environment without external infrastructure, making it ideal for building payment protocols.
Payment QR Codes are widely accepted globally, with mature user habits and strong compatibility.
Clear use cases include online e-commerce payments and offline QR-based transactions.

**2. Proposal Objectives**
   
To establish a universal Payment QR Code specification that includes:
A standardized format (e.g., transaction amount, target wallet address, memo field, etc.).
Support for multiple payment tokens (e.g., USDT, BTCB, Meme Token.).
Extensibility to accommodate future tokens or payment methods.
A standard URL protocol for requesting native BNB transfers, BNB Token transfers, and BSC transactions allows for a better user experience across apps and wallets in the BNB Chain ecosystem.

**3. Real Case**

With this feature, when users scan the merchant’s QR code using Binance Wallet, both the transaction amount and the Token type will be automatically populated. This not only significantly reduces the risk of errors caused by manual input or incorrect Token selection but also streamlines the payment process, enhancing user experience and transaction accuracy.

**4. Core Features**
   
QR Code Generation and Parsing Specification

Standardized fields ：
```
recipient: Recipient wallet address.

token: The contract address of token

amount: Transaction amount.

memo: Optional memo information.
```

```vb.net
bnb:<recipient>
      ?token=<token ca>
      &amount=<amount>
      &memo=<memo>
```

Examples
```vb.net
URL describing a transfer request for 1 USDT.
bnb:0xded849dedb95bb59dee408650cc8f4e18bd458f4?token=0x55d398326f99059fF775485246999027B3197955&amount=1&memo=OrderId12345
```

```vb.net
URL describing a transfer request for 1,000 Broccoli714 token.(BEP20 Token)
bnb:0xded849dedb95bb59dee408650cc8f4e18bd458f4?token=0x6d5AD1592ed9D6D1dF9b93c793AB759573Ed6714&amount=1000&memo=OrderId12345
```

**5. Ecosystem Value**
   
Enhance BNB's competitiveness in the payment sector, attracting more merchants and users.
Strengthen the connection between BNB and real-world applications, promoting mainstream adoption.
Reduce technical costs for developers and merchants while improving user experience.
