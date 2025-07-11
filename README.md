# ☀️ HeliosBot - Ultimate Discord Bot với SQLite

[![Discord.js](https://img.shields.io/badge/Discord.js-v14-blue)](https://discord.js.org/)
[![SQLite](https://img.shields.io/badge/SQLite-3-green)](https://www.sqlite.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-brightgreen)](https://nodejs.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

> ☀️ **The Ultimate Discord Bot** với SQLite Database, Crypto Exchange, Power 6/55 Jackpot, và nhiều tính năng siêu cool!

## ✨ Features Chính

### 🗄️ **SQLite Database System**

- ⚡ **Tốc độ cao** - Truy vấn ~1ms, không lag
- 🔒 **Bảo mật** - Local database, không phụ thuộc mạng
- 📁 **Dễ backup** - Chỉ cần copy file .db
- 🚀 **Ổn định** - Không có connection timeout
- 💿 **Nhẹ nhàng** - Không cần MongoDB server

### 💱 **Crypto Exchange System**

- 💰 **HLC Coin Trading** - Mua bán coin HLC với xu
- 📈 **Real-time Market** - Giá fluctuate theo thời gian thực
- 📊 **Portfolio Tracking** - Theo dõi danh mục đầu tư
- 🎯 **Trading History** - Lịch sử giao dịch chi tiết
- 💎 **Market Analytics** - Thống kê thị trường

### 💎 **Power 6/55 Jackpot System**

- 🎰 **Jackpot Tích Lũy** - Jackpot tăng từ những vé không trúng
- 🎫 **Multiple Tickets** - Mua 1-5 vé mỗi lần chơi
- 🏆 **Dual Jackpot** - Jackpot 1 (6 số) & Jackpot 2 (5 số + đặc biệt)
- 📊 **Player Stats** - Thống kê cá nhân chi tiết
- 💰 **Prize Structure** - Giải thưởng 100 xu/số trúng

### 💰 **Economy System**

- 🎁 **Daily Rewards** - Claim coins mỗi ngày với streak bonuses
- 📈 **XP & Level System** - Level up để unlock rewards
- 🏆 **Global Leaderboard** - Compete với users khác
- 💎 **Admin Commands** - Quản lý coins user
- 🔥 **Streak System** - Weekly milestones với extra bonuses

### 🎫 **Advanced Ticket System**

- 🎯 **Smart Routing** - Auto-detect ticket interactions
- 📋 **Guild Configs** - Tùy chỉnh theo từng server
- 🔧 **Admin Panel** - Quản lý tickets dễ dàng
- 📊 **Analytics** - Thống kê ticket usage

### 📰 **News & Announcement System**

- 📢 **Broadcast News** - Gửi thông báo tới toàn server
- 📋 **Templates** - Mẫu thông báo có sẵn
- 👥 **Subscription** - User tự đăng ký nhận tin
- 🎨 **Rich Embeds** - Thông báo đẹp với embed

### 🎮 **Fun & Games**

- 🎣 **Fishing System** - Câu cá kiếm coins
- 🐍 **Snake Game** - Game rắn săn mồi interactive
- 🌤️ **Weather Command** - Xem thời tiết real-time
- 🎲 **Random Games** - Nhiều mini-games khác

### 🔧 **Technical Excellence**

- 🔄 **Auto-Loading System** - Commands tự động load
- 🛡️ **Global Error Handler** - Xử lý lỗi toàn diện
- ⚡ **Performance Optimized** - SQLite WAL mode
- 🎛️ **Interaction System** - Button & dropdown support
- 📝 **Comprehensive Logging** - Log system chi tiết

## 🚀 Quick Start

### ⚡ Installation

```bash
# 1. Clone project
git clone https://github.com/hebi/heliosbot
cd heliosbot

# 2. Install dependencies
npm install

# 3. Setup SQLite database
npm run setup

# 4. Configure environment
cp .env.example .env
# Edit .env với Discord bot token

# 5. Start bot
npm start
```

### 🔧 Environment Setup

```env
# ========================================
# 🤖 HELIOSBOT CONFIGURATION (SQLite Edition)
# ========================================

# Discord Bot Token (Required)
DISCORD_TOKEN=your_discord_bot_token_here

# ========================================
# 🗄️ SQLITE DATABASE CONFIGURATION
# ========================================

# SQLite Database Path (local file - fast & reliable)
DATABASE_PATH=./data/heliosbot.db

# Database Backup Settings
BACKUP_PATH=./backups/
BACKUP_INTERVAL=24
BACKUP_RETENTION=30

# ========================================
# 🔐 ADMIN SETTINGS
# ========================================

# Bot Owner Discord ID (for admin commands)
OWNER_ID=your_discord_user_id_here
BOT_ADMIN_ID=your_discord_user_id_here

# ========================================
# 🎮 BOT CONFIGURATION
# ========================================

# Command prefix
BOT_PREFIX=h

# Starting balance for new users
STARTING_COINS=100

# Bot Status Message
BOT_STATUS=💱 Crypto Exchange | 💎 Power 6/55 | 🗄️ SQLite

# ========================================
# 💎 POWER 6/55 CONFIGURATION
# ========================================

# Jackpot Starting Amounts (in xu)
JACKPOT1_START=3000000
JACKPOT2_START=1000000

# Ticket Price
TICKET_PRICE=20

# ========================================
# 💱 CRYPTO EXCHANGE CONFIGURATION
# ========================================

# HLC Coin Settings
HLC_STARTING_PRICE=12.5
MARKET_UPDATE_INTERVAL=30

# ========================================
# 🌤️ WEATHER API
# ========================================

# AccuWeather API Key
ACCUWEATHER_API_KEY=your_accuweather_api_key
```

## 📖 Commands

### 💰 Economy Commands

| Command        | Aliases          | Description                              | Cooldown |
| -------------- | ---------------- | ---------------------------------------- | -------- |
| `hdaily`       | `hclaim`, `hd`   | Claim daily coin reward với streak bonus | 24 hours |
| `hbalance`     | `hbal`, `hcoins` | Xem coin balance, level, và user stats   | 3s       |
| `hleaderboard` | `hlb`, `htop`    | View top users by coins (paginated)      | 5s       |
| `haddcoins`    | -                | [Admin] Add coins to user                | -        |
| `hremovecoins` | -                | [Admin] Remove coins from user           | -        |
| `hsetcoins`    | -                | [Admin] Set user coins                   | -        |

### 💱 Crypto Exchange Commands

| Command            | Aliases                | Description                      | Cooldown |
| ------------------ | ---------------------- | -------------------------------- | -------- |
| `hcrypto-exchange` | `hcrypto`, `hexchange` | Mở Crypto Exchange trading panel | 5s       |

### 💎 Power 6/55 Commands

| Command       | Aliases             | Description                  | Cooldown |
| ------------- | ------------------- | ---------------------------- | -------- |
| `hpower-6-55` | `hp655`, `hjackpot` | Chơi Power 6/55 Jackpot game | 5s       |

### 🎮 Fun & Games

| Command    | Aliases    | Description             | Cooldown |
| ---------- | ---------- | ----------------------- | -------- |
| `hfish`    | `hfishing` | Câu cá để kiếm coins    | 30s      |
| `hsnake`   | -          | Chơi game rắn săn mồi   | 10s      |
| `hweather` | `hw`       | Xem thời tiết real-time | 5s       |

### 🔧 Utility Commands

| Command | Aliases           | Description                         | Cooldown |
| ------- | ----------------- | ----------------------------------- | -------- |
| `hhelp` | `hh`, `hcommands` | Show all commands với categories    | 3s       |
| `hping` | `hlatency`        | Check bot latency & database status | 2s       |

### 🎫 Ticket Commands

| Command   | Aliases | Description        | Cooldown |
| --------- | ------- | ------------------ | -------- |
| `hticket` | -       | Tạo support ticket | 5s       |

### 📰 News Commands

| Command | Aliases | Description            | Cooldown |
| ------- | ------- | ---------------------- | -------- |
| `hnews` | -       | News management system | 5s       |

## 🏗️ Project Structure

```
heliosbot/
├── index.js                    # Main bot file (SQLite integrated)
├── package.json                # Dependencies
├── .env                        # Configuration
├── README.md                   # This file
├── quick-setup.js              # Auto structure creation
├── database/                   # 🗄️ SQLite Database
│   └── sqliteDB.js            # Database class & methods
├── setup/                      # 🔧 Setup Scripts
│   └── setup-database.js      # Database initialization
├── migration/                  # 🔄 Migration Tools
│   └── mongodb-to-sqlite.js   # MongoDB to SQLite migration
├── data/                       # 📁 Database Files
│   └── heliosbot.db           # SQLite database file
├── backups/                    # 💾 Database Backups
├── logs/                       # 📝 Log Files
└── commands/                   # 🎮 Commands (Auto-loaded)
    ├── commandLoader.js        # Auto-loading system
    ├── economy/               # 💰 Economy commands
    │   ├── daily.js           # Daily rewards
    │   ├── balance.js         # Check balance
    │   ├── leaderboard.js     # Top users
    │   ├── addcoins.js        # [Admin] Add coins
    │   ├── removecoins.js     # [Admin] Remove coins
    │   └── setcoins.js        # [Admin] Set coins
    ├── crypto/                # 💱 Crypto Exchange
    │   └── crypto-exchange.js # Trading system
    ├── games/                 # 🎮 Games & Fun
    │   ├── power-6-55.js      # Jackpot game
    │   ├── fish.js            # Fishing
    │   └── snake.js           # Snake game
    ├── utility/               # 🔧 Utility commands
    │   ├── help.js            # Help system
    │   ├── ping.js            # Latency test
    │   └── weather.js         # Weather info
    ├── tickets/               # 🎫 Ticket System
    │   ├── ticket.js          # Ticket creation
    │   └── ticket-interactions.js # Ticket handlers
    ├── news/                  # 📰 News System
    │   └── news.js            # News management
    └── admin/                 # 👑 Admin commands
        └── eval.js            # Code execution
```

## 🎮 System Deep Dive

### 🗄️ SQLite Database Schema

**Tables:**

- `users` - User data, coins, stats, Power 6/55 records
- `guild_configs` - Server-specific configurations
- `tickets` - Support ticket system
- `power655_jackpot` - Jackpot amounts & stats
- `power655_history` - Jackpot win history
- `crypto_market` - HLC market data
- `crypto_portfolios` - User crypto holdings
- `trading_history` - Crypto trading records
- `news_subscriptions` - News subscription preferences
- `admin_actions` - Admin action logging

### 💎 Power 6/55 System

**Game Mechanics:**

- **Ticket Price**: 20 xu per ticket
- **Number Range**: 01-45 (pick 6 numbers)
- **Drawing**: 6 main numbers + 1 special number
- **Jackpot 1**: Match all 6 main numbers
- **Jackpot 2**: Match 5 main + special number
- **Regular Prizes**: 100 xu per matching number (min 3)

**Jackpot Accumulation:**

- 70% of ticket sales → Jackpot 1
- 20% of ticket sales → Jackpot 2
- 10% system fee

### 💱 Crypto Exchange System

**HLC Token:**

- **Starting Price**: 12.5 xu per HLC
- **Price Fluctuation**: Based on trading volume
- **Market Data**: 24h high/low, volume, market cap
- **Portfolio**: Track holdings, profit/loss
- **Trading**: Buy/sell with real-time pricing

### 🎁 Daily Rewards System

**Mechanics:**

- **Base Reward**: 50-100 coins
- **Streak Bonus**: +10 coins per consecutive day
- **Random Bonus**: 0-49 extra coins
- **XP Reward**: 50 XP per claim
- **Terms Agreement**: Required for first claim

## 🛠️ Development

### 🔄 Adding New Commands

```javascript
// commands/category/newcommand.js
module.exports = {
  name: "newcommand",
  description: "Description of command",
  category: "Category",
  aliases: ["alias1", "alias2"],
  cooldown: 5,
  usage: "newcommand [args]",

  async execute(message, args, { client, database, errorHandler }) {
    // Command logic with SQLite database
    const user = await database.getUser(message.author.id);

    // Your logic here
    await message.reply("Hello from SQLite!");

    // Save if needed
    await database.saveUser(user);
  },
};
```

### 🎛️ Adding Interactions

```javascript
// For button/dropdown interactions
module.exports.handleInteraction = async (
  interaction,
  { client, database, errorHandler }
) => {
  if (!interaction.isButton()) return;

  const customId = interaction.customId;

  if (customId === "my_button") {
    await interaction.reply("Button clicked!");
  }
};
```

### 🔧 Useful Scripts

```bash
npm start              # Production mode
npm run dev            # Development với nodemon
npm run setup          # Initialize SQLite database
npm run migrate        # Migrate from MongoDB to SQLite
npm run backup         # Backup database
npm run health         # Health check
npm run clean          # Clean temp files
```

## 🌐 Deployment

### 🚂 Railway (Recommended)

```bash
# Install Railway CLI
npm install -g @railway/cli

# Login & Deploy
railway login
railway init
railway up

# Set environment variables on Railway dashboard
```

### 🔋 VPS Deployment

```bash
# On your VPS
git clone https://github.com/hebi/heliosbot
cd heliosbot
npm install
npm run setup

# Configure .env
nano .env

# Use PM2 for process management
npm install -g pm2
pm2 start index.js --name "heliosbot"
pm2 startup
pm2 save
```

## 📊 Migration từ MongoDB

Nếu bạn có dữ liệu cũ trong MongoDB, sử dụng migration tool:

```bash
# 1. Đảm bảo MongoDB connection string trong .env
MONGO_URI=mongodb+srv://...

# 2. Chạy migration
npm run migrate

# 3. Xóa MONGO_URI khỏi .env (không còn cần)
```

## 🐛 Troubleshooting

### **"Cannot find module '../database/sqliteDB'"**

```bash
# Tạo cấu trúc files
node quick-setup.js
npm run setup
```

### **"SQLite3 not installed"**

```bash
npm install sqlite3
```

### **"Invalid Token"**

- ✅ Check Discord bot token trong `.env`
- ✅ Regenerate token nếu cần

### **"Database locked"**

- ✅ Đảm bảo chỉ có 1 instance bot chạy
- ✅ Restart bot nếu cần

### **Commands Not Working**

- ✅ Check prefix (default: `h`)
- ✅ Verify bot permissions
- ✅ Check command files

## 📈 Performance Benchmarks

**SQLite vs MongoDB:**

- ✅ **Query Speed**: ~1ms vs ~50-200ms
- ✅ **No Network Latency**: Local vs Cloud dependency
- ✅ **Reliability**: 99.99% vs 99.9% (network dependent)
- ✅ **Setup Complexity**: Minimal vs Moderate
- ✅ **Hosting Cost**: $0 vs $5-50/month

**System Requirements:**

- **RAM**: 50-100MB (vs 200-500MB with MongoDB)
- **Disk**: 10-50MB for database file
- **CPU**: Minimal usage
- **Network**: No database connection needed

## 🏆 Advanced Features

### 🔄 Auto-Loading System

- Commands tự động load từ thư mục
- Hot reload support
- Category-based organization
- Alias system

### 🛡️ Error Handling

- Global error catcher
- Comprehensive logging
- Auto-recovery mechanisms
- Admin notifications

### 📊 Analytics

- Command usage tracking
- User activity monitoring
- Performance metrics
- Database health checks

## 📞 Support

- 📧 **GitHub Issues**: [Create an issue](https://github.com/hebi/heliosbot/issues)
- 💬 **Discord Server**: [Join support server](https://discord.gg/heliosbot)
- 📖 **Documentation**: Check this comprehensive README
- 🎥 **Video Tutorials**: [YouTube Channel](https://youtube.com/@hebi)

## 🔗 Links

- 🌐 **Demo Bot**: [Invite HeliosBot](https://discord.com/oauth2/authorize?client_id=YOUR_BOT_ID)
- 📚 **Discord.js Guide**: [Official Documentation](https://discordjs.guide/)
- 🗄️ **SQLite Documentation**: [SQLite.org](https://www.sqlite.org/)
- 🎮 **Command Examples**: [Wiki](https://github.com/hebi/heliosbot/wiki)

## 🎉 Credits

- ☀️ **HeliosBot** - Created with ❤️ by hebi
- ⚡ **Discord.js** - For amazing Discord API wrapper
- 🗄️ **SQLite** - For fast & reliable local database
- 🎨 **ASCII Art** - For epic terminal aesthetics
- 🎮 **Community** - For feedback and suggestions

## 📜 License

MIT License - feel free to modify and distribute!

## 🚀 What's Next?

**Planned Features:**

- 🎯 **Gambling System** - Blackjack, slots, roulette
- 🏪 **Shop System** - Buy items with coins
- 🎭 **Role Rewards** - Special roles for achievements
- 📱 **Mobile Dashboard** - Web interface for management
- 🤖 **AI Integration** - Smart responses and recommendations
- 🌍 **Multi-language** - Support multiple languages

---

<div align="center">

**☀️ HeliosBot - Shining bright in Discord with SQLite power! ☀️**

[![Star this repo](https://img.shields.io/github/stars/hebi/heliosbot?style=social)](https://github.com/hebi2222/heliosbot.git)
[![Follow me](https://img.shields.io/github/followers/hebi?style=social)](https://github.com/hebi2222)

Made with 💎, ☀️ and lots of ☕ by **hebi**

**🗄️ Powered by SQLite - Fast, Reliable, Zero Dependencies! 🚀**

</div>Follow meơ(https://img.shields.io/github/followers/hebi?style=social)](https://github.com/hebi2222)

Made with 💎 and lots of ☕ by **hebi**

</div>
