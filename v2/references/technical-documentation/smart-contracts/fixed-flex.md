# Fixed Flex

### Introduction to Fixed Flex Bonds

Fixed Flex Bonds are a novel financial instrument within Amet Finance, designed to offer flexibility and security in the DeFi space. These bonds allow issuers to raise capital by offering bonds that can be purchased with any token and provide returns in a different token. This dual-token mechanism is a standout feature of Fixed Flex Bonds, offering unparalleled versatility in how bonds are structured and executed.

#### Key Features:

* **Flexibility in Tokens**: Issuers can set up bonds with any ERC20 token as the purchase token and choose a different ERC20 token as the payout token.
* **Depositing Payouts**: Issuers can deposit the payout tokens into the contract at any time before the bond's maturity, not necessarily at the point of issuance.
* **Transparency for Investors**: Purchasers can view what percentage of the total payout is currently held in the contract, ensuring transparency and trust in the bond's solvency.

### Detailed Example with Alice and Bob

Let's consider a scenario where Alice, the issuer, wants to raise capital by issuing a bond. She decides to accept DAI as the purchase token and will provide returns in ETH.

1. **Issuance**: Alice creates the bond using `Issue.sol`, setting DAI as the purchase token and WETH as the payout token. She defines the total number of bonds, the price per bond, the payout, and the maturity date.
2. **Purchase**: Bob, an investor, finds Alice's bond offering appealing. He purchases bonds using DAI. The contract records Bob's investment, and he receives NFTs representing his stake.
3. **Payout Deposit**: Alice doesn't need to deposit WETH immediately upon issuing the bonds. However, before the maturity date, she deposits enough WETH into the contract to cover the bond repayments, ensuring she meets her obligations to bondholders.
4. **Redemption**: At maturity, Bob can redeem his bonds to receive his payout. He can see the percentage of the total payout available in the contract at any time, ensuring transparency.

### Contract Overview

* **Issue.sol**: This contract handles the issuance of new bonds, allowing issuers to define the terms and conditions of the bond, including the tokens involved and the financial parameters.
* **Bond.sol**: Represents individual bond contracts, tracking the investments, purchase, payout, and managing the redemption process.
* **Vault.sol**: Manages the financial aspects, including the storage and handling of fees.

### Referral and Fee Structure

* **Referral Rewards**: When a bond is purchased through a referral, the referrer earns a reward, incentivizing users to promote bond offerings. The reward is a percentage of the purchase amount, paid in the purchase token.
* **Issuance Fee**: Alice pays an issuance fee to create the bond, contributing to the platform's sustainability and security.
* **Purchase Fee**: Each time a bond is purchased, a fee is deducted, part of which can be allocated as the referral reward. The rest supports the platform's operational costs and development.

Fixed Flex Bonds offer a dynamic and secure way for issuers and investors to engage with the DeFi bond market, backed by transparent and robust smart contract functionality. By leveraging these contracts, Amet Finance provides a versatile platform for raising capital and investing in the growing world of decentralized finance
