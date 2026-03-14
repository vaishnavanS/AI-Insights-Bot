# AI-Insights-Bot

Hey! This is a project I built to solve a personal problem: I wanted a way to stay updated on the **2026 Tamil Nadu Elections** and **Generative AI** trends without constantly checking news sites or getting lost in social media. 

Instead of just getting a link that I'd never click, this bot scrapes the actual article content and sends a summary directly to my WhatsApp.

## Why I Built This
Being an engineering student, I'm always looking for ways to automate my information flow. I started with a simple News API, but realized the data wasn't "fresh" enough for local TN politics. I pivoted to an RSS-based scraper that visits real news sites, pulls the body text, and cleans up the HTML so it looks perfect on a phone screen.

## How it Works
1. **Search:** It monitors specific Google News RSS feeds for "Tamil Nadu election" and "Generative AI."
2. **Unmask:** Google News uses redirect links, so the bot "unmasks" them to find the original source.
3. **Scrape:** It uses `newspaper4k` to visit the site and pull the actual article body.
4. **Deliver:** The content is cleaned of messy HTML tags and sent via Twilio to WhatsApp.

## Technical Setup
* **Language:** Python 3.10+
* **The "Engine":** `feedparser` for RSS and `newspaper4k` for full-text extraction.
* **The "Courier":** Twilio API for the WhatsApp integration.
* **The "Fixes":** Used `urllib.parse` to handle URL encoding and regex to strip out annoying HTML tags.

##  Get it Running
If you want to try it out, you'll need a [Twilio](https://www.twilio.com/) account.

1. **Clone the repo:**
   ```bash
   git clone [https://github.com/vaishnavanS/AI-Insights-Bot.git](https://github.com/vaishnavanS/AI-Insights-Bot.git)
