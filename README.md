# Kijiji Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Kijiji Scraper](https://oxylabs.io/products/scraper-api/web/kijiji?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Kijiji website effortlessly. This brief guide explains how an Kijiji Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Kijiji results by providing your own URLs to our service. We can return the HTML for any Kijiji page you like.

#### Python code example

The example below illustrates how you can get HTML of Kijiji page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.kijiji.ca/h-gta-greater-toronto-area/1700272'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/kijiji-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html id=\"reset\" lang=\"en\">\n<head>\n    <meta charset=\"utf-8\">\n    <title>Kijiji in To ... </html>",
      "created_at": "2023-12-18 11:12:51",
      "updated_at": "2023-12-18 11:12:52",
      "page": 1,
      "url": "https://www.kijiji.ca/h-gta-greater-toronto-area/1700272",
      "job_id": "7142471772355440641",
      "status_code": 200
    }
  ]
}
```
With our Kijiji Scraper, you can seamlessly pull public data from any Kijiji web page. Gather necessary property details, including price, reviews, or property descriptions, to keep an eye on the real estate market and get a leg up on your competitors. For any queries, reach out to our support team through live chat or email us at hello@oxylabs.io.