# Link Shortener
Followed tutorial to create serverless Link Shortener here: [https://www.freecodecamp.org/news/how-to-build-a-serverless-app/](https://www.freecodecamp.org/news/how-to-build-a-serverless-app/)
- Deployed on Vercel (free JAM stack hosting site)
- Frontend: Next.js + TypeScript + Ant Design (components Library)
- NO MIDDLEWARE (though technically Next.js serverless functions are executed by Node.js)
- Backend: MongoDB

## Steps
- Create tsconfig.json file - `touch tsconfig.json`
- Install TypeScript - `npm install --save-dev typescript @types/react @types/node`
- Next.js detects & populates tsconfig.json
- Manually change index.js, _app.js, api/hello.js to TSX/TS files
- Install Ant Design components & Axios `npm install antd axios`
- Create UI inside `index.tsx` with component library and style with `Home.module.css`
- Initialize free MongoDB Atlas cloud database & add a user
- Copy-paste MongoDB URI into .env.local for Next.js to load env variables (.env file for reference)
- Install MongoDB package - `npm install mongodb`
- Create script `_connector.ts` to connect to Atlas
- Create script `shorten_link.ts` to shorten link and save link into database using `connector.ts`
- Add `vercel.json` to change redirect link to not include `/api/redirect` to `r/`
- Add MONGODB_URI secret through Vercel UI
- Make sure that the cluster has allowlisted connections from anywhere, since Vercel does not support static IP addresses

## NEXT Auto Generated
This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
