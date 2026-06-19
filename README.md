# Morning Alpha

An open-source AI agent that automatically collects market news, earnings reports, and company updates to generate daily investment research reports.

Instead of spending hours reading financial news, earnings releases, and analyst opinions, Morning Alpha continuously monitors the market and delivers a structured research report every morning.

---

## Features

### Market Intelligence Collection

* Collects the latest market news
* Tracks earnings reports and company updates
* Monitors multiple information sources
* Consolidates data into a single research pipeline

### AI-Powered Analysis

* Summarizes key developments
* Identifies positive and negative signals
* Extracts major investment risks
* Generates structured research notes

### Bull / Neutral / Bear Signal Engine

Automatically classifies market sentiment based on:

* News momentum
* Earnings trends
* Revenue growth
* Profitability changes
* Market reactions

Output example:

```text
Signal: Bull

Confidence: 82%

Positive Factors:
- Revenue growth accelerating
- Strong earnings surprise
- Improving market sentiment

Risk Factors:
- Elevated valuation
- Slowing macro environment
```

### Historical Comparison

Compare current conditions with the previous 30 days:

* News sentiment trend
* Earnings revisions
* Signal changes
* Key market events

### Automated Delivery

Research reports can be delivered through:

* Notion
* Slack
* Email

### Daily Scheduling

Run automatically every morning at 7:00 AM.

---

## Architecture

```text
Scheduler (7 AM)
        │
        ▼
News Collection
        │
        ▼
Earnings Collection
        │
        ▼
AI Analysis
        │
        ▼
30-Day Comparison
        │
        ▼
Bull / Neutral / Bear Signal
        │
        ▼
Notion Storage
        │
        ├──► Slack Notification
        │
        └──► Email Delivery
```

---

## Tech Stack

* Python
* OpenAI API
* Notion API
* Slack API
* SMTP Email
* RSS Feeds
* Docker
* GitHub Actions

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourname/morning-alpha.git

cd morning-alpha
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create environment variables:

```bash
cp .env.example .env
```

Fill in your credentials:

```env
OPENAI_API_KEY=

NOTION_TOKEN=
NOTION_DATABASE_ID=

SLACK_WEBHOOK_URL=

SMTP_HOST=
SMTP_PORT=
SMTP_USERNAME=
SMTP_PASSWORD=
EMAIL_RECIPIENT=
```

---

## Usage

Run manually:

```bash
python main.py
```

Run with Docker:

```bash
docker compose up
```

---

## Example Report

```text
Company: NVIDIA

Signal: Bull

Confidence: 86%

Summary:
Revenue growth exceeded expectations.
Demand for AI infrastructure remains strong.

Positive Factors:
- Strong earnings beat
- Data center expansion
- Positive analyst revisions

Risk Factors:
- Premium valuation
- Increased competition

Action Items:
- Review valuation metrics
- Monitor next earnings release
```

---

## Scheduling

### Linux Cron

```bash
0 7 * * * python /app/main.py
```

### GitHub Actions

Run automatically every morning without maintaining your own server.

Example workflow is available in:

```text
.github/workflows/daily_report.yml
```

---

## Roadmap

### Version 1

* News collection
* Earnings tracking
* AI analysis
* Notion integration

### Version 2

* Multi-company watchlists
* Sector-level analysis
* Portfolio monitoring

### Version 3

* AI investment copilot
* Interactive dashboard
* Real-time alerts

---

## Disclaimer

This project is for research and educational purposes only.

The generated reports do not constitute investment advice, financial advice, trading advice, or recommendations to buy or sell any securities.

Always perform your own due diligence before making investment decisions.

---

## Contributing

Contributions are welcome.

If you would like to improve the project:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

Bug reports, feature requests, and documentation improvements are highly appreciated.

---

## License

MIT License

Copyright (c) 2026

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software.
