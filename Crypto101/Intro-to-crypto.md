# Beginner's Guide To Crypto

Hey everyone, we get a lot of questions about crypto coins. I thought I'd make a resource that could help more beginners learn the basics.

## What's The Blockchain
A blockchain is a digital ledger of transactions that is duplicated and distributed across the entire network of computer systems on the blockchain. Its contents are public, but they are encrypted by different types of hashing algorithms.

The blockchain serves as a database, such as an SQL database. The difference is that nobody is in charge of the Blockchain and no single party can make adjustments to the information that is stored on it.

It differs from a typical database in the way it stores information because blockchains store data in blocks that are then chained together. Each new block contains information that is derived from it's predecessors.

Blockchains are immutable, which means that the data entered is irreversible, making the blockchain ideal for storing ledgers of transactions.

There is a lot more to add when explaining what are blockchains and how does all that work, but I'll leave you off with a [video](https://www.youtube.com/watch?v=bBC-nXj3Ng4) that covers all the basics.

Verifying the transactions that are stored on the blockchain is usually done by using computing power to solve the encrypted messages in a specific algorhitm [PoW](https://ethereum.org/en/developers/docs/consensus-mechanisms/pow/) thus reaching consensus of what transactions are valid, or by staking specific amount of coins in a single wallet as collateral for the transactions that are verified [PoS](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/).
## Consensus Mechanisms

- Proof of Work PoW
- Proof of Stake PoS
- Mixed combination of PoW and PoS
- Proof of Space [PoSpace](https://www.chia.net/) *In my opinion, Proof of Space as used by Chia Coin would go under PoW Consensus Mechanisms.*

### Proof of Work

Proof of Work (PoW) is a consensus mechanism that requires computing power to solve encrypted messages in a specific algorhitm in order to verify their validity. algorithm that sets the difficulty and rules for the work miners do. Mining is the work itself. It's the act of adding valid blocks to the chain, thus creating the blockchain in real time.

The proof-of-work protocol requires miners to go through an intense race of trial and error to find the nonce for a block. When racing to create a block, a miner will repeatedly put a dataset, that you can only get from downloading and running the full chain (as a miner does), through a mathematical function to verify if the transactions that are submited are valid.

All blockchains are configured differently, but all have built in features for protecting against fraudulent entries by requiring the transaction to be seen as valid after a number of new blocks. This means that if a miner mistakenly verifies a transaction, it still needs to be verified by other miners who will create new blocks thus reaching consensus that the information is true.

Depending on the blockchain algorhitm and it's decryption methods, we can easily devide the PoW blockchains into CPU mineable, GPU mineable and ASIC mineable blockchains.

All PoW blockchain incentivise their miners to contribute their computing power by rewarding the miners for successfully minting a new block. Most blockchains are configured to reduce the number of newly minted coins for each new block and only incenivise miners with the transaction fees that are consumed by users that are transacting over that blockchain.

The objective of PoW is to extend the chain. The longest chain is most believable as the valid one because it's had the most computational work done on it. Because miners work in a decentralized way, it's possible for two valid blocks to be mined at the same time. This creates a temporary fork. Eventually one chain will become the accepted chain once a subsequent block has been mined and added, making it longer.

To consistently create malicious, yet valid, blocks, you'd need over 51% of the network mining power to beat everyone else. You'd need a lot of computing power to be able to do this amount of "work". And the energy spend might even outweigh the gains you'd make from such attack.
### Proof of Stake

Unlike proof-of-work, validators don't need to use significant amounts of computational power because they're selected at random and aren't competing. They don't need to mine blocks; they just need to create blocks when chosen and validate proposed blocks when they're not. This validation is known as attesting. You can think of attesting as saying "this block looks good to me." Validators get rewards for proposing new blocks and for attesting to ones they've seen.

In order to participate in the Proof of Stake consensus protocol, you are required to put a stake, specific amount of coins in your node thus becoming a validator. It's important to add that if you attest to malicious blocks, you lose your stake and lose your coins.

There are a lot of concerns about PoS, since PoS requires users to lock up significant amounts in their stakes, this is usualy seen as more money for the rich etc. etc. This [video](https://www.youtube.com/watch?v=9rgyH_GljZw) gives a nice outline of the Benefits and Flaws of PoS.

### Combination of PoW and PoS

Hybrid PoW/PoS consensus mechanisms utilize elements of both PoW and PoS models when determining transaction validation rights, and for doing so, hybrid aims to mitigate the weaknesses of each consensus mechanism.

A hybrid consensus starts with having PoW miners to create new blocks containing transactions to be added to the blockchain. Once these blocks are created, PoS miners decide whether to confirm them or not. PoS miners purchase votes by staking a portion of their tokens. However, instead of examining the total vote count, the hybrid PoW/PoS mechanism randomly chooses 5 ‘votes’ to determine the efficacy of the newly created block.

Hybrid blockchains are slowly starting to drop out of flavor due to the double dependencies, one being on the miner with the most computing power, and one being the stakers with the biggest stakes or the eldest wallets on the chain. This could easily translate to early adopters of that blockchain having superior positioning over new participants. That does mean that this consensus mechanism is less succeptable to 51% attacks and eliminates the possibility of hash power monopoly to a great extent and ensures the security of the network.

## Mining

Mining is widely known in cryptocurrency as the Proof of Work (PoW) decentralized consensus mechanism for validating transactions and creating new blocks on the blockchain.

To successfully mine a block, your computing power will need to solve encrypted messages in a specific algorhitm or a set of different algorhitms and verify the contents of the messages.

There are many algorhitms and alterations of the main ones with the adition of some features unique to their blockchains.

In this tutorial, I'm going to devide the algos by the preffered computing power required for solving messages in their blockchain.

### CPU Mining

When Bitcoin was first released, you could mine 100 coins a day using just your CPU. Unfortunately, today it’s impossible to mine Bitcoin with your CPU due to the ASICs specially designed and built to solve Bitcoin's algorithm. 
CPUs have fewer arithmetic logic units, circuits that perform arithmetic operations, and thus are relatively slow when it comes to performing large amounts of calculations.

However, there are a ton of algorhitms that are designed specifically for CPU mining and are usualy configured to run memory bound hashing algorithms that “rely on random access to slow memory.” Since this isn't the most efficient problem solving methodology, this generally means that GPUs and ASICs are as effective as CPUs but due to their significantly higher power consumption they are not profitable.

Sometimes the CPU algorhitm solving capabilities are bolstered by configuring blockchains to be able to run on multiple algorhitms that greatly reduces risks of Aplication Specific Integrated Circuits overtaking the blockchain.

#### CPU Mineable Algorhitms

### GPU Mining

