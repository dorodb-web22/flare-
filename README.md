# flare-

RockPaperScissors – On-Chain Game 🎮

A small, clear, and secure Rock–Paper–Scissors implementation on an EVM chain.
Perfect for learning commit–reveal patterns, event-driven flows, and basic game logic in Solidity.

⸻⸻⸻
🔎 Project Description

This repo contains a Solidity smart contract that implements a two-player Rock–Paper–Scissors game using a commit–reveal scheme. Players commit a hash of their move + nonce, then later reveal the move and nonce so the contract can verify and determine the winner on-chain. The contract deploys with no constructor inputs, so it’s super easy to test in Remix or any EVM-compatible testnet.
⸻⸻⸻
🎯 What it Does
	•	Lets Player A create a new game (no inputs).
	•	Lets Player B join that game.
	•	Both players submit a hashed commitment of their move.
	•	After both commits are in, players reveal moves and nonces.
	•	Contract verifies commitments and resolves the winner (or tie).
	•	If a player refuses to reveal, the other can claim a win after a timeout.

⸻⸻⸻
✨ Features
	•	Zero deployment arguments — instant deploy.
	•	Commit–reveal for fair gameplay.
	•	Timeout claim to prevent ghosting.
	•	Event logging for easy tracking and UIs.
	•	Multiple parallel games via gameId.
	•	Beginner-friendly, commented Solidity code.

⸻⸻⸻
🔗 Deployed Smart Contract

Transaction / Verified deployment (Coston2 testnet):
https://coston2-explorer.flare.network//tx/0x26b837ea954a8d58605b86ea4cbda25b31be2899fa600ad926ebe4ec30682343

Tip: Open that transaction to confirm the deployment address and use the contract address to import the ABI into Remix or your frontend.

⸻⸻⸻
🚀 Quick Start (Remix)
	1.	Open Remix → create a new file RockPaperScissors.sol and paste the contract source above.
	2.	Compile with the Solidity version ^0.8.20 (or exact 0.8.20). Match optimizer settings if you want to verify on explorers.
	3.	Deploy to Coston2 (Flare testnet) or any EVM testnet. No constructor args required.
	4.	Once deployed, use the transaction link above to cross-check the deployed address and logs.

⸻⸻⸻
🧾 Verification & Explorer Tips
	•	If you want the contract source verified on Routescan/Blockscout, use the exact compiler version and optimizer settings used in Remix.
	•	The provided transaction link will show the deployer and bytecode; use that address for verification/import.
