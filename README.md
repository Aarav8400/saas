This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

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

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

````md
# Clerk Setup with Next.js

## Introduction

Clerk ek user authentication aur management service hai jo aapki website mein secure sign-in, sign-up aur user profiles add karna aasan banaati hai. Is README mein hum Clerk ko Next.js app ke sath kaise setup karte hain, wo step-by-step samjhaenge.

## Installation

### 1. Next.js Project Create karo

Pehle ek Next.js project banao agar tumhare paas nahi hai:

```bash
npx create-next-app my-app
cd my-app
```
````

### 2. Clerk SDK Install karo

Clerk ke liye Next.js SDK install karo:

```bash
npm install @clerk/nextjs
```

## Clerk Account Setup

1. Clerk ke official website [Clerk.com](https://clerk.com) pe jao aur apna account banao.
2. Naya project create karo. Tumhe **Frontend API** mil jaayega jo agle step mein chahiye hoga.

## Configuration

1. Apne Next.js project mein ek `.env.local` file banao aur isme Clerk ke environment variables add karo:

```env
NEXT_PUBLIC_CLERK_FRONTEND_API=your-clerk-frontend-api
CLERK_API_KEY=your-clerk-api-key
```

2. Ab apne `pages/_app.js` ya `pages/_app.tsx` file mein ClerkProvider ko import karo:

```js
import { ClerkProvider } from "@clerk/nextjs";

function MyApp({ Component, pageProps }) {
  return (
    <ClerkProvider>
      <Component {...pageProps} />
    </ClerkProvider>
  );
}

export default MyApp;
```

## Add Sign-in and Sign-up

1. Clerk ke pre-built sign-in aur sign-up components ko Next.js app mein integrate karo.

**pages/sign-in.js**:

```js
import { SignIn } from "@clerk/nextjs";

export default function SignInPage() {
  return <SignIn />;
}
```

**pages/sign-up.js**:

```js
import { SignUp } from "@clerk/nextjs";

export default function SignUpPage() {
  return <SignUp />;
}
```

2. Ab tum `/sign-in` aur `/sign-up` URLs ko access karke Clerk ke authentication pages dekh sakte ho.

## User Profile

Agar tum user profile manage karna chahte ho, toh Clerk ka `<UserProfile />` component use kar sakte ho.

**pages/user-profile.js**:

```js
import { UserProfile } from "@clerk/nextjs";

export default function UserProfilePage() {
  return <UserProfile />;
}
```

## Example Usage

Clerk ke components ko Next.js app mein use karke, tum sign-up, sign-in, aur user profile ko easily manage kar sakte ho. Clerk tumhare liye sab security aur authentication handle karega.

## Run the Project

```bash
npm run dev
```

Isse tumhara app local environment mein chal jayega. Tum apna Clerk integration dekh sakte ho `/sign-in`, `/sign-up`, aur `/user-profile` pages par.

```

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.


```
