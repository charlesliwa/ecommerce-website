# Ecommerce Website

A modern, full-stack ecommerce website built with Next.js, Stripe, and TypeScript. Features a complete shopping experience with product browsing, shopping cart, and secure payment processing.

## Features

- 🛍️ **Product Catalog** - Browse products fetched from Stripe
- 🛒 **Shopping Cart** - Add, remove, and manage items with persistent cart state
- 💳 **Stripe Checkout** - Secure payment processing via Stripe
- 📱 **Responsive Design** - Mobile-first design with Tailwind CSS
- 🎨 **Modern UI** - Built with shadcn/ui components and Heroicons
- ⚡ **Server Components** - Optimized performance with Next.js App Router
- 💾 **Cart Persistence** - Cart state saved to localStorage using Zustand

## Tech Stack

- **Framework:** [Next.js 16](https://nextjs.org/) with App Router
- **Language:** [TypeScript](https://www.typescriptlang.org/)
- **Styling:** [Tailwind CSS v4](https://tailwindcss.com/)
- **UI Components:** [shadcn/ui](https://ui.shadcn.com/)
- **State Management:** [Zustand](https://zustand-demo.pmnd.rs/)
- **Payment Processing:** [Stripe](https://stripe.com/)
- **Icons:** [Heroicons](https://heroicons.com/)

## Getting Started

### Prerequisites

- Node.js 20 or higher
- npm, yarn, pnpm, or bun
- A Stripe account with API keys

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd ecommerce-website
```

2. Install dependencies:
```bash
npm install
# or
yarn install
# or
pnpm install
```

3. Set up environment variables:
Create a `.env.local` file in the root directory:
```env
STRIPE_SECRET_KEY=sk_test_your_stripe_secret_key
NEXT_PUBLIC_BASE_URL=http://localhost:3000
```

4. Run the development server:
```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Project Structure

```
ecommerce-website/
├── app/                    # Next.js App Router pages
│   ├── checkout/           # Checkout page and server action
│   ├── products/           # Product listing and detail pages
│   ├── success/            # Payment success page
│   ├── layout.tsx          # Root layout with navbar
│   └── page.tsx           # Home page
├── components/             # React components
│   ├── ui/                # shadcn/ui components
│   ├── carousel.tsx       # Product carousel
│   ├── navbar.tsx         # Navigation bar
│   ├── product-card.tsx   # Product card component
│   ├── product-detail.tsx # Product detail view
│   └── product-list.tsx   # Product listing grid
├── lib/                   # Utility libraries
│   ├── stripe.ts         # Stripe client configuration
│   └── utils.ts          # Utility functions
├── store/                 # State management
│   └── cart-store.ts     # Zustand cart store
└── public/               # Static assets
```

## Key Features

### Shopping Cart
- Add products to cart with quantity management
- Persistent cart state using Zustand with localStorage
- Real-time cart total calculation
- Remove items or adjust quantities

### Stripe Integration
- Fetch products from Stripe
- Create checkout sessions
- Handle payment success and cancellation
- Secure payment processing

### Responsive Navigation
- Mobile-friendly hamburger menu
- Cart icon with item count badge
- Smooth transitions and animations

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `STRIPE_SECRET_KEY` | Your Stripe secret key | Yes |
| `NEXT_PUBLIC_BASE_URL` | Base URL for your application | Yes (for production) |

## Deployment

### Deploy to Vercel

The easiest way to deploy is using [Vercel](https://vercel.com):

1. Push your code to GitHub
2. Import your repository on Vercel
3. Add your environment variables
4. Deploy!

### Other Platforms

This Next.js app can be deployed to any platform that supports Node.js:
- [Netlify](https://www.netlify.com/)
- [Railway](https://railway.app/)
- [Render](https://render.com/)
- Any Node.js hosting service

## Stripe Setup

1. Create a [Stripe account](https://stripe.com)
2. Get your API keys from the [Stripe Dashboard](https://dashboard.stripe.com/apikeys)
3. Add products in your Stripe Dashboard
4. Use test mode keys for development
5. Update your environment variables

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is private and proprietary.
