---
title: "Block Construction"
seoTitle: "Steps in Block Construction"
seoDescription: "Learn about block construction, from transaction validation to consensus mechanisms, and how blocks are built and added to a blockchain"
datePublished: Mon Dec 02 2024 17:38:55 GMT+0000 (Coordinated Universal Time)
cuid: cm47be2wc000509jj2myt4p7j
slug: block-construction
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/MykFFC5zolE/upload/cdfcd0ddd17fe84a6dedd9c8ee3c0647.jpeg
tags: blockchain

---

**Block construction** is the process of creating and finalizing a block, which is a collection of data (mostly transactions) that gets added to the distributed ledger.

## **Step in Block Construction**

**Step 1. Transaction Pool (Mempool):**

*Step a*: Unconfirmed information submitted by the network's participants is stored in a *temporary pool* called *the mempool*.

*Step b*: The miner or validator selects transactions from this pool to construct a block.

**Step 2. Transaction Validation**

Each transaction is checked for:

\- *Validity*: Verifying signatures and ensuring sufficient balances.

\- *Double-Spending:* Ensuring that no coins are spent more than once

\- *Network Rules*: Conforming to blockchain protocol rules.

**Step 3: Merkle Tree Construction**

Transactions are organized into a *Merkle Tree*:

\- Transaction hashes are paired and hashed together recursively until a single root hash, the *Merkle Root*, is generated.

**Step 4. Consensus Mechanism:**

The method of block construction depends on the blockchain’s consensus algorithm: *1\.* ***Proof of Work (PoW)****:*

Miners compete to solve a cryptographic puzzle by finding a nonce that satisfies the block’s target difficulty. The first miner to solve the puzzle broadcasts the block to the network for validation.

*2\.* ***Proof of Stake (PoS)****:*

Validators are selected based on the amount of cryptocurrency they have staked. The selected validator proposes (đề xuất) a block, which is then voted on or validated by other participants.

*3\.* ***Other Mechanisms****:*

**Delegated Proof of Stake (DPoS)**: A small set of elected delegates construct blocks.

**Proof of Authority (PoA)**: Validators are pre-approved authorities.

**Step 5. Adding Metadata**

Additional data is added to the block header, such as the block’s height and consensus-related metadata (e.g., the validator’s identity in PoS).

**Step 6. Block Propagation and Verification:**

• The constructed block is broadcast to the network.

• Other nodes verify:

• The block’s structure and validity.

• The correctness of transactions.

• That the block hash matches the network’s difficulty target (in PoW).

**Step 7. Adding the Block to the Chain:**

Once validated, the block is appended to the blockchain. The blockchain updates its state (e.g., account balances, smart contract outputs).

**Tóm tắt**:

* Thông tin từ các participants của network trình lên mempool (thường là các transactions) =&gt; Miner (POW) hoặc Validator (PoS) sẽ chọn 1 block để qua bước xác thực. (Usually prioritizing in order of higher fee.)
    
* Sau đó sẽ lựa chọn các miner/validator và xác thực block : Miner của POW thì giải puzzle ai giải được trước thì đưa qua vòng validation / Validator thì sẽ được chọn dựa theo stake, sau đó thì phải trình lên cho các validators khác xác thực.
    
* Nếu pass, tạo merkle tree bằng cách pair các hash của các tx với nhau cho dến khi tạo thành 1 merkle root. (for ensuring the intergrity of the chain).
    
* Adding metadata và đưa block đã xác thực vào network.