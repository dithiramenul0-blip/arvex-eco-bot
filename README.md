# ArveX Bot™ - Professional Discord Bot

> Enterprise-grade Discord bot for ArveX Hosting™ built with Discord.js v14 and MongoDB

## 🌟 Features

### Core Systems
- ✅ **Economy System** - Daily rewards, work, crime, bank, shop, trading
- ✅ **Quest System** - Daily, weekly, monthly, special quests with achievements
- ✅ **Leveling System** - XP tracking, voice XP, rank cards, prestige
- ✅ **Hosting Rewards** - Free VPS, Minecraft servers, web hosting claims
- ✅ **Moderation** - Ban, kick, mute, timeout, warn, anti-spam, anti-raid
- ✅ **Ticket System** - Button-based tickets with transcripts
- ✅ **Giveaway System** - Create, end, reroll giveaways
- ✅ **Referral System** - Invite tracking with fake invite detection
- ✅ **Hosting Tycoon** - Virtual hosting company system
- ✅ **Utility Commands** - AFK, polls, suggestions, reminders, calculator

### Technical Features
- 🔒 Advanced error handling & anti-crash protection
- 🗄️ MongoDB database integration
- ⚡ Slash commands + Prefix commands
- 🎯 Event handler system
- 📦 Modular command architecture
- 🔐 Permission system with role-based access
- ⏱️ Cooldown system
- 📊 Webhook logging
- 🎨 Professional embed templates
- 🚀 Production-ready code

## 📋 Prerequisites

- Node.js 18+ (Latest LTS recommended)
- MongoDB Atlas account (Free tier works)
- Discord Bot Token
- 2GB RAM minimum for production

## 🚀 Installation

### 1. Clone Repository
```bash
git clone https://github.com/dithiramenul0-blip/arvex-eco-bot.git
cd arvex-eco-bot
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure Environment
```bash
cp .env.example .env
# Edit .env with your credentials
```

### 4. Setup Discord Bot
- Go to [Discord Developer Portal](https://discord.com/developers/applications)
- Create new application
- Go to Bot section and create bot
- Copy token to `.env`
- Enable Intents:
  - Message Content Intent
  - Guild Members Intent
  - Presence Intent
- Set permissions (Administrator for development)

### 5. Setup MongoDB
- Create account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
- Create cluster
- Copy connection string to `.env`

### 6. Start Bot
```bash
# Development
npm run dev

# Production
npm start
```

## 📁 Project Structure

```
arvex-eco-bot/
├── src/
│   ├── index.js                 # Main bot entry point
│   ├── config/
│   │   └── config.js           # Configuration management
│   ├── commands/
│   │   ├── economy/            # Economy commands
│   │   ├── quests/             # Quest commands
│   │   ├── leveling/           # Leveling commands
│   │   ├── moderation/         # Moderation commands
│   │   ├── utility/            # Utility commands
│   │   └── admin/              # Admin commands
│   ├── events/
│   │   ├── ready.js            # Bot ready event
│   │   ├── messageCreate.js    # Message handling
│   │   ├── interactionCreate.js # Slash command handling
│   │   └── guildMemberAdd.js   # Member join event
│   ├── handlers/
│   │   ├── commandHandler.js   # Command loader
│   │   ├── eventHandler.js     # Event loader
│   │   └── cooldownHandler.js  # Cooldown manager
│   ├── models/
│   │   ├── User.js             # User schema
│   │   ├── Guild.js            # Guild schema
│   │   ├── Economy.js          # Economy schema
│   │   ├── Quest.js            # Quest schema
│   │   └── Ticket.js           # Ticket schema
│   ├── utils/
│   │   ├── logger.js           # Logging utility
│   │   ├── embed.js            # Embed templates
│   │   ├── errorHandler.js     # Error handling
│   │   ├── validators.js       # Input validation
│   │   └── helpers.js          # Helper functions
│   ├── database/
│   │   └── connection.js       # MongoDB connection
│   └── constants/
│       ├── colors.js           # Color constants
│       ├── emojis.js           # Emoji constants
│       └── messages.js         # Message templates
├── .env.example
├── .gitignore
├── package.json
├── ecosystem.config.js         # PM2 configuration
└── README.md
```

## 🛠️ Available Commands

### Economy
- `ax!balance` - Check your balance
- `ax!daily` - Claim daily reward
- `ax!work` - Work for coins
- `ax!crime` - Attempt a crime
- `ax!transfer <user> <amount>` - Transfer coins
- `ax!shop` - View shop items
- `ax!buy <item>` - Purchase item
- `ax!inventory` - View your inventory

### Leveling
- `ax!rank` - View your rank card
- `ax!leaderboard` - Global leaderboard
- `ax!prestige` - Prestige your account

### Moderation
- `ax!ban <user> [reason]` - Ban user
- `ax!kick <user> [reason]` - Kick user
- `ax!mute <user> <duration> [reason]` - Mute user
- `ax!warn <user> [reason]` - Warn user
- `ax!purge <amount>` - Delete messages

### Tickets
- `ax!ticket create` - Create support ticket
- `ax!ticket close` - Close ticket
- `ax!ticket claim` - Claim ticket

### Admin
- `ax!reload` - Reload commands
- `ax!ping` - Check bot latency
- `ax!stats` - View bot statistics

## 🔐 Security Features

- Input validation and sanitization
- Rate limiting per user
- Permission-based access control
- Encrypted sensitive data
- Environment variable protection
- SQL injection prevention
- XSS protection
- CSRF tokens for API

## 📊 Performance

- Optimized database queries
- Caching system for frequently accessed data
- Event-driven architecture
- Minimal memory footprint
- Auto-scaling ready

## 🐛 Error Handling

- Comprehensive error catching
- Detailed error logging
- User-friendly error messages
- Automatic error recovery
- Webhook error notifications

## 📝 Logging

Logs are stored in `logs/` directory with:
- Bot activity logs
- Error logs
- Command usage logs
- Database operation logs

## 🚀 Deployment

### VPS Deployment (Recommended)
1. Install Node.js 18+
2. Clone repository
3. Setup `.env` with production credentials
4. Install PM2: `npm install -g pm2`
5. Start with PM2: `pm2 start ecosystem.config.js`

### Docker Deployment
```bash
docker build -t arvex-bot .
docker run -d --env-file .env arvex-bot
```

## 📄 License

MIT License - See LICENSE file

## 👥 Support

For support, join our [Discord Server](https://discord.gg/arvex)

## 🔄 Updates

Regularly updated with new features and improvements. 

---

**ArveX Bot™** © 2024 ArveX Development Team. All rights reserved.
