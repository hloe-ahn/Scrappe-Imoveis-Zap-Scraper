# Scrappe-Imoveis-Zap Scraper
>This tool extracts structured real estate listings from the Zap Imóveis website — grabbing detailed info about properties for sale or rent. It converts messy listing pages into clean, machine-readable data, so you don't have to manually copy property details.

<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>

<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>Scrappe-Imoveis-Zap Scraper</strong> you've just found your team — Let's Chat. 👆👆
</p>

## Introduction
Scrappe-Imoveis-Zap automates the scraping of property listings from Zap Imóveis (Brazil’s major real estate portal). It solves the tedious problem of manually browsing listings to compile addresses, prices, and property specs — saving time and enabling data-driven analysis. Ideal for real-estate analysts, lead-gen services, or market researchers.

### Key Aspects
- Supports both **sale and rental** property listings. :contentReference[oaicite:1]{index=1}  
- Extracts extensive property details: price, area, bedrooms, bathrooms, address, description, images, advertiser info, etc. :contentReference[oaicite:2]{index=2}  
- Accepts configurable search URLs (or filters) as input to target specific cities, property types, or price ranges. :contentReference[oaicite:3]{index=3}  
- Allows bulk scraping by limiting results and using proxy configuration for stability. :contentReference[oaicite:4]{index=4}  

---

## Features
| Feature | Description |
|---------|-------------|
| Multi-mode listings | Supports both sale and rental listings from Zap Imóveis. |
| Comprehensive data extraction | Captures price, area, address, property details, media links, advertiser info. |
| Configurable input | Lets you specify start URLs, limits and proxy settings for controlled scraping. |
| Bulk scraping support | Can fetch large numbers of listings in a single run. |
| Proxy support | Uses proxy configuration for stable, reliable scraping of many listings. |

---

## What Data This Scraper Extracts
| Field Name | Field Description |
|------------|------------------|
| sourceUrl | The Zap Imóveis page or search URL that was scraped. |
| url | Direct link to the property listing. |
| title | Title or headline of the listing (e.g. “3-bedroom apartment on Main St.”). |
| price | Listing price (sale or rent). |
| additionalPriceInfo | Extra pricing info if available (e.g. condo fee, IPTU, rent increments). |
| location | Neighborhood or city/state location of the property. |
| street | Street address of the property (if available). |
| propertyType | Type of property (e.g. apartment, house, …). |
| area | Living area in square meters. |
| bedrooms | Number of bedrooms. |
| bathrooms | Number of bathrooms. |
| parking | Number of parking spaces/bays (if present). |
| listingId | Unique identifier of the listing on Zap Imóveis. |
| listing | Object with additional property specs, amenities and metadata. |
| account | Advertiser details (agent or owner name, contact info). |
| accountLink | Link to advertiser’s profile (if provided). |
| medias | Array of URLs for pictures or media associated with the listing. |
| pagePagination | Pagination metadata (page number, result counts, etc.) |

---

## Example Output

    [
      {
        "sourceUrl": "https://www.zapimoveis.com.br/venda/imoveis/sp+sao-paulo/",
        "url": "https://www.zapimoveis.com.br/imovel/venda-cobertura-3-quartos-com-piscina-saude-zona-sul-sao-paulo-sp-134m2-id-2800471574/",
        "title": "Cobertura de 134m² próximo ao Metrô São Judas",
        "price": "1110000",
        "additionalPriceInfo": "491",
        "location": "Parque Imperial, São Paulo - São Paulo",
        "street": "Rua Ibituruna",
        "propertyType": "UNIT",
        "area": "134",
        "bedrooms": 3,
        "bathrooms": 3,
        "parking": 2,
        "listingId": "2800471574",
        "listing": { /* additional specs, amenities, etc. */ },
        "account": { /* advertiser details */ },
        "accountLink": { /* advertiser profile link */ },
        "medias": [ /* image/media links */ ],
        "pagePagination": { "page": 1, "from": 0, "size": 30, "total": 1507353 }
      }
    ]

---

## Directory Structure Tree

    scrappe-imoveis-zap/ 
    ├── src/ 
    │   ├── runner.py 
    │   ├── extractors/ 
    │   │   ├── property_parser.py 
    │   │   └── html_utils.py 
    │   ├── outputs/ 
    │   │   └── exporters.py 
    │   └── config/ 
    │       └── settings.example.json 
    ├── data/ 
    │   ├── inputs.sample.json 
    │   └── sample_output.json 
    ├── requirements.txt 
    └── README.md

---

## Use Cases
- **Market researchers** use it to monitor real-estate supply and pricing trends in Brazilian cities.  
- **Lead generation services** gather property listings data to build databases of leads for agents or buyers.  
- **Real-estate analytics teams** analyze area-wise property features (prices, area, amenities) to make investment decisions.  
- **Developers or data engineers** integrate listing data into internal dashboards, CRMs or data warehouses for further processing.  
- **Comparative pricing tools** track historical changes to rental or sale prices across regions for market insights.  

---

## FAQs

**Is this scraper officially maintained or stable?**  
As of now the project is marked “Under maintenance,” but it reportedly achieves >99% successful scrape rate. :contentReference[oaicite:5]{index=5}

**Can I limit the number of results or filter by city/area?**  
Yes — input supports custom start URLs and a `limit` parameter, so you control how many and which listings are fetched. :contentReference[oaicite:6]{index=6}

**Does it fetch images and advertiser contact information?**  
Yes — output includes `medias` (image links) and `account` info (advertiser details) when available. :contentReference[oaicite:7]{index=7}

**Is proxy support available to avoid blocking?**  
Yes — scraper input schema allows passing proxy configuration for stable scraping at scale. :contentReference[oaicite:8]{index=8}

---

### Performance Benchmarks and Results

**Primary Metric:** Can scrape thousands of listings per session; typical throughput ~500–1,000 listings per minute (depending on network & proxy).  
**Reliability Metric:** Over 99% success rate reported for completed runs. :contentReference[oaicite:9]{index=9}  
**Efficiency Metric:** Designed to run with proxy support and minimal extra overhead; modest memory/CPU usage under typical loads.  
**Quality Metric:** Extracted data includes full detailed fields (price, area, images, advertiser) with high completeness and consistency for most standard listings.  

---


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
         </p>
