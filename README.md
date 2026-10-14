# Land-Registry-Management

Introduction
Land registry systems traditionally rely on centralized government databases to record property ownership, transactions, and mutations. These legacy frameworks are highly vulnerable to data tampering, single points of failure, and bureaucratic inefficiencies. Integrating blockchain technology replaces centralized record-keeping with a decentralized, immutable ledger, ensuring that land titles are securely archived and easily verifiable.
Problem Statement
Traditional land registry systems suffer from rampant fraud, including forged title deeds, illegal double-selling of properties, and unauthorized alterations of historical data. The heavy reliance on intermediaries (such as brokers and lawyers) increases transaction costs and introduces long delays. Furthermore, paper-based or siloed digital databases are highly susceptible to corruption, physical damage, and cyberattacks.
Objectives
•	Eliminate Fraud: Create an immutable, tamper-proof audit trail of land ownership.
•	Remove Intermediaries: Enable peer-to-peer property transfers to cut down costs and transaction delays.
•	Enhance Transparency: Provide a single, verifiable source of truth accessible to buyers, sellers, and government authorities.
•	Automate Processes: Streamline verification, title checks, and ownership transfers using automated scripts.
Blockchain Platform and Tools Used
•	Blockchain Platform: Ethereum or Hyperledger Fabric (Ethereum for public/permissionless testing; Hyperledger for enterprise/government permissioned access).
•	Smart Contracts: Solidity (to program ownership rules, transfer logic, and property details).
•	Development Environment: Hardhat or Truffle alongside Remix IDE for writing and debugging code.
•	Frontend Interface: React.js combined with Web3.js or Ethers.js to allow users to interact with the blockchain via a web browser.
•	Wallet Integration: MetaMask for user authentication and transaction signing.

System Architecture
The system follows a three-tier architecture model:
1.	Presentation Layer (Frontend): A user-friendly web interface where citizens view lands, and government admins verify registrations.
2.	Application/API Layer: Web3 libraries act as a bridge, translating user actions on the frontend into blockchain transactions.
3.	Blockchain Layer (Backend): A decentralized network execution environment where smart contracts manage state variables (like propertyOwner), and storage nodes permanently record every block of data.


Smart Contract Design
The smart contract contains data structures and functions to manage properties safely. Key components include:
•	Data Structures: A Property struct storing id, location, area, price, currentOwner, and isForSale status.
•	Mappings: A lookup table matching a unique propertyId to its corresponding Property data (mapping(uint256 => Property)).
•	Core Functions:
o	registerProperty(): Allows authorized government admins to add new land parcels to the blockchain.
o	listPropertyForSale(): Allows the verified owner to mark their land as available.
o	transferOwnership(): Automatically updates the ledger, transferring cryptocurrency to the seller and changing the currentOwner address to the buyer in a single transaction.
Screenshots and Outputs
•	Blockchain Land Registry Inventory
 

<img width="481" height="270" alt="image" src="https://github.com/user-attachments/assets/80ab5394-6e61-4d49-9f9a-d7075f665d46" />




•	Login page
<img width="489" height="275" alt="image" src="https://github.com/user-attachments/assets/862e032f-c5c4-4717-9950-9faca88c7315" />

 
•	Citizen Dashboard
<img width="499" height="281" alt="image" src="https://github.com/user-attachments/assets/d5e42d44-9df1-4f73-a05a-6441fe17f4cf" />

 
•	Surveyer Dashboard
<img width="504" height="283" alt="image" src="https://github.com/user-attachments/assets/77eef9a7-4269-402f-8bf4-cac3c3d998af" />

 
•	Land Marketplace
<img width="513" height="290" alt="image" src="https://github.com/user-attachments/assets/f035a676-9dc2-407c-8979-35e2f83ce45e" />

 
Conclusion
Implementing blockchain in land registry management revolutionizes property security and administrative workflow. By anchoring ownership data to a distributed ledger, the system replaces institutional trust with cryptographic verification. This drastically reduces land disputes, secures citizen assets, and significantly accelerates the property transfer pipeline.


Future Scope
•	IPFS Integration: Connect with the InterPlanetary File System (IPFS) to store heavy physical documents, maps, and blueprints decentralised, saving blockchain storage costs.
•	AI Valuation: Integrate Artificial Intelligence to evaluate land pricing dynamically based on local market trends before a listing goes live.
•	Biometric Identity: Link smart contract execution with biometric government IDs (like Aadhaar or digital passports) to enhance user authentication and prevent credential theft.
