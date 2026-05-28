
# Time Coin: A Time-Based Decentralized Currency White Paper

> Tian zhi dao, sun you yu er bu bu zu.  
> — Tao Te Ching, Chapter 77

## Abstract

This paper proposes the first purely time-based decentralized monetary system in human history. The system implements the core mechanism of "one device, one vote, one wallet" based on Physical Unclonable Functions (PUF), achieves the unforgeability of time based on Verifiable Delay Functions (VDF), and relies on the Bitcoin blockchain for ultimate security and full-chain transparency.

The sole basis for Time Coin issuance is verifiable online time. Any entity possessing a connectable smart device, by expending an equal amount of verifiable time, receives an equal amount of Time Coin. There are no capital thresholds, no technical thresholds, and no identity thresholds. The only way to adjust any system parameter is through real-time voting by all nodes on a one-person-one-vote basis.

Time Coin does not attempt to design fairness; it is fairness itself. It does not attempt to hide any information; it is completely transparent itself. It does not attempt to solve problems; it allows problems to dissolve on their own.

---

## 1. The Problem

Since the birth of Bitcoin, all cryptocurrencies have failed to solve two fundamental problems:

- The monopoly of capital over currency issuance rights: Under the PoW mechanism, capital can monopolize bookkeeping and issuance rights by purchasing computing power; under the PoS mechanism, capital can monopolize staking rights and issuance rights by holding tokens; all other consensus mechanisms ultimately evolve into a game of capital.
- Exploitation caused by information asymmetry: The circulation history and flow of funds are obscured, allowing money laundering, fraud, and speculative activities to thrive.

The root of the problem lies in the fact that all such currencies attempt to seek fairness in the spatial dimension and all retain artificially designed information barriers.

**The only resource that cannot be bought by capital, cannot be accelerated, and cannot be forged, is time.**  
**The only method that can completely eliminate exploitation is complete, unconditional transparency.**

---

## 2. Three Unshakable Core Rules

The entire set of rules for Time Coin consists only of the following three articles. There are no exceptions, no patches, and no hidden clauses.

### Rule One: One Device, One Vote, One Wallet

Any single independent physical computing device possesses and can only possess one node identity and one bound wallet. This binding relationship, once established, cannot be dissolved. Each node can receive, and can only receive, one Time Coin per consensus cycle.

The node identity is automatically generated from the device's built-in Physical Unclonable Function (PUF) chip and the Bitcoin block height hash. It is globally unique and non-repeatable. Resetting the system will permanently lose the wallet, and only a new wallet can be regenerated.

The wallet private key is physically derived at the hardware layer by the PUF chip and never exists outside the chip in any digital form (such as mnemonic phrases or ciphertext). The user's control over the wallet is equivalent to absolute possession of the physical device; there is no "independent custody" separate from the device.

When a device's PUF fails due to aging, damage, or any other reason, that node dies permanently and stops generating Time Coin; any Time Coin already in its wallet will be permanently frozen along with that node and exit circulation. No one can transfer or recover them. If the device ages, existing Time Coin in the wallet can be transferred in advance to any other valid node. If the device is lost, the only recovery method is to retrieve the device.

Any operation such as resetting the system, formatting the device, or replacing the chip will permanently destroy the locally stored wallet private key and all Time Coin data.

Even on the same physical device, the node identity and wallet generated after a reset are entirely new and independent, bearing no relation to the previous identity and wallet.

All Time Coin in the original wallet, having permanently lost the ability to obtain signature authorization from the original PUF chip, can never again participate in any transaction, effectively equivalent to physical destruction. This is like throwing cash into a fire: the money itself has not vanished, but it can never be used by anyone again.

Pure software virtual environments (without a physical PUF chip) cannot generate valid node identities and wallets.

The node rights of all devices are completely equal: a 50 Raspberry Pi = a $10,000 phone = a $100 million supercomputer.

Any device, at any location, receives exactly the same yield per unit of time.

**Timeline Lockdown:**  
The economic life of a physical device possesses absolute exclusivity. When a device's PUF chip is first activated by any compliant client based on this protocol, an irreversible "protocol lock" flag is generated inside the PUF's secure enclave. Once locked, that PUF chip absolutely refuses, at the physical level, to perform handshake or signing computations with any other protocol fork client.

Within the lifecycle of a single physical device, it can, and inevitably must, participate in the time proof of only one Time Coin fork chain. If a node entity intends to participate in another fork chain, the only legal path is to acquire another brand new, unactivated physical device.

