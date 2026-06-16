[Expedia Scraper](https://apify.com/memo23/expedia-scraper?fpr=data)

# Expedia.com Hotel Reviews Scraper

**Unlock the Full Power of Expedia.com Hotel Review Data** - The only scraper you need to track, analyze, and understand hotel reviews on Expedia.com with enterprise-grade reliability and precision. Whether you're monitoring hotel reputation, analyzing customer feedback, or conducting hospitality research, our scraper delivers comprehensive, real-time insights while saving you time and resources.

*"From guest reviews to travel insights, we turn Expedia.com's data into your competitive advantage."*

## Overview

The Expedia.com Hotel Reviews Scraper is your go-to tool for extracting hotel review data from Expedia.com and Hotels.com. Ideal for hotel managers, market analysts, travel agencies, and researchers, it tracks review details, ratings, guest feedback, management responses, and hotel-level aggregate scores across hotels worldwide. With easy setup and multiple export formats (JSON, CSV), it's perfect for anyone looking to gather comprehensive hotel review data from Expedia.com.

## What does Expedia.com Hotel Reviews Scraper do?

The Expedia.com Hotel Reviews Scraper is a powerful tool that enables you to:

### Comprehensive Data Collection

- **Review Data**

- Extract complete review text and titles
- Scrape ratings and review scores (e.g., "8/10 Good")
- Capture review rating labels, verification status, and stay month
- Gather guest names and reviewer information
- Analyze review dates and temporal trends
- Track sentiment analysis (liked/disliked features)
- Extract hotel management responses when available
- **Guest Insights**

- Extract trip type information (e.g., "Stayed 1 night in Feb 2025")
- Capture normalized travel companion details (e.g., "Traveled with family", "Traveled with partner")
- Identify traveler types (business traveler, leisure traveler)
- Download review photos when available
- Access guest feedback on specific amenities
- **Hotel-Level Aggregate Data**

- Extract hotel overall rating (e.g., `8.2`)
- Extract hotel rating label (e.g., `"Very good"`)
- Extract hotel total review count
- Extract hotel category ratings such as cleanliness, location, and staff & service

### Advanced Scraping Capabilities

- **Pagination Handling**: Automatically navigates through all review pages
- **Date Filtering**: Filter reviews by date range (get only recent reviews)
- **Efficient Processing**: Processes reviews with duplicate detection
- **Smart Pagination**: Stops automatically when reaching older reviews (date filter optimization)
- **Incremental Data Collection**: Build comprehensive review datasets over time

### Flexible Scraping Options

- **Hotel Review Pages**: Extract all reviews for specific hotels

- Expedia UK: `https://www.expedia.co.uk/Kastoria-Hotels-Hotel-Anastassiou.h6136437.Hotel-Information`
- Expedia US: `https://www.expedia.com/New-York-Hotels-Hotel-Name.h123456.Hotel-Information`
- Expedia short hotel path (no slug): `https://www.expedia.com/h17369936.Hotel-Information`
- Expedia Brazil: `https://www.expedia.com.br/Rio-De-Janeiro-Hotels-Premier-Copacabana-Hotel.h53296.Hotel-Information`
- Expedia Germany: `https://www.expedia.de/Berlin-Hotels-Hotel-Name.h123456.Hotel-Information`
- Hotels.com: `https://el.hotels.com/ho434012/hotel-anastassiou-kastoria-ellada/`
- **Expedia Deeplinks**: `https://expe.app.link/KjB1EuacRSb` (automatically resolved to hotel page)

This tool is ideal for:

- Hotel reputation management and monitoring
- Guest satisfaction analysis and sentiment tracking
- Competitive intelligence for hospitality businesses
- Building comprehensive review databases for market research
- Tracking rating trends and customer feedback over time

## Features

- **Comprehensive Data Extraction**: Detailed review information, ratings, guest feedback, and sentiment analysis
- **Hotel Aggregate Review Metrics**: Overall hotel score, rating label, total review count, and category ratings
- **Management Responses**: Capture hotel replies to guest reviews when available
- **Multiple Platform Support**:

- **Expedia.com**: All major Expedia domains (US, UK, Brazil, Germany, France, Spain, Italy, Netherlands, Japan, Australia, and more)
- **Hotels.com**: Full support for Hotels.com reviews
- **Flexible Input**: Supports multiple input formats:

- Direct hotel URLs (long slug or short `.../h{propertyId}.Hotel-Information`)
- Expedia deeplinks (expe.app.link) - automatically resolved
- Multiple hotels in a single run
- **Date Filtering**: Filter reviews by date (from specific date until now)
- **Optional Category Ratings Toggle**: Control whether hotel-level aggregate fields are requested
- **Automatic Pagination**: Handles multi-page reviews automatically
- **Efficient Processing**: Concurrent scraping with configurable concurrency settings
- **Reliable Performance**: Built-in retry mechanisms and proxy support
- **Structured Data Export**: Download review data in JSON or CSV format for analysis

## Supported Platforms

The Expedia.com Hotel Reviews Scraper can extract data from:

1. **Expedia.com** - Hotels on all Expedia domains

- Example: `https://www.expedia.co.uk/Kastoria-Hotels-Hotel-Anastassiou.h6136437.Hotel-Information`
- Example: `https://www.expedia.com/New-York-Hotels-Hotel-Name.h123456.Hotel-Information`
- Example (short URL): `https://www.expedia.com/h17369936.Hotel-Information`
- Example: `https://www.expedia.com.br/Rio-De-Janeiro-Hotels-Premier-Copacabana-Hotel.h53296.Hotel-Information`
- Example: `https://www.expedia.de/Berlin-Hotels-Hotel-Name.h123456.Hotel-Information`
- Fields: `reviewText`, `reviewRating`, `reviewRatingLabel`, `verified`, `hotelOverallRating`, `hotelTotalReviews`, `hotelCategoryRatings`, `hotelResponse`, `tripType`, `traveledWith`, `sentiments`, etc.
2. **Hotels.com** - All Hotels.com hotel pages

- Example: `https://el.hotels.com/ho434012/hotel-anastassiou-kastoria-ellada/`
- Fields: Same comprehensive review data as Expedia.com

Each platform has the same unified data structure, making it easy to analyze reviews across both Expedia and Hotels.com properties.

## Quick Start

1. **Sign up for Apify**: Create your free account at [apify.com](https://apify.com/).
2. **Find the Scraper**: Search for "Expedia.com Hotel Reviews Scraper" in the Apify Store.
3. **Configure Input**: Set up your scraping parameters using the input schema.
4. **Run the Scraper**: Execute the scraper on the Apify platform.
5. **Data Collection**: The scraper will output all available review data.

## Input Configuration

Here's an example of how to set up the input for the Expedia.com Hotel Reviews Scraper:

```
{
    "startUrls": [
        "https://www.expedia.co.uk/Kastoria-Hotels-Hotel-Anastassiou.h6136437.Hotel-Information",
        "https://www.expedia.com/New-York-Hotels-Hotel-Name.h123456.Hotel-Information",
        "https://www.expedia.com/h17369936.Hotel-Information",
        "https://www.expedia.com.br/Rio-De-Janeiro-Hotels-Premier-Copacabana-Hotel.h53296.Hotel-Information",
        "https://el.hotels.com/ho434012/hotel-anastassiou-kastoria-ellada/",
        "https://expe.app.link/KjB1EuacRSb"
    ],
    "reviewsFrom": "2025-01-01",
    "includeCategoryRatings": true,
    "maxItems": 1000,
    "maxConcurrency": 10,
    "minConcurrency": 1,
    "maxRequestRetries": 100,
    "proxy": {
        "useApifyProxy": true
    }
}
```

### Input Fields Explanation

- `startUrls`: Array of hotel URLs to scrape reviews from:

- Expedia URL: `"https://www.expedia.co.uk/Kastoria-Hotels-Hotel-Anastassiou.h6136437.Hotel-Information"`
- Hotels.com URL: `"https://el.hotels.com/ho434012/hotel-anastassiou-kastoria-ellada/"`
- Expedia Deeplink: `"https://expe.app.link/KjB1EuacRSb"` (automatically resolved)
- `reviewsFrom`: Filter reviews from this date until now (optional). Format: `YYYY-MM-DD` (e.g., `"2025-01-01"`)

- Only scrapes reviews posted on or after this date
- Uses smart pagination stopping to optimize performance
- Leave empty to get all reviews
- `includeCategoryRatings`: Fetch hotel-level aggregate fields such as `hotelOverallRating`, `hotelRatingLabel`, `hotelTotalReviews`, and `hotelCategoryRatings` (default: `true`)

- When enabled, the actor emits one additional Apify charge event: `additional-cost`
- Set to `false` if you only need review-level output
- `maxItems`: Maximum number of reviews to scrape (default: 1000).
- `maxConcurrency`: Maximum number of pages processed simultaneously (default: 10).
- `minConcurrency`: Minimum number of pages processed simultaneously (default: 1).
- `maxRequestRetries`: Number of retries for failed requests (default: 100).
- `proxy`: Proxy settings for enhanced scraping reliability.

- `useApifyProxy`: Use Apify's proxy service (recommended: `true`)

## Pricing Note

- `includeCategoryRatings` is enabled by default because most users want hotel-level benchmark fields
- When `includeCategoryRatings` is enabled, the actor sends one additional Apify charging event per run: `additional-cost`
- If you do not need hotel-level aggregate data, set `includeCategoryRatings` to `false`

## Date Filtering Feature

The `reviewsFrom` parameter allows you to filter reviews by date, making it perfect for:

- **Recent reviews**: Get only the latest feedback
- **After renovation**: Track reviews since hotel improvements
- **Monitoring**: Get new reviews since last check
- **Seasonal analysis**: Analyze reviews for specific time periods

## Deeplink URL Support

The scraper automatically handles Expedia deeplink URLs (`expe.app.link`), which are commonly used in:

- **Mobile sharing**: Hotel links shared from Expedia mobile app
- **Marketing campaigns**: Promotional deeplinks
- **Social media**: Shortened URLs from social platforms
- **Email campaigns**: Tracking links in email marketing

### How It Works

1. Scraper detects deeplink URL format (`https://expe.app.link/...`)
2. Automatically follows redirects to resolve the final hotel page
3. Extracts hotel ID from the resolved URL
4. Scrapes reviews normally

**Example:**

```
{
    "startUrls": [
        "https://expe.app.link/KjB1EuacRSb"
    ]
}
```

The deeplink resolves to:

```
https://www.expedia.com/Winter-Park-Hotels-Winter-Park-Mountain-Lodge.h5507.Hotel-Information
```

And the scraper extracts reviews for hotel ID `5507`.

## Output Structure

The scraper provides comprehensive information about hotel reviews from Expedia.com and Hotels.com. The output includes detailed review text, ratings, guest information, trip details, sentiment analysis, and review metadata. Here's a breakdown of the main components:

### Sample JSON Output

```
{
    "placeName": "Kastoria Hotels Hotel Anastassiou",
    "placeAddress": "",
    "provider": "expedia",
    "hotelId": "6136437",
    "hotelUrl": "https://www.expedia.co.uk/Kastoria-Hotels-Hotel-Anastassiou.h6136437.Hotel-Information",
    "locale": "en_GB",
    "verified": true,
    "hotelOverallRating": 8,
    "hotelRatingLabel": "Very good",
    "hotelTotalReviews": 69,
    "hotelCategoryRatings": [
        { "label": "Cleanliness", "percent": 84 },
        { "label": "Location", "percent": 82 },
        { "label": "Staff & service", "percent": 86 }
    ],
    "reviewId": "67bf52814570c67eb5d18a8b",
    "reviewText": "Nice simple stay.",
    "reviewTitle": "",
    "reviewDate": "2025-03-13T00:00:00.000Z",
    "stayDate": "2025-02-01T00:00:00.000Z",
    "reviewRating": 8,
    "reviewRatingLabel": "Good",
    "rating": "8/10 Good",
    "authorName": "Jeffrey",
    "reviewerName": "Jeffrey",
    "tripType": "Stayed 1 night in Feb 2025",
    "stayDuration": 1,
    "traveledWith": "Traveled with family",
    "liked": [
        "cleanliness",
        "staff & service"
    ],
    "disliked": [],
    "sentiments": [
        "Liked: cleanliness, staff & service"
    ],
    "photos": [],
    "hotelResponse": "Thank you very much for your rating.We hope to see you again soon.Have a great time.",
    "hotelResponseAuthor": "Anastassiou hotel",
    "hotelResponseDate": "2025-04-08T00:00:00.000Z",
    "page": 0,
    "scrapedAt": "2026-02-05T13:11:47.005Z"
}
```

### Output Fields Detailed Explanation

#### Hotel Information

- **`placeName`** (string): Hotel name extracted from URL. Example: `"Kastoria Hotels Hotel Anastassiou"`
- **`placeAddress`** (string): Hotel address (currently empty in API responses)
- **`provider`** (string): Platform source - either `"expedia"` or `"hotels"`
- **`hotelId`** (string): Unique hotel identifier. Example: `"6136437"`
- **`hotelUrl`** (string): Direct link to the hotel page on Expedia/Hotels.com
- **`locale`** (string): Locale derived from the source domain or input URL. Examples: `"en_US"`, `"pt_BR"`, `"de_DE"`
- **`verified`** (boolean): Whether the review is marked as verified by the source site
- **`hotelOverallRating`** (number | null): Hotel overall score on a 0-10 scale. Example: `8.2`
- **`hotelRatingLabel`** (string | null): Hotel rating label. Examples: `"Very good"`, `"Muito boa"`
- **`hotelTotalReviews`** (number | null): Total number of hotel reviews shown by Expedia/Hotels.com
- **`hotelCategoryRatings`** (array | null): Hotel category breakdown with normalized labels and integer percentages. Example: `[{ "label": "Cleanliness", "percent": 84 }]`

#### Review Content

- **`reviewId`** (string): Unique review identifier for duplicate detection. Example: `"67bf52814570c67eb5d18a8b"`
- **`reviewText`** (string): Guest's detailed feedback. Example: `"Nice simple stay."`
- **`reviewTitle`** (string): Review headline (often empty)

#### Rating Information

- **`reviewDate`** (string): Review post date in ISO 8601 format. Example: `"2025-03-12T23:00:00.000Z"`
- **`stayDate`** (string | null): Stay month in ISO 8601 format derived from the trip summary. Example: `"2025-02-01T00:00:00.000Z"`
- **`reviewRating`** (number): Numeric score (0-10 scale). Example: `8`
- **`reviewRatingLabel`** (string | null): Human-readable review label. Examples: `"Good"`, `"Excellent"`, `"Excelente"`
- **`rating`** (string): Full rating with descriptor. Example: `"8/10 Good"`

#### Guest Information

- **`authorName`** (string): Guest's name or display name. Example: `"Jeffrey"`
- **`reviewerName`** (string): Same as authorName (for compatibility)

#### Trip Details

- **`tripType`** (string): Stay duration and timing. Example: `"Stayed 1 night in Feb 2025"`
- **`stayDuration`** (number | null): Number of nights in the stay. Example: `1`
- **`traveledWith`** (string | null): Normalized travel companion info. Examples: `"Traveled with family"`, `"Traveled with partner"`, `"Solo traveler"`, `"Business traveler"` (null if not specified)

#### Sentiment Analysis

- **`liked`** (array of strings): Parsed liked topics from the sentiment labels
- **`disliked`** (array of strings): Parsed disliked topics from the sentiment labels
- **`sentiments`** (array of strings): Guest-liked/disliked features. Example: `["Liked: cleanliness, staff & service"]` or `["Disliked: noise, outdated facilities"]`

#### Media

- **`photos`** (array of strings): Guest-uploaded photo URLs (often empty)

#### Management Response

- **`hotelResponse`** (string | null): Hotel management response text when the property replied to the review
- **`hotelResponseAuthor`** (string | null): Response author extracted from the Expedia/Hotels.com response heading
- **`hotelResponseDate`** (string | null): Response date in ISO 8601 format

#### Metadata

- **`page`** (number): Pagination page number (zero-indexed). Example: `0`
- **`scrapedAt`** (string): Scrape timestamp in ISO 8601 format. Example: `"2026-02-05T13:11:47.005Z"`

## Use Cases

### 1. Hotel Reputation Management

Monitor and analyze guest reviews to understand hotel performance and identify areas for improvement.

```
{
    "startUrls": ["https://www.expedia.com/MyHotel.h123456.Hotel-Information"],
    "reviewsFrom": "2025-01-01",
    "maxItems": 1000
}
```

### 2. Competitive Analysis

Compare reviews across multiple hotels to benchmark performance against competitors.

```
{
    "startUrls": [
        "https://www.expedia.com/Hotel-A.h111111.Hotel-Information",
        "https://www.expedia.com/Hotel-B.h222222.Hotel-Information",
        "https://www.expedia.com/Hotel-C.h333333.Hotel-Information"
    ],
    "includeCategoryRatings": true,
    "maxItems": 5000
}
```

### 3. Market Research

Analyze review trends across locations or time periods for hospitality market insights.

```
{
    "startUrls": [
        "https://www.expedia.com/New-York-Hotel.h123456.Hotel-Information",
        "https://www.expedia.com/London-Hotel.h234567.Hotel-Information"
    ],
    "reviewsFrom": "2024-01-01",
    "maxItems": 10000
}
```

### 4. Sentiment Analysis

Extract and analyze guest sentiments to understand what guests like and dislike.

```
{
    "startUrls": ["https://www.expedia.co.uk/Kastoria-Hotels-Hotel-Anastassiou.h6136437.Hotel-Information"],
    "maxItems": 2000
}
```

## Performance & Limits

- **Rate Limiting**: The scraper includes built-in delays and retry mechanisms
- **Concurrency**: Adjust `maxConcurrency` based on your needs (1-20 recommended)
- **Memory**: Each review is approximately 1-2 KB in JSON format
- **Speed**: Typically processes 100-200 reviews per minute (depends on hotel and settings)
- **Date Filter Optimization**: Using `reviewsFrom` can reduce scraping time by 50-80% for recent reviews

## Error Handling

The scraper includes comprehensive error handling:

- **Automatic Retries**: Failed requests are retried up to `maxRequestRetries` times
- **Duplicate Detection**: Reviews are deduplicated by `reviewId`
- **Proxy Support**: Use Apify proxy to avoid blocks
- **Smart Pagination**: Stops automatically when reaching end of reviews
- **Graceful Failures**: Continues scraping even if individual pages fail

## Troubleshooting

### No Reviews Found

- Check if the hotel URL is correct
- Verify the hotel has reviews on Expedia/Hotels.com
- Try running without `reviewsFrom` filter first
- If you disabled `includeCategoryRatings`, hotel-level fields such as `hotelOverallRating` and `hotelCategoryRatings` will be `null`

### Scraper Stops Early

- Check `reviewsFrom` date - scraper stops when all reviews are older
- Verify `maxItems` isn't too low
- Check logs for error messages

### Duplicate Reviews

- The scraper automatically handles duplicates using `reviewId`
- Duplicates are logged but not added to output
- Normal behavior when re-scraping the same hotel

## Support & Contact

For custom solutions, bulk scraping, or support:

- 📧 Email: [muhameddidovic@gmail.com](mailto:muhameddidovic@gmail.com)
- 🏪 Apify Store: Search for "Expedia.com Hotel Reviews Scraper"
- 💬 Apify Support: Contact through Apify platform

## Explore More Scrapers

If you found this Apify Scraper useful, be sure to check out our other powerful scrapers and actors at [memo23's Apify profile](https://apify.com/memo23). We offer a wide range of tools to enhance your web scraping and automation needs across various platforms and use cases.

## Legal & Ethical Use

- This scraper is intended for legitimate business purposes only
- Respect Expedia.com and Hotels.com Terms of Service
- Use responsibly and ethically
- Do not overload servers with excessive requests
- Consider using data for analysis and research within legal boundaries

---

**Built with ❤️ by Muhammad Didovic**

*Last Updated: March 2026*