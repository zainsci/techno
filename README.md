# Techno

A comprehensive Discord bot built with TypeScript, providing essential features for small communities.

## Technical Stack

- **Runtime:** Node.js
- **Language:** TypeScript
- **Library:** [discord.js](https://discord.js.org/) (v14+)
- **ORM:** [Prisma](https://www.prisma.io/)
- **Database:** SQLite

## Getting Started

### Prerequisites

- Node.js (v18.x or higher)
- A Discord Bot Token (Get one at the [Discord Developer Portal](https://discord.com/developers/applications))

### Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the root directory and add your bot token:
   ```env
   DISCORD_TOKEN=your_token_here
   ```

### Database Setup

Initialize the SQLite database using Prisma:
```bash
npx prisma generate
npx prisma db push
```

### Running the Bot

Start the bot in development mode:
```bash
npm run dev
```

## Core Features

### Welcome System
- Automatic welcome messages for new members
- Customizable welcome channel
- Optional role assignment for new members

### Configuration & Tools
- `/settings` - Configure bot settings
- `/announce` - Make server announcements
- `/suggestion` - Create suggestion system
- `/help` - Show available commands

### Moderation
- `/kick` - Kick members from the server
- `/ban` - Ban members from the server
- `/clear` - Delete multiple messages at once
- `/warn` - Warn members for rule violations
- `/mute` - Temporarily mute members

### Information
- `/ping` - Check bot's latency
- `/serverinfo` - Display server information
- `/userinfo` - Display user information

### Fun & Games
- `/poll` - Create simple polls
- `/8ball` - Ask the magic 8ball a question
- `/roll` - Roll a dice
- `/flip` - Flip a coin
- `/joke` - Tell a random joke
- `/meme` - Share a random meme

### Safety
- Link filtering
- Bad word filtering

### Role Management
- `/role` - Assign/remove roles
- Role hierarchy management
- Temporary role assignments
- Role-based permissions

### Music (Coming Soon)
- `/play` - Play music from YouTube
- `/skip` - Skip current song
- `/queue` - Show music queue
- `/stop` - Stop playing music