This protocol deprives a single physical device of the right to simultaneously hold multiple time-based currencies. The choice of which time rule to follow must be paid for with the corresponding physical hardware cost.

### Rule Two: Time Standard · Full-Chain Transparency

The sole basis for Time Coin issuance is verifiable online computing time. The complete lifecycle of every single Time Coin will be permanently recorded in an immutable manner.

- No pre-mining, no founder rewards, no institutional allocations, no form of advance distribution whatsoever.
- There is no fixed total supply cap; the issuance volume is automatically proportional to the number of active nodes across the network.
- There is no offline time compensation; only nodes that complete continuous VDF calculations online can receive Time Coin.
- All nodes compute the same Verifiable Delay Function (VDF) simultaneously, based on the same Bitcoin block hash.
- The non-parallelizable nature of the VDF ensures that the only difference in completion time among all nodes is due to physical variance.
- All devices that finish computing early must wait for the network-wide broadcast of the next consensus cycle before continuing.
- The consensus cycle is an integer multiple of the VDF computation count, determined by real-time weighted voting of all nodes.
- For every consensus cycle of continuous VDF computation completed, all active nodes simultaneously receive one and only one Time Coin.
- Every single Time Coin will permanently record the block height of its birth and the PUF identifier of its generating device.
- Every transaction of every single Time Coin permanently records the transaction time and the wallet identifiers of both sender and receiver, achieving one independent ledger per Time Coin.
- Ownership of Time Coin can only be transferred via peer-to-peer transfer; any form of export, duplication, or backup is invalid.
- Every Time Coin inherently carries a complete transaction history chain; any transfer of ownership must add a new transaction record to the history chain of that Time Coin itself.
- Every transaction must be validated by the PUF chip signature of the sending device before it can take effect.
- Each Time Coin is the smallest unit, indivisible, and can only be transacted in integer multiples.
- Any Time Coin data that leaves its corresponding wallet loses its complete history chain, cannot be verified by the entire network nodes, and is considered invalid currency.

**Definition of Time Coin: Unit and Circulation**

- **Smallest unit: 1 Time Coin**  
  The Time Coin is an indivisible, uncuttable, non-subdividable complete unit of value, corresponding to the unique time output of a single device within one consensus cycle.

- **Non-Mergeable Time Coin Ontology**  
  Any multiple Time Coins cannot be merged, combined, or compressed. Every single Time Coin, from its birth to the cessation of its circulation, perpetually maintains an independent identity and independent history chain.

- **Integer Transactions Only**  
  All transfers, payments, and exchanges can only be conducted in integer amounts of 1, 2, 3... No decimals, no change splitting.

- **History Only Appends, Never Alters**  
  The transaction history of each Time Coin can only append new records; it cannot be deleted, tampered with, overwritten, merged, or simplified.

- **Departure from Wallet Means Death**  
  The sole legitimate environment for a Time Coin's existence is the hardware secure enclave within the "hot wallet" memory area protected by the device's PUF chip hardware-level encryption.

  - **Export Prohibition:** Time Coin data and its derived private keys are absolutely forbidden to leave the PUF secure enclave in any form (export files, screenshots, copy-paste, plaintext network transmission) and enter conventional operating system memory or external storage. Once such a downgrade occurs, it immediately triggers a "history break," and its internal state is instantly marked by the system as "history broken."
  - **Re-import Prohibition:** Any behavior attempting to re-import Time Coin data that has ever left the PUF environment back into a wallet will be automatically recognized and rejected by the entire network nodes.
  - **Fragmentation Equals Invalid Coin:** When a transaction is initiated, the receiving party's PUF, upon receiving the data, will verify the causal chain of that Time Coin. If it discovers any spliced traces within the chain not generated by a PUF physical signature, or detects conditions such as timestamp inversion or hash breaks, it is judged as "history fragmentation." A Time Coin that triggers an alert is rejected by the entire network and considered invalid currency.
  - **Legitimate Peer-to-Peer Enclave Handshake:** The only permitted "transfer" is a "state-append handshake" conducted directly between the PUF secure enclaves of two online devices via an encrypted channel. The Time Coin data packet must never pass through any third-party server or non-PUF environment under any circumstances.

- **Transactions Are State Append, Not Data Relocation**  
  When a user replaces an old phone with a new one, the experience feels like "Time Coin has been transferred to the new phone," but in the underlying logic:  
  The old phone's PUF secure enclave physically signs and appends a record to the end of the local Time Coin's causal chain: "Control transferred to new phone PUF hash."  
  Subsequently, the old PUF enclave establishes a peer-to-peer encrypted tunnel with the new PUF enclave and directly pushes this "complete Time Coin data with its updated tail" into the new phone's PUF enclave. Throughout the entire process, the Time Coin data never touches any conventional operating system, achieving absolute security isolation.

