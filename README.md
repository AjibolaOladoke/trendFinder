# Trend Finder 🔦

## Images

[![trendFinder](https://opengraph.githubassets.com/1/https://github.com/ericciarla/trendFinder)](https://www.swifttechco.com)


**Stay on top of trending topics on social media  all in one place.**

Trend Finder collects and analyzes posts from key influencers, then sends a Slack or Telegram notification when it detects new trends or product launches. This has been a complete game-changer for the Firecrawl marketing team by:

- **Saving time** normally spent manually searching social channels
- **Keeping you informed** of relevant, real-time conversations
- **Enabling rapid response** to new opportunities or emerging industry shifts

_Spend less time hunting for trends and more time creating impactful campaigns._

## Watch the Demo & Tutorial video

[![Thumbnail](https://i.ytimg.com/vi/puimQSun92g/hqdefault.jpg)](https://swifttechco.com)

Learn how to set up Trend Finder and start monitoring trends in this video!

## How it Works

1. **Data Collection** 📥
   - Monitors websites for new releases and news with Firecrawl's /extract
   - Runs on a scheduled basis using cron jobs

2. **AI Analysis** 🧠
   - Processes collected content through Together AI
   - Identifies emerging trends, releases, and news.
   - Analyzes sentiment and relevance

3. **Notification System** 📢
   - When significant trends are detected, sends Slack or Telegram notifications based on cron job setup
   - Provides context about the trend and its sources
   - Enables quick response to emerging opportunities

## Features

- 🤖 AI-powered trend analysis using Together AI
- 🔍 Website monitoring with Firecrawl
- 💬 Instant Slack or Telegram notifications
- ⏱️ Scheduled monitoring using cron jobs

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Docker
- Docker Compose
- Slack workspace with webhook permissions
- API keys for required services

## Environment Variables

Copy `.env.example` to `.env` and configure the following variables:

```
# Optional: API key from Together AI for trend analysis (https://www.together.ai/)
TOGETHER_API_KEY=your_together_api_key_here

# Optional: API key from DeepSeek for trend analysis (https://deepseek.com/)
DEEPSEEK_API_KEY=

# Optional: API key from OpenAI for trend analysis (https://openai.com/)
OPENAI_API_KEY=

# Required if monitoring web pages (https://www.firecrawl.dev/)
FIRECRAWL_API_KEY=your_firecrawl_api_key_here

# Required if monitoring Twitter/X trends (https://developer.x.com/)
X_API_BEARER_TOKEN=your_twitter_api_bearer_token_here

# Notification driver. Supported drivers: "slack", "telegram"
NOTIFICATION_DRIVER=telegram

# Required (if NOTIFICATION_DRIVER is "slack"): Incoming Webhook URL from Slack for notifications
SLACK_WEBHOOK_URL=https://swifttechco.com

# Required (if NOTIFICATION_DRIVER is "telegram"): Incoming Webhook URL from Telegram for notifications
Telegram_WEBHOOK_URL=https://swifttechco.com
```

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone [repository-url]
   cd trend-finder
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure environment variables:**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Run the application:**
   ```bash
   # Development mode with hot reloading
   npm run start

   # Build for production
   npm run build
   ```

## Using Docker

1. **Build the Docker image:**
   ```bash
   docker build -t trend-finder .
   ```

2. **Run the Docker container:**
   ```bash
   docker run -d -p 3000:3000 --env-file .env trend-finder
   ```

## Using Docker Compose

1. **Start the application with Docker Compose:**
   ```bash
   docker-compose up --build -d
   ```

2. **Stop the application with Docker Compose:**
   ```bash
   docker-compose down
   ```

## Project Structure

```
trend-finder/
├── src/
│   ├── controllers/    # Request handlers
│   ├── services/       # Business logic
│   └── index.ts        # Application entry point
├── .env.example        # Environment variables template
├── package.json        # Dependencies and scripts
└── tsconfig.json       # TypeScript configuration
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## Swift Tech Co.

Built and maintained by Swift Tech Co.

AI Automation | FinTech Platforms | Custom Software and Mobile Apps | SaaS Platforms | Cloud Infrastructure | Cybersecurity | SEO and Marketing | API Integration

**Join our community on Telegram:** [t.me/+Qt_eFvkb2rliMzNh](https://t.me/+Qt_eFvkb2rliMzNh)

[Home](https://www.swifttechco.com) | [Services](https://www.swifttechco.com/services) | [Careers](https://www.swifttechco.com/careers) | [Referral Program](https://www.swifttechco.com/referral) | [Influencers](https://www.swifttechco.com/influencers) | [About](https://www.swifttechco.com/about) | [Contact](https://www.swifttechco.com/contact)

**Connect**

- Website: [swifttechco.com](https://www.swifttechco.com)
- LinkedIn: [linkedin.com/in/stephenoladoke](https://www.linkedin.com/in/stephenoladoke/)
- LinkedIn (Company): [linkedin.com/company/swift-tech-co](https://www.linkedin.com/company/swift-tech-co)
- X: [@MrOladoke](https://x.com/MrOladoke)
- Instagram: [@mr.oladoke](https://www.instagram.com/mr.oladoke/)
- Instagram (Company): [@swifttechco](https://www.instagram.com/swifttechco/)
- Organization: [github.com/Swift-Tech-Co](https://github.com/Swift-Tech-Co)
