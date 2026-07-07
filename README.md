[Artsy Scraper](https://apify.com/parseforge/artsy-scraper?fpr=data)

![ParseForge Banner](https://images.apifyusercontent.com/RHzPvdHJ2joNXJHSWjeziGDTOTaycOsfmbNq9q8ZVRM/w:1800/cb:1/aHR0cHM6Ly9yYXcuZ2l0aHVidXNlcmNvbnRlbnQuY29tL1BhcnNlRm9yZ2UvYXBpZnktYXNzZXRzL21haW4vYmFubmVyLmpwZw.webp)

# 🎨 Artsy Scraper - Artworks, Artists & Shows

> 🚀 Scrape artworks, artists, and gallery shows from Artsy. Get titles, prices, dimensions, provenance, images, and availability. Search by keyword and filter by for-sale status or show type.

> 🕒 Last updated: 2026-04-16

Collect art market data from Artsy without coding. Scrape artworks with prices, dimensions, medium, provenance, and high-resolution images. Extract artist profiles with biographies and artwork counts. Collect gallery show details with dates, locations, and partner information. Search by keyword and filter by availability or show status.

Whether you are a collector tracking artwork prices, a gallery building a digital catalog, a researcher studying art market trends, or an appraiser comparing similar pieces, this tool delivers structured data from one of the world's largest online art marketplaces.

| Target | Artsy - online art marketplace and gallery platform |
| --- | --- |
| Use Cases | Art market research, price tracking, collection management, gallery monitoring, art investment analysis |

---

## 📋 What it does

- 🖼️ Extracts artwork titles, artist names, dates, medium, category, and dimensions (inches and centimeters) for every piece
- 💰 Collects list prices, price ranges, sale messages, and auction status to track market values
- 📸 Returns primary images and full image galleries with width, height, and aspect ratio metadata
- 👤 Scrapes artist profiles with nationality, biography, birth/death dates, gender, and artwork counts
- 🏛️ Collects gallery show information including exhibition names, dates, locations, partner names, and artwork counts
- ✅ Includes availability status, for-sale flags, condition descriptions, and certificates of authenticity

The scraper operates in three modes: artworks, artists, and shows. Each mode returns a specialized set of fields. Artwork records include 25+ fields with pricing, dimensions, and provenance details.

💡 **Why it matters**: The art market is notoriously opaque. Prices, availability, and provenance information are scattered across gallery websites and marketplaces. This scraper centralizes that data into structured records you can analyze in spreadsheets or databases.

---

## 🎬 Full Demo

🚧 Coming soon

---

## ⚙️ Input

| Field | Type | Description |
| --- | --- | --- |
| Mode | Select | What to scrape: Artworks, Artists, or Gallery Shows |
| Keyword / Search Query | Text | Keyword to search for (used in artworks and artists modes) |
| Max Items | Number | Free users: Limited to 10 items. Paid users: up to 1,000,000 |
| For Sale Only | Checkbox | Only return artworks currently for sale (artworks mode only) |
| Shows Status | Select | Filter shows by Upcoming, Running, or Closed (shows mode only) |

**Example 1: For-sale artworks by keyword**

```
{
  "mode": "artworks",
  "keyword": "picasso",
  "forSale": true,
  "maxItems": 100
}
```

**Example 2: Gallery shows currently running**

```
{
  "mode": "shows",
  "showsStatus": "running",
  "maxItems": 50
}
```

> ⚠️ **Good to Know**: Free users are limited to 10 results per run. The "For Sale Only" filter applies only to artworks mode. Shows can be filtered by upcoming, running, or closed status.

---

## 📊 Output

### 🧾 Schema

**Artworks mode:**

| Emoji | Field | Type | Description |
| --- | --- | --- | --- |
| 🖼️ | imageUrl | String | Primary artwork image URL |
| 📝 | title | String | Artwork title |
| 👤 | artistNames | String | Artist name(s) |
| 🔗 | url | String | Direct link to artwork on Artsy |
| 📅 | date | String | Year or date created |
| 🎨 | medium | String | Medium (oil, linocut, print, etc.) |
| 🏷️ | category | String | Artwork category |
| 📐 | dimensionsIn | String | Dimensions in inches |
| 📐 | dimensionsCm | String | Dimensions in centimeters |
| 💰 | priceDisplay | String | Formatted display price |
| 💵 | priceAmount | Number | Price amount as number |
| 💱 | priceCurrencyCode | String | Price currency code |
| 📊 | saleMessage | String | Sale status message |
| ✅ | availability | String | Current availability status |
| 🛒 | isForSale | Boolean | Whether artwork is for sale |
| 🔨 | isInAuction | Boolean | Whether artwork is in auction |
| 🏛️ | partnerName | String | Gallery or partner name |
| 📋 | conditionDescription | String | Condition details |
| 📜 | certificateOfAuthenticity | String | Certificate details |
| 📸 | images | Array | Full image gallery with dimensions |
| 📅 | scrapedAt | String | Timestamp when data was collected |
| ⚠️ | error | String | Error message if extraction failed |

**Artists mode:**

| Emoji | Field | Type | Description |
| --- | --- | --- | --- |
| 🖼️ | imageUrl | String | Artist profile image |
| 👤 | name | String | Artist name |
| 🌍 | nationality | String | Artist nationality |
| 📅 | birthday | String | Birth year or date |
| 📅 | deathday | String | Death year or date |
| 📝 | biography | String | Artist biography text |
| 🎨 | artworksCount | Number | Total artworks on platform |
| 🛒 | forSaleArtworksCount | Number | Artworks currently for sale |
| 🔗 | url | String | Artist profile URL |

**Shows mode:**

| Emoji | Field | Type | Description |
| --- | --- | --- | --- |
| 📝 | name | String | Exhibition name |
| 📅 | startAt | String | Show start date |
| 📅 | endAt | String | Show end date |
| 📊 | status | String | Show status |
| 🎨 | artworksCount | Number | Number of artworks in show |
| 📍 | locationCity | String | Show location city |
| 🌐 | locationCountry | String | Show location country |
| 🏛️ | partnerName | String | Gallery or partner name |
| 🔗 | url | String | Show page URL |

 
 
 

---

## ✨ Why choose Artsy Scraper

| Feature | Details |
| --- | --- |
| 🖼️ Three scraping modes | Artworks, artists, and gallery shows in a single tool |
| 💰 Pricing data | List prices, price ranges, sale messages, and auction indicators |
| 📐 Full dimensions | Measurements in both inches and centimeters with aspect ratios |
| 👤 Artist profiles | Biography, nationality, birth/death dates, and artwork counts |
| 🏛️ Gallery shows | Exhibition names, dates, locations, and partner information |
| ⚡ Fast API extraction | No browser needed - direct API calls for quick results |
| 📦 Multiple exports | Download as JSON, CSV, or Excel |

> 📊 **25+ data fields per artwork including pricing, dimensions, and provenance**

---

## ✨ Why choose this Actor

|  | Capability |
| --- | --- |
| 🎯 | **Built for the job.** Scoped specifically to this data source so you skip the parser engineering entirely. |
| 🔖 | **Structured output.** Clean, typed fields ready for analysis, dashboards, or downstream pipelines. |
| ⚡ | **Fast.** Optimized request patterns return results in seconds, not minutes. |
| 🔁 | **Always fresh.** Every run pulls live data, so the dataset reflects the source as of run time. |
| 🌐 | **No infra to manage.** Apify handles proxies, retries, scaling, scheduling, and storage. |
| 🛡️ | **Reliable.** Battle-tested across many runs and edge cases, with graceful error handling. |
| 🚫 | **No code required.** Configure in the UI, run from CLI, schedule via cron, or call from any language with the Apify SDK. |

> 📊 Production-grade structured data without the engineering overhead of building and maintaining your own scraper.

---

## 📈 How it compares

| Feature | Artsy Scraper | Other Tools |
| --- | --- | --- |
| Artworks + artists + shows | Yes | Usually one type |
| Pricing with currency | Yes | Rarely |
| Dimensions in inches and cm | Yes | No |
| Condition and authenticity | Yes | No |
| Artist biography and counts | Yes | Limited |
| Gallery show dates and locations | Yes | No |
| For-sale and auction filters | Yes | No |
| Export formats | JSON, CSV, Excel | Varies |

---

## 🚀 How to use

1. **Sign up** - [Create a free account with $5 credit](https://console.apify.com/sign-up?fpr=vmoqkp)
2. **Find the tool** - Search for "Artsy Scraper" in the Apify Store
3. **Configure** - Choose mode (artworks, artists, or shows), set keyword and filters
4. **Run it** - Click "Start" and wait for results
5. **Export data** - Download as JSON, CSV, or Excel, or connect to Google Sheets

---

## 💼 Business use cases

| 🎨 **Art Collectors** Track artwork prices and availability across galleries to find pieces before they sell and compare market values | 🏛️ **Galleries** Monitor competitor listings, pricing strategies, and exhibition schedules to plan your own programming |
| --- | --- |
| 📊 **Market Researchers** Analyze art market trends by medium, artist, price range, and geography for investment reports | 💼 **Appraisers** Compare similar artworks by the same artist, medium, and date for accurate valuation estimates |

---

---

## 🌟 Beyond business use cases

Data like this powers more than commercial workflows. The same structured records support research, education, civic projects, and personal initiatives.

| ### 🎓 Research and academia     - Empirical datasets for papers, thesis work, and coursework - Longitudinal studies tracking changes across snapshots - Reproducible research with cited, versioned data pulls - Classroom exercises on data analysis and ethical scraping | ### 🎨 Personal and creative     - Side projects, portfolio demos, and indie app launches - Data visualizations, dashboards, and infographics - Content research for bloggers, YouTubers, and podcasters - Hobbyist collections and personal trackers |
| --- | --- |
| ### 🤝 Non-profit and civic     - Transparency reporting and accountability projects - Advocacy campaigns backed by public-interest data - Community-run databases for local issues - Investigative journalism on public records | ### 🧪 Experimentation     - Prototype AI and machine-learning pipelines with real data - Validate product-market hypotheses before engineering spend - Train small domain-specific models on niche corpora - Test dashboard concepts with live input |

## 🤖 Ask an AI assistant about this scraper

Open a ready-to-send prompt about this ParseForge actor in the AI of your choice:

- 💬 [**ChatGPT**](https://chat.openai.com/?q=How%20do%20I%20use%20the%20Artsy%20Scraper%20-%20Artworks%2C%20Artists%20%26%20Shows%20by%20ParseForge%20on%20Apify%3F%20Show%20me%20input%20examples%2C%20output%20fields%2C%20common%20use%20cases%2C%20and%20how%20to%20integrate%20it%20into%20a%20workflow.)
- 🧠 [**Claude**](https://claude.ai/new?q=How%20do%20I%20use%20the%20Artsy%20Scraper%20-%20Artworks%2C%20Artists%20%26%20Shows%20by%20ParseForge%20on%20Apify%3F%20Show%20me%20input%20examples%2C%20output%20fields%2C%20common%20use%20cases%2C%20and%20how%20to%20integrate%20it%20into%20a%20workflow.)
- 🔍 [**Perplexity**](https://perplexity.ai/search?q=How%20do%20I%20use%20the%20Artsy%20Scraper%20-%20Artworks%2C%20Artists%20%26%20Shows%20by%20ParseForge%20on%20Apify%3F%20Show%20me%20input%20examples%2C%20output%20fields%2C%20common%20use%20cases%2C%20and%20how%20to%20integrate%20it%20into%20a%20workflow.)
- 🅒 [**Copilot**](https://copilot.microsoft.com/?q=How%20do%20I%20use%20the%20Artsy%20Scraper%20-%20Artworks%2C%20Artists%20%26%20Shows%20by%20ParseForge%20on%20Apify%3F%20Show%20me%20input%20examples%2C%20output%20fields%2C%20common%20use%20cases%2C%20and%20how%20to%20integrate%20it%20into%20a%20workflow.)

## ❓ Frequently Asked Questions

### 💳 Do I need a paid Apify plan to run this actor?

No. You can start right now on the free Apify plan, which includes **$5 in free monthly credit**. That is enough to run this actor several times and explore the output before committing to anything. Paid plans unlock higher limits, more concurrent runs, and larger datasets. [Create a free Apify account here](https://console.apify.com/sign-up?fpr=vmoqkp) to get started.

### 🚨 What happens if my run fails or returns no results?

Failed runs are not charged. If the source site changes, proxies get rate-limited, or a specific input matches nothing, re-run the actor or open our [contact form](https://tally.so/r/BzdKgA) and we will investigate. You can also check the run log in the Apify console to see why the run stopped.

### 📏 How many items can I scrape per run?

Free users are limited to **10 items per run** so you can preview the output and confirm the actor works for your use case. Paid users can raise `maxItems` up to **1,000,000** per run. [Upgrade here](https://console.apify.com/sign-up?fpr=vmoqkp) if you need full scale.

### 🕒 How fresh is the data?

Every run fetches live data at the moment of execution. There is no cache or delay: the records you get reflect what the source returned at that moment. Schedule the actor to maintain a rolling snapshot of the data you need.

### 🧑‍💻 Can I call this actor from my own code?

Yes. Apify exposes every actor as a REST endpoint and ships first-class SDKs for [Node.js](https://docs.apify.com/sdk/js) and [Python](https://docs.apify.com/sdk/python). You can start a run, read the dataset, and handle webhooks from your own app in a few lines. All you need is your Apify API token.

### 📤 How do I export the data?

Every Apify dataset can be downloaded in one click from the console as CSV, JSON, JSONL, Excel, HTML, XML, or RSS. You can also pull results programmatically via the [Apify API](https://docs.apify.com/api/v2) or stream them into BigQuery, S3, and other destinations through built-in integrations.

### 📅 Can I schedule the actor to run automatically?

Yes. Use the Apify scheduler to run the actor on any cadence, from hourly to monthly. Results are saved to your dataset and can be delivered to webhooks, email, Slack, cloud storage, or automation tools such as Zapier and Make.

---

## 🔌 Automating with code

**Node.js example:**

```
import { ApifyClient } from 'apify-client';
const client = new ApifyClient({ token: 'YOUR_API_TOKEN' });
const run = await client.actor("parseforge/artsy-scraper").call({
  mode: "artworks",
  keyword: "picasso",
  forSale: true,
  maxItems: 100
});
const { items } = await client.dataset(run.defaultDatasetId).listItems();
console.log(items);
```

**Python example:**

```
from apify_client import ApifyClient
client = ApifyClient("YOUR_API_TOKEN")
run = client.actor("parseforge/artsy-scraper").call(run_input={
    "mode": "artworks",
    "keyword": "picasso",
    "forSale": True,
    "maxItems": 100
})
items = list(client.dataset(run["defaultDatasetId"]).iterate_items())
print(items)
```

See the [Apify API docs](https://docs.apify.com/api/v2) for more integration options.

## 🔌 Integrate with your tools

- [Make](https://docs.apify.com/platform/integrations/make) - Automate art data workflows
- [Zapier](https://docs.apify.com/platform/integrations/zapier) - Get alerts on new listings
- [GitHub](https://docs.apify.com/platform/integrations/github) - Version control integration
- [Slack](https://docs.apify.com/platform/integrations/slack) - Get notifications when runs complete
- [Airbyte](https://docs.apify.com/platform/integrations/airbyte) - Data pipeline integration
- [Google Drive](https://docs.apify.com/platform/integrations/drive) - Export directly to spreadsheets

---

## 🔌 Integrate with any app

Artsy Scraper - Artworks, Artists & Shows connects to any cloud service via [Apify integrations](https://apify.com/integrations):

- [**Make**](https://docs.apify.com/platform/integrations/make) - Automate multi-step workflows
- [**Zapier**](https://docs.apify.com/platform/integrations/zapier) - Connect with 5,000+ apps
- [**Slack**](https://docs.apify.com/platform/integrations/slack) - Get run notifications in your channels
- [**Airbyte**](https://docs.apify.com/platform/integrations/airbyte) - Pipe results into your warehouse
- [**GitHub**](https://docs.apify.com/platform/integrations/github) - Trigger runs from commits and releases
- [**Google Drive**](https://docs.apify.com/platform/integrations/drive) - Export datasets straight to Sheets

You can also use webhooks to trigger downstream actions when a run finishes. Push fresh data into your product backend, or alert your team in Slack.

---

## 🔗 Recommended Actors

| Actor | Description |
| --- | --- |
| [Etsy Scraper](https://apify.com/parseforge/etsy-scraper) | Collect handmade and vintage marketplace listings |
| [LiveAuctioneers Scraper](https://apify.com/parseforge/liveauctioneers-scraper) | Extract auction house results and lot data |
| [Poshmark Scraper](https://apify.com/parseforge/poshmark-scraper) | Collect fashion resale marketplace listings |
| [CoinGecko Scraper](https://apify.com/parseforge/coingecko-scraper) | Cryptocurrency market data and trends |
| [eBay Scraper](https://apify.com/parseforge/ebay-scraper) | Auction and marketplace listing data |

Browse our complete collection of [data extraction tools](https://apify.com/parseforge) for more.

---

## 🆘 Need Help?

- Check the FAQ section above for common questions
- Visit the [Apify documentation](https://docs.apify.com) for platform guides
- Contact us to request a new scraper, propose a custom project, or report an issue at [Tally contact form](https://tally.so/r/BzdKgA)

---

> **Disclaimer**: This Actor is an independent tool and is not affiliated with, endorsed by, or connected to Artsy. It accesses only publicly available data.