- **The Sole Purpose of the Blockchain: Time Notarization**  
  The underlying network of this protocol (such as the Bitcoin blockchain) does not assume a "bookkeeping" function; it merely serves as an "absolute time notary."  
  Whenever a Time Coin internally appends a transfer record, the existence of the blockchain is solely to provide an "immutable external timestamp hash" for the internal causal chain of the Time Coin, used to assist in proving that its history has not been rolled back. The blockchain does not store any transaction data or user information of Time Coin.

### Rule Three: Universal Real-Time Governance

The sole mechanism for adjusting any system parameter is the continuous real-time weighted voting of all active nodes. The consequences of any adjustment are borne jointly by all nodes.

- The only adjustable parameter is the length of the consensus cycle.
- The system presets 15 options for exponentially growing consensus cycles. Any node can choose any option at any time and can change its choice at any time.
- Votes, as part of the node's state, propagate automatically across the entire network with the node's heartbeat.
- All nodes independently calculate and verify the network-wide voting result, taking the vote shares of the top 10 options with the highest total votes to calculate a weighted average, thereby deriving the current effective consensus cycle.
- The effective consensus cycle is automatically updated and takes effect immediately every 10 minutes. There are no voting periods, no approval processes, and no central statistical node.
- Credentials generated without accepting the consensus, or by tampering with the time cycle, do not possess Time Coin properties within this time chain, are considered invalid data, and will be directly rejected for reception, verification, and transaction by all network nodes.
- Consensus can be formed with two or more devices online.
- Adjustment of any other parameter is illegal.

---

## 3. Self-Regulating Mechanism

Time Coin requires no human intervention; it is a perfectly self-balancing system.

### Automatic Dissolution of Capital Attacks

If a capital party purchases a large number of devices attempting to monopolize issuance rights, the following multi-layered automatic balancing mechanisms will be triggered:

- Increase in total network node count → Time Coin issuance volume increases synchronously → The price of a single Time Coin automatically falls.
- All nodes vote to extend the consensus cycle → The yield per unit time for all nodes decreases correspondingly.
- The capital party's rigid costs for electricity, bandwidth, venue, and labor remain unchanged → Profits shrink dramatically.
- Large-scale mining farms will face exponentially increasing manual transaction costs; the larger the scale, the more severe the loss.
- When revenue falls below cost, the capital party automatically shuts down and leaves → The system returns to equilibrium.

Individual users are almost entirely unaffected (smart devices are already in long-term operation, and the marginal cost of participating as a node is nearly zero).

### Automatic Price Stability

The value of Time Coin is perpetually anchored to the benchmark of "1 Time Coin = verifiable human time of 1 consensus cycle." Its price will not stabilize around the operating cost; instead, the operating cost will automatically stabilize around the price of Time Coin.

- Time Coin price rises → More users run nodes → Supply increases → Price falls back.
- Time Coin price falls → Speculators leave → Supply decreases → Price rebounds.

This mechanism inherently avoids dramatic surges, crashes, and speculative hype. The price of Time Coin is essentially the fair price of time.

### Automatic Isolation of Toxic Assets

All transaction histories are completely open and transparent; the market will automatically complete screening and isolation:

- Time Coins involved in illegal transactions will be spontaneously refused acceptance by most merchants and users.
- Any market entity can autonomously refuse any Time Coin involved in illegal transactions, without needing approval from any third party.
- There is no unified, mandatory blacklist; all filtering behavior is voluntary and market-driven.

---

## 4. Security

The security of Time Coin is jointly guaranteed by physics and mathematics:

- **Sybil Attack Immunity:** The combination of PUF and Bitcoin block height hash ensures that a single physical device can only generate one unique node identity over its entire lifecycle.
- **Computational Power Attack Immunity:** VDF is non-parallelizable; the level of computing power does not affect the yield per unit time.
- **Theft Immunity:** The wallet private key is completely controlled by the user; the system stores no private keys.
- **Double-Spend Immunity:** Time Coin can only be transferred peer-to-peer between compliant wallets and cannot exist independently separate from its corresponding wallet.
- **51% Computational Power Attack Immunity:** Acquiring 51% of issuance rights would require controlling 51% of the world's smart devices, which is economically unfeasible.

