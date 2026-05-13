# Audience Analytics Dashboard
**MSIT 5910 Capstone Project — University of the People**

A centralized, web-based analytics solution designed for a mid-sized media organization operating across radio, television, and online publication channels.

## Project Overview
This system consolidates audience data from three previously disconnected platforms:
- Broadcast ratings (Radio & TV)
- Website analytics (Google Analytics)
- Social media metrics (Meta Business Suite)

## Repository Structure

```
audience-analytics-dashboard/
├── README.md                    ← this file
├── /docs
│   ├── technical_report.pdf     ← full system documentation
│   ├── ethics_statement.pdf     ← GDPR & data privacy notes
│   └── functional_requirements.pdf
├── /design
│   ├── architecture_diagram.png ← layered architecture visual
│   └── dashboard_wireframes.pdf ← UI mockups
└── /config
    ├── data_sources_config.md   ← connector settings (read-only)
    └── sample_data/
        ├── broadcast_performance.csv
        ├── web_analytics.csv
        └── social_media_engagement.csv
```

## Branches
- **main** — stable, reviewed configuration (production)
- **development** — active work and testing before merging

## Data Sources
| Source | Platform | Connector Type | Access Level |
|--------|----------|---------------|--------------|
| Web Traffic | Google Analytics | API (read-only) | Field whitelisted |
| Social Media | Meta Business Suite | API (read-only) | Field whitelisted |
| Broadcast | Radio/TV software | CSV upload | Manual refresh |

## Key Metrics (KPIs)
1. Total weekly reach (all platforms combined)
2. Platform engagement rate
3. Top-performing content piece
4. Primary traffic source
5. Audience demographic breakdown

## Security Notes
- All API connectors use **read-only** access tokens
- Credentials stored as environment variables (never hardcoded)
- GDPR Article 5 data minimization: only required fields are pulled
- OWASP access control enforced at the integration layer
