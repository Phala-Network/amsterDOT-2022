# Phala x amsterDOT Hackathon 2022

![](assets/Logo-bg.svg)

On this page, you will find everything you need to participant in the Phala bounties in the amsterDOT Hackathon event.

Phala Network is a Kusama/Polakdot parachain focusing on trustless cloud computing, based on Secure Enclave technology. Unlike conventional smart contracts, Phala Fat Contracts can:

- **be privacy-preserving**: you can store secret data like private keys, API keys, or privacy data in a contract;
- **interact with HTTP services**: you can build an Oracle or Telegram bot as a Fat Contract;
- **run computation extensive code**: you can build games and analytics jobs in Fat Contracts without block latency.

To learn more about what you can build on Phala, please read the challenge ideas, refer to our [documentation](https://wiki.phala.network/en-us/build/developer/fat-contract-tutorial/).
<!-- and don't forget to join our workshop ==LINK, DATE==. -->

**[Check out the hackathon landing page for more details and information.](https://github.com/Phala-Network/amsterDOT-2022)**

## Challenges and prizes

The challenges are in two categories: (1) Beginner, (2) Advanced.

| Challenge            | Prize (in PHA) | Winners |
| -------------------- | -------------- | ------- |
| Beginner Challenge   | 500            | 50      |
| Advanced - 1st       | TBA            | 1       |
| Advanced - 2nd       | TBA            | 1       |
| Advanced - 3rd       | TBA            | 1       |
| Advanced - qualified | TBA            | -       |

### **In addition, documentation and tutorial contributions are elegible to our [Bounty Program](https://github.com/Phala-Network/bounty-program).**

The contribution can be:

- Fixes or improvements on our [wiki repo](https://github.com/Phala-Network/phala-wiki-next)
- Published video tutorials on Youtube and Twitter (please submit an issue in the Code Bounty Program repo)
- Documentation or bug fixes in our [main repo](https://github.com/Phala-Network/phala-blockchain) or [JS SDK](https://github.com/Phala-Network/js-sdk)

## 📅 Dates

- Start hack: 21 April
- Duration: 6 weeks
- End of hack: 02 June
- Announcement of winners: TBA

## ✍️ Registration

TBA

------------------------------------------------------------------------------------------

## 🧑‍💻 [Beginner Challenge] Link your Github account to on-chain identity with HTTP Request

### Challenge description

In this challenge, you will experience how to use Fat Contract's HTTP request capability to associate a Phala account with a Github user. Such functionality serves as the core for [Decentralized Identity (DID)](https://www.gsma.com/identity/decentralised-identity). Further, we will show how to deploy your contract in [Phala Testnet](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fpoc5.phala.network%2Fws#/explorer) and interact with it through our [frontend SDK](https://github.com/Phala-Network/js-sdk).

The Fat Contract "Redeem POAP" links on-chain accounts to Github accounts and then distributes POAP redeem code to the verified users. The simple protocol is listed below:

1. The user should create a Github Gist with a special format with the account id: "This gist is owned by address: 0x01234...."
2. The user submits the raw file URL to the Fat Contract by a _query_ ("https://gist.githubusercontent.com/[username]/[gist-id]/raw/...")
3. The contract then
    - Verifies the URL is valid
    - Fetches the content of the URL (by Fat Contract's HTTP in Query feature)
    - Verifies the account claim in the gist is valid
    - Extracts the Github username from the URL and the account id from the claim
    - Produces an `Attestation` struct with the Github username and the account id, and signs it with a contract-owned key (by Fat Contract's confidentiality and cryptographic feature)
4. The user receives the `SignedAttestation`, and then submit the attestation to the contract by a `redeem` _command_
5. The contract verifies the attestation, and then links the Github username and the account id
6. If the user didn't claim any POAP, it reveals a POAP code to the user after the verification

By the end of this task, you will be able to:

- Write your first Fat Contract and deploy it to our Testnet;
- Use provided contract frontend to interact with your contract in a secure way.

Follow our [Tutorial](https://wiki.phala.network/en-us/build/developer/fat-contract-tutorial/) for detailed instructions.

## Submission requirements

1. Take a screenshot of the running **Redeem POAP** application
2. Send the screenshots and share your feeling on Twitter
3. Join our [Discord server](https://discord.gg/zQKNGv4) and submit the link to your tweet in the **#amsterdot-hack-submission** chat room.

**Submit the challenge at this repo:** You need to submit the work to this repo as a Github Issue after you have finished the above steps. Please create an issue in this repository with the following information:

- Title: **"Beginner Challenge Submission"**
- Content:
    - The Twitter link
    - Your Discord handler (will contact you for prizes)

We will select the first 50 successful submissions to give out the prize, based on the submission date on the Github issue list.

## Resources

- The tutorial: <https://wiki.phala.network/en-us/build/developer/fat-contract-tutorial/>
- Phala Network core blockchain repo: <https://github.com/Phala-Network/phala-blockchain>
- Frontend UI repo: <https://github.com/Phala-Network/js-sdk>

## Let's connect

- Discord (join #dev group): https://discord.gg/zQKNGv4
- Official site: http://phala.network/
- Github: https://github.com/Phala-Network
- Medium: https://medium.com/phala-network
- Twitter: https://twitter.com/PhalaNetwork/
- Forum: https://forum.phala.network/
