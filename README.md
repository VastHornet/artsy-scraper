[Artsy Scraper](https://apify.com/lulzasaur/artsy-scraper?fpr=data)

Scrape artworks, artists, and galleries from [Artsy.net](https://www.artsy.net/) — the world's largest online art marketplace. Uses the public Artsy GraphQL API (Metaphysics) with cursor-based pagination.

## Search Types

| Type | What You Get |
| --- | --- |
| **Artworks** | Title, artist, date, medium, dimensions, price, gallery, category, image URL |
| **Artists** | Name, nationality, birthday, bio, image URL |
| **Galleries** | Name, location, bio, image URL |

## Output Fields (Artworks)

| Field | Description |
| --- | --- |
| `title` | Artwork title |
| `artist` | Artist name |
| `date` | Year or date range |
| `medium` | Materials used (e.g. "Oil on canvas") |
| `dimensions` | Physical dimensions |
| `imageUrl` | Image URL |
| `price` | Sale/price message |
| `gallery` | Gallery or partner name |
| `category` | Artwork category (Painting, Sculpture, etc.) |
| `artsyUrl` | Direct link on Artsy |
| `scrapedAt` | ISO timestamp |

## Output Fields (Artists)

| Field | Description |
| --- | --- |
| `name` | Artist name |
| `birthday` | Birth year |
| `nationality` | Artist nationality |
| `bio` | Short biography |
| `imageUrl` | Artist portrait URL |
| `artsyUrl` | Direct link on Artsy |
| `scrapedAt` | ISO timestamp |

## Use Cases

- **Art market research**: Track prices, mediums, and trends across categories
- **Artist discovery**: Find artists by keyword, nationality, or period
- **Gallery analysis**: Map gallery inventory and pricing strategies
- **Collection building**: Search for specific artworks, mediums, or periods
- **Price monitoring**: Track sale messages and availability across galleries
- **Data journalism**: Analyze the art market at scale

## Example Output (Artwork)

```
{
  "title": "Guernica Study",
  "artist": "Pablo Picasso",
  "date": "1937",
  "medium": "Oil on canvas",
  "dimensions": "24 x 36 in",
  "imageUrl": "https://d32dm0rphc51dk.cloudfront.net/...",
  "price": "Contact for price",
  "gallery": "Gagosian",
  "category": "Painting",
  "artsyUrl": "https://www.artsy.net/artwork/...",
  "scrapedAt": "2026-04-25T12:00:00.000Z"
}
```

## Example Output (Artist)

```
{
  "name": "Banksy",
  "birthday": "1974",
  "nationality": "British",
  "bio": "Banksy is an anonymous England-based street artist...",
  "imageUrl": "https://d32dm0rphc51dk.cloudfront.net/...",
  "artsyUrl": "https://www.artsy.net/artist/banksy",
  "scrapedAt": "2026-04-25T12:00:00.000Z"
}
```

## Tips

- Use broad keywords like "abstract" or "sculpture" for large datasets
- Use artist names like "picasso" or "warhol" for focused results
- The `artworks` search type returns the most detailed data including pricing
- Set `maxResults` up to 5000 for comprehensive market analysis

---

## Run on Apify

This scraper runs on the [Apify platform](https://apify.com/?fpr=lulzasaur) — a full-stack web scraping and automation cloud. Sign up for a free account to get started with 30-day trial of all features.

[Try Apify free ->](https://apify.com/?fpr=lulzasaur)