# 🔐 GenEscrow Frontend

**Live demo page for GenEscrow - AI-Powered Escrow with Real Payable Custody on GenLayer**

## 🌐 Live Demo

👉 [View Live Demo](https://hoveiser.github.io/genesrow-frontend/)

## 📋 About

This is the landing page for **GenEscrow**, a decentralized escrow smart contract on GenLayer that holds real GEN tokens (payable custody) and uses AI validators to adjudicate disputes between freelancers and clients.

## 🎯 Contract Details

- **Network:** GenLayer Testnet Bradbury (LIVE)
- **Contract Address:** `0xF2Dba0F446cc9D27156e516AaaBA46e7f48f28Ad`
- **Source Code:** [genesrow](https://github.com/hoveiser/genesrow)
- **Explorer:** [View on GenLayer Explorer](https://explorer-studio.genlayer.com/address/0xF2Dba0F446cc9D27156e516AaaBA46e7f48f28Ad)

## 🧪 What's Inside

The demo page showcases:
- How GenEscrow works (payable custody + AI adjudication)
- Four real test cases on Bradbury (happy path, AI approve, AI refund x2)
- Technical implementation details
- Links to GenLayer Studio and documentation

## 🚀 How to Use GenEscrow

1. Go to [GenLayer Studio](https://studio.genlayer.com)
2. Load the contract using address `0xF2Dba0F446cc9D27156e516AaaBA46e7f48f28Ad`
3. Call `create_escrow(freelancer, job_description, deliverable_url)` with GEN value
4. Test the full flow: `mark_delivered` → `dispute` → `resolve`
5. Watch AI validators adjudicate in real-time!

## 💡 Learn More

- **GenLayer Website:** https://genlayer.com
- **GenLayer Docs:** https://docs.genlayer.com
- **GenLayer Studio:** https://studio.genlayer.com

## License

MIT
