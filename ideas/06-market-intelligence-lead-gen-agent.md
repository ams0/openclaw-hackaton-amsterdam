# Idea 6: Market Intelligence & Lead Generation Agent

## Overview
Build an OpenClaw-powered research agent that continuously scrapes the web, monitors competitors, aggregates news, and qualifies sales leads — delivering daily intelligence reports directly to a team's Slack or WhatsApp channel.

## Problem It Solves
Sales and marketing teams spend hours manually researching prospects, tracking competitor moves, and reading industry news. OpenClaw can automate this entire research loop locally, without paying for expensive SaaS tools.

## Core Features
- **Competitor Monitor**: Track competitor websites, pricing pages, and job boards for changes; alert the team when something noteworthy happens.
- **News Digest**: Aggregate RSS feeds and web sources on configurable topics and deliver a morning briefing.
- **Lead Qualifier**: Given a list of company names or LinkedIn URLs, OpenClaw scrapes publicly available data and scores each lead against an ideal-customer-profile (ICP) rubric.
- **LinkedIn Outreach Drafter**: "Draft a personalised cold message to the VP of Engineering at Acme Corp" → researches the target and composes a message.
- **Conference & Event Tracker**: Scrape event sites for relevant upcoming conferences and extract speaker and sponsor lists as potential leads.

## Tech Stack
- OpenClaw web-scraping skill (Playwright or requests + BeautifulSoup)
- RSS parser
- Local LLM for summarisation, scoring, and drafting
- Slack / WhatsApp integration
- SQLite for lead database storage

## Stretch Goals
- CRM integration (HubSpot, Salesforce) to push qualified leads automatically
- Automated A/B testing of outreach message styles
- Keyword alerting: notify immediately if a competitor announces a new product

## Why It's Great for a Hackathon
Broad appeal across business functions, easy to demo with real company names, and produces tangible output (a lead score report or a news digest) that judges can evaluate immediately.
