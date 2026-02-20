# 🗳️ Blockchain – Transparent & Secure Blockchain - Based Voting System

**Secure, transparent, and tamper-proof voting system** built on the **Algorand blockchain**.

This project demonstrates **on-chain governance**, **smart contract-based proposal creation**, and **wallet-integrated voting** using **Algorand's high-performance blockchain**.

---

## 🚀 Project Overview

**BlockChainVoting** is a decentralized voting platform built using:

* 🔹 **Algorand Smart Contracts** (PyTeal / AlgoKit)
* 🔹 **React + TypeScript** Frontend
* 🔹 **AlgoKit** monorepo structure
* 🔹 **Wallet integration** for secure voting

### ✅ Key Features

* ✅ **Secure on-chain voting**
* ✅ **Smart contract-based proposal creation**
* ✅ **Transparent vote counting**
* ✅ **Wallet integration**
* ✅ **Frontend + Smart Contract architecture**

### 🛡️ Guarantees

* 🔒 **Tamper-proof voting**
* 🔍 **Transparent results**
* ⚖️ **Decentralized governance logic**

---

## 🧠 How Voting Works

```
1️⃣ Admin deploys the voting smart contract
    ↓
2️⃣ Proposals are created on-chain
    ↓
3️⃣ Users connect wallet
    ↓
4️⃣ Users cast vote (recorded on blockchain)
    ↓
5️⃣ Results are fetched transparently via Indexer
```

Each vote:
* ✅ Is **immutable**
* ✅ Is **publicly verifiable**
* ✅ **Cannot be altered**

---

## 📂 Project Structure

```
BlockChainVoting/
│
├── projects/
│   ├── contracts/            # Smart Contracts
│   │   └── smart_contracts/  # Voting logic
│   └── frontend/             # React Frontend
│       ├── src/
│       │   ├── Home.tsx      # Landing page
│       │   ├── components/   # Voting UI
│       │   ├── contracts/    # Generated contract clients
│       │   └── utils/        # Network configuration
│       └── .env              # Environment variables
│
├── algokit.yaml
└── README.md
```

### 🔹 Smart Contracts

**Location:** `projects/contracts/smart_contracts/`

Contains:
* Voting logic
* Proposal creation
* Vote casting
* Result computation

### 🔹 Frontend

**Location:** `projects/frontend/`

Important files:
* `src/Home.tsx` → Landing page
* `src/components/` → Voting UI
* `src/contracts/` → Generated contract clients
* `src/utils/network/` → Network configuration

---

## 🛠️ Tech Stack

### Backend (Smart Contracts)
* **Algorand Blockchain**
* **PyTeal** (Smart Contract Language)
* **AlgoKit** (Development Framework)

### Frontend
* **React** + **TypeScript**
* **Vite** (Build Tool)
* **TailwindCSS** (Styling)
* **Algorand Wallet Integration**

### Tools
* **AlgoKit CLI**
* **Docker**
* **Node.js 18+**

---

## ⚙️ Setup & Installation

### Prerequisites

Before starting, ensure you have:

* ✅ **Docker** (running)
* ✅ **Node.js 18+**
* ✅ **npm**
* ✅ **AlgoKit CLI** installed

