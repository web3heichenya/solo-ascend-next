# Solo Ascend - Web3 Hero NFT Gaming Platform

A Next.js-based Web3 gaming platform featuring NFT heroes, forging mechanics, and token-bound accounts (TBA). Built with modern web technologies and blockchain integration.

## 🎮 Features

- **NFT Hero System**: Mint and manage unique hero NFTs with different classes and attributes
- **Forging Mechanics**: Upgrade heroes through a forging system with oracle integration
- **Token-Bound Accounts (TBA)**: Advanced NFT functionality with account abstraction
- **3D Visualizations**: Interactive 3D effects using Three.js and React Three Fiber
- **Multi-language Support**: Internationalization with i18next
- **Web3 Integration**: Full wallet connectivity via RainbowKit and Wagmi
- **Responsive Design**: Mobile-first approach with Tailwind CSS

## 🚀 Tech Stack

- **Framework**: Next.js 15.4 with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS v4 with custom cyber theme
- **3D Graphics**: Three.js, React Three Fiber, Drei
- **Web3**:
  - RainbowKit for wallet connection
  - Wagmi for Ethereum interactions
  - Viem for low-level blockchain operations
- **State Management**: Zustand
- **UI Components**: Radix UI, Shadcn/ui components
- **Internationalization**: i18next, react-i18next
- **Data Fetching**: TanStack Query (React Query)

## 📦 Installation

### Prerequisites

- Node.js 18+
- pnpm (recommended) or npm/yarn
- MetaMask or other Web3 wallet

### Setup

1. Clone the repository:

```bash
git clone [repository-url]
cd solo-ascend/next
```

2. Install dependencies:

```bash
pnpm install
# or
npm install
```

3. Create environment variables:

```bash
cp .env.example .env.local
```

4. Configure your environment variables:

```env
NEXT_PUBLIC_ALCHEMY_API_KEY=your_alchemy_api_key
NEXT_PUBLIC_WALLET_CONNECT_PROJECT_ID=your_walletconnect_project_id
# Add other required environment variables
```

5. Run the development server:

```bash
pnpm dev
# or
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the application.

## 📝 Available Scripts

```bash
# Development
pnpm dev              # Start development server with Turbopack
pnpm build            # Build for production
pnpm start            # Start production server

# Code Quality
pnpm lint             # Run ESLint
pnpm lint:fix         # Run ESLint with auto-fix
pnpm format           # Format code with Prettier
pnpm format:check     # Check code formatting
pnpm type-check       # Run TypeScript type checking

# Maintenance
pnpm clean            # Clean build cache and node_modules cache
```

## 🏗️ Project Structure

```
src/
├── app/                 # Next.js app router pages
│   ├── page.tsx        # Home page
│   ├── faq/            # FAQ page
│   └── layout.tsx      # Root layout
├── components/         # React components
│   ├── effects/        # 3D effects and animations
│   ├── forge/          # Forging system components
│   ├── hero/           # Hero NFT components
│   ├── layout/         # Layout components
│   ├── tba/            # Token-bound account components
│   ├── ui/             # Reusable UI components
│   └── wallet/         # Wallet connection components
├── hooks/              # Custom React hooks
├── lib/                # Utility libraries
│   ├── contracts/      # Smart contract ABIs and interfaces
│   ├── providers.tsx   # App providers setup
│   └── store.ts        # Zustand store configuration
├── styles/             # Global styles
└── types/              # TypeScript type definitions
```

## 🎨 Key Components

### Hero System

- **HeroDisplay**: Main hero viewing and interaction interface
- **HeroMintCard**: NFT minting functionality
- **HeroDetailsCard**: Display hero attributes and stats
- **HeroSearchModal**: Search and filter heroes

### Forging System

- **ForgeItemCard**: Individual forge item display
- **ForgeOracleModal**: Oracle integration for forging
- **PendingForgeButton**: Track pending forge operations

### Web3 Integration

- **WalletConnect**: RainbowKit wallet connection
- **TBAAssetsModal**: Token-bound account asset management
- **InventoryModal**: User inventory management

## 🔧 Configuration

### Tailwind Configuration

The project uses Tailwind CSS v4 with custom cyber-themed styling. Configuration can be found in `tailwind.config.js`.

### TypeScript Configuration

TypeScript is configured with strict mode enabled. See `tsconfig.json` for details.

### ESLint & Prettier

Code quality is maintained with ESLint and Prettier. Configuration files:

- `.eslintrc.json` - ESLint rules
- `.prettierrc` - Prettier formatting rules

## 🌐 Internationalization

The app supports multiple languages using i18next. Language files are located in the `public/locales` directory.

Supported languages:

- English (en)
- Additional languages can be added by creating new translation files

## 🔗 Blockchain Integration

### Smart Contracts

The application interacts with custom smart contracts for:

- Hero NFT minting and management
- Forging mechanics
- Token-bound accounts

Contract ABIs are located in `src/lib/contracts/abis/`.

### Network Support

- Ethereum Mainnet
- Polygon
- Other EVM-compatible chains (configurable)

## 🚢 Deployment

### Production Build

```bash
pnpm build
pnpm start
```

### Vercel Deployment

The easiest way to deploy is using [Vercel](https://vercel.com):

1. Push your code to GitHub
2. Import your repository to Vercel
3. Configure environment variables
4. Deploy

### Docker Support

```dockerfile
# Dockerfile example (if applicable)
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN pnpm install
COPY . .
RUN pnpm build
EXPOSE 3000
CMD ["pnpm", "start"]
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is proprietary software. All rights reserved.

## 🔗 Links

<div align="center">

[![Visit Solo Ascend](https://img.shields.io/badge/🎮%20Visit-Solo%20Ascend-blue?style=for-the-badge&logo=gaming&logoColor=white)](https://solo-ascend.vercel.app/) [![Follow on Twitter](https://img.shields.io/badge/🐦%20Follow-@web3heichen-blue?style=for-the-badge&logo=twitter&logoColor=white)](https://x.com/web3heichen)

</div>

## 💡 Troubleshooting

### Common Issues

1. **Wallet Connection Issues**
   - Ensure MetaMask is installed and unlocked
   - Check you're on the correct network
   - Clear browser cache if connection persists

2. **Build Errors**
   - Run `pnpm clean` to clear caches
   - Delete `node_modules` and reinstall dependencies
   - Ensure all environment variables are set

3. **Transaction Failures**
   - Check gas settings
   - Verify contract addresses
   - Ensure sufficient balance for gas fees

For more help, check the FAQ page in the application or reach out to the community.
