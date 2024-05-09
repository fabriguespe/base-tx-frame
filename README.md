# XMTP Base Frame

This is a Farcaster and XMTP Frame starter made with [Next.js](https://nextjs.org/) following the [frames.js OpenFrames](https://framesjs.org/middleware/openframes) standard, working on Base mainnet.

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

Click on Debug to open the frames.js debugger, sign in with farcaster or with wallet to try XMTP openframes.

You can start editing the frame by modifying `app/transaction/route.tsx`.

The files in the `/app/api` folder `/app/api/mint/route.ts`, `app/api/send/route.ts`, `app/api/swap/complete/route.ts` e `app/api/swap/approval/route.ts` handle the logic for the completion of the mint, send, swap and swap approval transactions.

After a transaction is made, the user is redirected to the frame `app/transaction/transaction-result/route.tsx`, which shows the status (if the transactionReceipt is available).

Under the hood, this project uses the following libraries:
- [Enso Finance](https://enso.finance) for the swap transaction
- [Zora ZDK](https://docs.zora.co/docs/zora-api/zdk) to retrieve the NFT metadata for the mint transaction
- [Viem](https://viem.sh) for everything else