### **2. vitalzk-sdk (The Developer Glue)**

> **Simple TypeScript and Rust interfaces for the VitalZK protocol.**

 

#### **Project Description**

The VitalZK SDK provides high-level functions for hospitals to issue credentials and for third-party apps to verify them. It abstracts away the complexity of Soroban RPC calls and ZK-proof serialization.

**Key Features:**

  * **Credential Signing:** Standardized methods for hospitals to sign medical JSON-LD.
  * **Proof Wrapper:** Prepares ZK-proofs for submission to the `vitalzk-contracts`.
  * **Stellar Integration:** Built-in support for `stellar-sdk` and `freighter-api`.

#### **Folder Structure**

```text
vitalzk-sdk/
├── src/
│   ├── node/            # Node.js specific logic (Issuers)
│   ├── browser/         # Browser/Client logic (Verifiers)
│   └── common/          # Shared types and constants
├── examples/            # Quick-start integration scripts
└── package.json
```

#### **Installation**

```bash
npm install @vitalzk/sdk
```

#### **Usage**

```typescript
import { VitalZK } from '@vitalzk/sdk';

// Initialize verifier
const vzk = new VitalZK('testnet');
const isValid = await vzk.verify(userProof, hospitalPublicKey);
```