Install AlgoKit from official docs:  
👉 [https://developer.algorand.org/docs/get-started/algokit/](https://developer.algorand.org/docs/get-started/algokit/)

---

### 1️⃣ Clone Repository

```bash
git clone https://github.com/sane-eagle/BlockChainVoting.git
cd BlockChainVoting
```

### 2️⃣ Bootstrap Workspace

```bash
algokit project bootstrap all
```

This will:
* Install dependencies
* Setup Python virtual environment
* Install smart contract requirements
* Install frontend dependencies

### 3️⃣ Build All Projects

```bash
algokit project run build
```

### 4️⃣ Run Frontend

```bash
cd projects/frontend
npm install
npm run dev
```

App will run at:
```
http://localhost:5173
```

---

## 🔐 Environment Variables

Create a `.env` file in `projects/frontend/`:

```env
# Algod (TestNet)
VITE_ALGOD_SERVER=https://testnet-api.algonode.cloud
VITE_ALGOD_PORT=
VITE_ALGOD_TOKEN=
VITE_ALGOD_NETWORK=testnet

# Indexer
VITE_INDEXER_SERVER=https://testnet-idx.algonode.cloud
VITE_INDEXER_PORT=
VITE_INDEXER_TOKEN=
```

**Important:** Restart dev server after editing:

```bash
npm run dev
```

---

## 🧪 Testing on TestNet

Make sure:

* ✅ Wallet is connected
* ✅ Account is funded (TestNet ALGO)
* ✅ App ID is correct
* ✅ Network = TestNet

### Get TestNet ALGO from:
👉 [https://bank.testnet.algorand.network/](https://bank.testnet.algorand.network/)

---

## 🔧 Smart Contract Interaction

Generated TypeScript clients are located at:
```
projects/frontend/src/contracts/
```

### Available Functions

Frontend calls:

* `deploy()` → Deploy voting contract
* `createProposal()` → Add new proposal
* `vote()` → Cast vote
* `getResults()` → Fetch results

### Example Usage

```typescript
import { VotingClient } from './contracts/VotingClient';

// Cast a vote
await votingClient.vote({
  proposalId: 1,
  voteChoice: 'yes'
});

// Get results
const results = await votingClient.getResults();
```

---

## 🎨 UI Customization (Hackathon Tip)

You can safely redesign the UI without breaking logic!

### Example Prompt for AI Redesign

```
Redesign projects/frontend/src/components/Voting.tsx using TailwindCSS 
to look like a modern Web3 governance dashboard. Include:
- Proposal cards
- Vote buttons (Yes / No)
- Wallet connection banner
- Results progress bar

Keep ALL logic, wallet connections, and contract calls EXACTLY as-is. 
Modify only JSX and Tailwind classes.
```

---

## 🐛 Troubleshooting

### ❌ "Missing VITE_ALGOD_SERVER"
* Check `.env` file exists in `projects/frontend/`
* Restart dev server

### ❌ Transactions Fail
* Ensure wallet is funded with TestNet ALGO
* Confirm TestNet is selected in wallet
* Confirm correct App ID

### ❌ Votes Not Updating
* Verify Indexer config in `.env`
* Check network consistency (TestNet vs MainNet)

---

## 🚀 Hackathon Extension Ideas

* 🎯 Add **time-restricted voting**
* 🎨 Add **NFT-based voting rights**
* 💰 Add **DAO treasury logic**
* 📊 Add **quadratic voting**
* 🗳️ Add **multi-proposal elections**
* 📈 Add **live result charts**
* 🔔 Add **notification system**
* 👥 Add **delegate voting**

---

## 🌐 Deployment

### Deploy Smart Contract

```bash
algokit deploy
```

### Deploy Frontend

Deploy to:
* **Vercel**
* **Netlify**
* **Railway**

Add environment variables in hosting dashboard.

---

## 📚 Useful Resources

* **Algorand Developer Portal**  
  [https://developer.algorand.org/](https://developer.algorand.org/)

* **AlgoKit Docs**  
  [https://developer.algorand.org/docs/get-started/algokit/](https://developer.algorand.org/docs/get-started/algokit/)

* **Algorand Workshops**  
  [https://algorand.co/algokit-workshops](https://algorand.co/algokit-workshops)

* **Algorand Discord**  
  [https://discord.gg/algorand](https://discord.gg/algorand)

---

## 🏆 Why BlockChainVoting?

* 🔍 **Transparent governance**
* ⛓️ **Fully on-chain**
* 🔒 **Secure and immutable**
* 🏛️ **Real-world DAO foundation**
* 🚀 **Hackathon-ready architecture**

---

## 👨‍💻 Built For

* 🏆 **Web3 Hackathons**
* 🏛️ **DAO Governance Projects**
* 🎓 **Student Blockchain Projects**
* 🌍 **Government Transparency Experiments**

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

* 🐛 **Report bugs**
* 💡 **Suggest features**
* 🔧 **Submit pull requests**
* ⭐ **Star the repository**

---

## Tech Stack:

- Solidity/Web3 (for writing/connecting the Blockchain contract)
- Next.js & Semantic UI React (front-end)
- MongoDB/ExpressJS/Node.js (back-end)
- IPFS (file storage for images)

## Screenshots of the app:

Homepage of the application:

![](screenshots/homepage.PNG)

Company registers/logs in:

![](screenshots/company_login.PNG)

Company creates an election if not created:

![](screenshots/create_election.PNG)

Dashboard on successful election creation:

![](screenshots/dashboard.PNG)

List of candidates for the election (here, you can add candidates):

![](screenshots/candidate_list.PNG)

Candidate has been notified on the mail:

![](screenshots/candidate_registeration_mail.PNG)

List of voters for the election (here, you can add voters):

![](screenshots/voterlist.PNG)

Voters have been sent their secure usernames and passwords on the mail:

![](screenshots/voter_registeration_mail.PNG)

Voter login page:

![](screenshots/voter_login.PNG)

Successful voting scenario:

![](screenshots/successful_voting.PNG)

Unsuccessful voting scenario:

![](screenshots/unsuccessful_voting.PNG)

Notification to each candidate and voter for the winner of candidates:

![](screenshots/winner_candidate_mail.PNG)


## 📄 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Yash Sawant**  
👨‍💻 Full-Stack Developer | Blockchain Enthusiast  
📧 yashsawant868@gmail.com  
🌐 GitHub: [https://github.com/sane-eagle](https://github.com/sane-eagle)
