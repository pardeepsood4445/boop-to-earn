# 🐶 Boop To Earn - Farcaster Mini App

**Boop it. Earn it. Built on Arbitrum.**  
A Farcaster Mini App that lets users "boop" to claim $BOOP tokens from a smart contract on Arbitrum One. The app tracks total boops, total users, and total tokens distributed—all within the standard Farcaster web mini app layout.

## 🌐 Live Mini App

Access the live version directly from Warpcast or visit:  
👉 https://boop-to-earn.vercel.app

---

## ⚙️ Features

- ✅ One-click **Boop** (via Farcaster in-app wallet)
- 📊 Real-time stats:
  - Total Boops
  - Total Unique Users
  - Boop Distributed
- 📦 Built with:
  - `wagmi` + `viem`
  - `@farcaster/miniapp-wagmi-connector`
  - `@farcaster/miniapp-sdk`
  - Hosted via Vercel
- 🟦 Arbitrum One (L2) support
- 🖼️ Optimized for Farcaster Mini App frame size (390px width)

---

## 📁 Project Structure

```
/
├── public/
│   ├── doglogo.png          # Main boop image
│   └── contract.json        # Contract address + ABI
├── index.html               # Main mini app UI and logic
├── vercel.json              # Optional: Vercel config
└── README.md                # You're reading this!
```

---

## 📝 Setup Instructions

1. **Clone this repo**
   ```bash
   git clone https://github.com/yourusername/boop-to-earn.git
   cd boop-to-earn
   ```

2. **Add your smart contract config**
   Update `/public/contract.json`:
   ```json
   {
     "address": "0xeF828e04005c1280F7c35C8AA00b1084C71f61B9",
     "abi": [ ... ]
   }
   ```

3. **Deploy to Vercel**
   Either use Vercel CLI:
   ```bash
   vercel deploy --prod
   ```
   Or deploy via [Vercel dashboard](https://vercel.com/).

---

## 🧠 Developer Notes

- Uses `farcasterMiniApp()` as wallet connector
- `writeContract()` calls the `boop()` function (no ETH required)
- Auto-fetches:
  - `totalBoops()`
  - `totalUniqueUsers()`
  - `totalTokensDistributed()`

---

## 📜 License

MIT License

---

## ✨ Credits

Built by [@pratiksharma.eth](https://warpcast.com/pratiksharma.eth)  
Inspired by dogs, memes, and good vibes.