---

## 5. Forks and Evolution

This protocol does not prohibit forks. Any fork based on this protocol is legal, and users are free to choose any chain to use.

Forks are the system's self-evolution mechanism. If a fork modifies the rules of this protocol and gains recognition from more users, it will become the de facto main chain. All forks not recognized by users will naturally perish due to the absence of active nodes running them.

No individual or organization has the right to determine which chain is "official." The sole arbiter is the free choice of all users.

A single device can only compute one VDF at any given time. Therefore, if one device installs two or more time fork wallets simultaneously, due to the non-parallelizability of computation, the redundant wallets will be unable to produce valid time proofs, and will be directly judged as invalid at the protocol level.

Absolute Isolation of the Time Dimension: The time scales of various fork chains are mutually independent; a Time Coin only possesses circulation legitimacy within the time chain where it was born. Any cross-chain transfer behavior cannot generate a continuous PUF signature causal chain at the cryptographic level, effectively equivalent to physical destruction and re-generation. The possibility of cross-chain circulation does not exist.

**All Time Coins based on this protocol and their forks must be completely open-source to allow verification of the authenticity and compliance of their protocol implementation.**

---

## 6. The Philosophical Declaration of Time Coin

### Absolute Decentralization: The Total Dissolution of Power and the Birth of a Self-Evident System

Time Coin does not pursue decentralization, because within the underlying architecture of Time Coin, the concept of a "center" simply does not exist. All past monetary systems, regardless of their technological packaging, have never been able to escape three implicit supreme powers: issuance rights, bookkeeping rights, and rule adjudication rights. Through the rigid constraints of physics and mathematics, Time Coin completely "dissolves" these three powers, returning them to every independent individual node.

**1. The Dissolution of Issuance Rights: From "Third-Party Granting" to "Self-Evident Time"**  
Within the Time Coin network, no entity possesses the privilege of issuing currency. The act of "issuance" itself is downgraded to the objective physical phenomenon of "time elapsing while a physical device is online."  
No miner block rewards needed, no staking for interest. Your device exists, time passes, the VDF computation is completed, and the coin is "natively" generated inside your device. Time Coin has no issuer, only witnesses of time.

**2. The Dissolution of Bookkeeping Rights: From "Global Dependency" to "One Coin, One Proof"**  
Traditional blockchains rely on all network nodes to jointly maintain a single "general ledger," meaning the legitimacy of your assets must depend on the acknowledgment of strangers.  
Time Coin's "one coin, one ledger" mechanism completely severs the dependency on a global ledger. Every Time Coin inherently carries an immutable causal chain; its legitimacy does not depend on records from any external node, but solely on the continuity of its own history and the PUF physical signatures of every controller in its chain. Others can neither help you keep your books nor tamper with your ledger.

**3. The Dissolution of Rule Adjudication Rights: From "Code Dictatorship" to "Real-Time Emergence"**  
In the Time Coin protocol, the adjustment power for the sole variable parameter (the length of the consensus cycle) does not reside in the hands of any developer, foundation, or super-node. It is entirely derived in real-time through weighted voting by all active nodes during every heartbeat cycle.  
There are no proposals, no voting days, no community governance committees. The system's rules adaptively emerge in real-time based on the current number of nodes, much like the flow rate of water. Time Coin has no ruler, only the physical-level self-consistency of algorithms.

---

## 7. Conclusion

Time Coin is not a replacement for Bitcoin, but the completion of Bitcoin.

- Bitcoin achieved "the inviolability of existing stock."
- Time Coin achieves "the fair sharing of incremental value" and "full-chain transparency."

Time Coin does not attempt to replace fiat currency, nor to eliminate nations, but awaits the arrival of a human community. It does not command anyone to do anything, nor does it prohibit anyone from doing anything. It merely provides the most basic framework, and then lets all of humanity engage in their own negotiations, self-regulate, and create the future themselves.

Time Coin has not created any new rules; it has simply written the universe's most fundamental laws — "the passage of time, the irreversibility of causality" — into code.

> This is "Wei dao ri sun, sun zhi you sun, yi zhi yu wu wei."  
> This is Tian zhi dao.

---

## Appendix

**This white paper is the sole official normative document for the Time Coin protocol. This protocol has no official code, no official implementation, no official website, no founder, and no form of official organization. Any entity is free to implement this protocol. All protocol implementations that conform to the rules of this white paper are valid Time Coin protocols.**

> Because true justice needs no father.

*Signed: Dao Heng Wu Ming*
