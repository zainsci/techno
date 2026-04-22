# Gemini Context: Techno

Techno is a comprehensive Discord bot designed for small communities, providing utility, moderation, and engagement features.

## Project Overview
- **Type:** Discord Bot (Node.js/TypeScript)
- **Framework:** `discord.js` (v14+)
- **ORM:** Prisma (v6+) with SQLite
- **Runtime:** `tsx` for direct TypeScript execution

### Key Features
- **Moderation:** Role assignment/removal, member kicks/bans, and message clearing.
- **Engagement:** Welcome messages, polls, and fun commands (8ball, roll, flip, jokes, memes).
- **Utility:** Server/User information, help system, and ping latency checks.
- **Automation:** Automatic welcome embeds for new members.

## Building and Running

### Prerequisites
- Node.js and npm installed.
- A Discord Bot Token from the [Discord Developer Portal](https://discord.com/developers/applications).

### Environment Setup
Create a `.env` file in the root directory:
```env
DISCORD_TOKEN=your_bot_token_here
```

### Installation
```bash
npm install
```

### Database Initialization
```bash
npx prisma generate
npx prisma db push
```

### Running the Bot
```bash
# Development mode with auto-reload
npm run dev
```

## Development Conventions

### Architecture
- **Entry Point:** `index.ts` contains the bot initialization, command registration, and event handlers.
- **Database:** Prisma is used for data persistence. The schema is located in `prisma/schema.prisma`.
- **Commands:** Uses Discord Slash Commands. New commands should be added to the `commands` array in `index.ts` and handled in the `InteractionCreate` event.

### Code Style
- Uses ES Modules (`"type": "module"` in `package.json`).
- TypeScript is used for type safety.
- `dotenv` is used for configuration management.

### Adding New Features
1. **Define Command:** Add the `SlashCommandBuilder` definition to the `commands` array in `index.ts`.
2. **Handle Interaction:** Add a new `case` to the `switch (commandName)` block in the `InteractionCreate` listener.
3. **Database Changes:** If needed, update `prisma/schema.prisma` and run `npx prisma db push`.
