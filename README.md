# T-Mobile Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [T-Mobile Scraper](https://oxylabs.io/products/scraper-api/ecommerce/t-mobile?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an T-Mobile website effortlessly. This brief guide showcases how T-Mobile Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get T-Mobile results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of T-Mobile page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.t-mobile.com/accessories'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/t-mobile-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head>\n    <meta charset=\"utf-8\">\n    <title>Cell Phone Accessories | ... </html>",
      "created_at": "2024-02-20 12:52:53",
      "updated_at": "2024-02-20 12:52:54",
      "page": 1,
      "url": "https://www.t-mobile.com/accessories",
      "job_id": "7165689769102451713",
      "status_code": 200
    }
  ]
}
```
With our T-Mobile Scraper, you can seamlessly draw out public data from any T-Mobile website. Gather essential information such as mobile plan details, customer feedback, or plan descriptions to examine the market trends and outperform your rivals. For assistance or further queries, don't hesitate to reach out to our support staff through live chat or drop us an email at hello@oxylabs.io.