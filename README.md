[Expedia Scraper](https://apify.com/getdataforme/Expedia-Scraper?fpr=data)

# Expedia Reviews Spider - Apify Actor

🕷️ **Automated web scraping actor for expedia**

## 📋 Overview

This Apify actor scrapes data from **expedia** using HTTP Request technology.
It was automatically generated and synchronized from the central repository.

## 🔗 Repository Information

| Property | Value |
| --- | --- |
| **Repository Name** | `expedia_reviews_spider_apify_hrequest` |
| **Spider Name** | `expedia_reviews_spider` |
| **Target Domain** | expedia |
| **Technology Type** | HTTP Request |
| **Template Used** | `apify_hrequest_template` |
| **Source Path** | `central_repo/src/custom/expedia/hrequest` |
| **GitHub Repository** | [View Repository](https://github.com/getdataforme/expedia_reviews_spider_apify_hrequest) |

## 🏠 Parent Repository

This actor is automatically synchronized from the central repository:

- **Central Repository**: [`getdataforme/central_repo`](https://github.com/getdataforme/central_repo)
- **Source Spider File**: `central_repo/src/custom/expedia/hrequest/expedia_reviews_spider.py`
- **Synchronization**: Automatic via GitHub Actions
- **Last Sync**: 2025-08-01 11:04:31 UTC

## 🔄 Development Workflow

### Making Changes

1. **DO NOT** edit files directly in this repository
2. Navigate to the [central repository](https://github.com/getdataforme/central_repo)
3. Edit the spider file at: `central_repo/src/custom/expedia/hrequest/expedia_reviews_spider.py`
4. Commit and push changes to the central repository
5. The GitHub Action will automatically sync changes to this repository

### Sync Process

- Changes to spider files trigger automatic synchronization
- The actor configuration and input schema are regenerated
- This README is updated with the latest information

## 📁 Repository Structure

```
├── src/
│   ├── main.py          # Apify actor entry point
│   └── spiders/
│       └── expedia_reviews_spider.py    # Spider implementation
├── .actor/
│   ├── actor.json       # Actor configuration
│   └── input_schema.json # Input parameters schema
├── requirements.txt     # Python dependencies
└── README.md           # This file
```

## 🚀 Usage

### Local Development

```
# Clone the repository
git clone https://github.com/getdataforme/expedia_reviews_spider_apify_hrequest.git
cd expedia_reviews_spider_apify_hrequest

# Install dependencies
pip install -r requirements.txt

# Run locally (if applicable)
python src/main.py
```

### Input Configuration

The actor accepts input parameters as defined in `.actor/input_schema.json`.
Common parameters may include:

- URLs to scrape
- Output format preferences
- Rate limiting settings
- Custom extraction parameters

## 🔗 Important Links

- 🏠 **[Central Repository](https://github.com/getdataforme/central_repo)** - Main development repository
- 📁 **[This Repository](https://github.com/getdataforme/expedia_reviews_spider_apify_hrequest)** - Generated Apify actor
- 🕷️ **[Source Spider](https://github.com/getdataforme/central_repo/blob/main/central_repo/src/custom/expedia/hrequest/expedia_reviews_spider.py)** - Original spider file
- 📚 **[Apify Documentation](https://docs.apify.com/)** - Apify platform documentation

## ⚠️ Important Notes

- **This repository is auto-generated** - Direct changes will be overwritten
- **All modifications** should be made in the central repository
- **Synchronization is automatic** - No manual intervention required
- **Issues and PRs** should be submitted to the central repository

---

*This README was automatically generated on 2025-08-01 11:04:31 UTC by the central repository sync process.*

## Apify Actor

This actor is published on [Apify](https://apify.com/).

### Actor Details

- **Actor Name**: expedia-reviews-spider-test
- **Organization**: See Apify Console
- **Console URL**: [https://console.apify.com/organization/3JrVZU8vEdLyeD4hC/actors/tLNVHf65UtYsrB7uy#/builds/0.0.1](https://console.apify.com/organization/3JrVZU8vEdLyeD4hC/actors/tLNVHf65UtYsrB7uy#/builds/0.0.1)

### Deployment

This actor is automatically deployed to Apify when changes are pushed to the `main` branch via GitHub Actions.

To run this actor:

1. Visit the Apify Console link above
2. Configure the input parameters
3. Click "Start" to run the actor