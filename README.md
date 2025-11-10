# Real-Time-Product-Intelligence-Platform

## Objective
Build an async Python service that:
• Receives real-time product data (name, price, reviews, image URL) via WebSocket
• Downloads and analyzes product images (extract metadata: format, size, dimensions,
etc.)
• Performs sentiment analysis on product reviews
• Aggregates and stores all product data and analytics
• Generates a DOCX report summarizing each product’s info, image metadata, and review
sentiment

## Core Requirements

Data Ingestion

• WebSocket client connects to a (mocked or public) server streaming product data in real
time
• Each product message includes: name, price, reviews (list of strings), image URL

Image Handling

• Download product image from URL
• Extract metadata (format, size, dimensions) using Pillow

Text Analytics

• Perform sentiment analysis on each review
• Aggregate sentiment scores (average, positive/negative counts)

Data Aggregation & Storage

• Store all product info, image metadata, and sentiment results in memory or SQLite
Report Generation
• For each product, generate a DOCX report (using python-docx) with:

o Product details (name, price)

o Image metadata

o Review sentiment analysis (with sample reviews)

o Embed product image

Error Handling and logging

• Handle connection errors, image download failures, and invalid data gracefully

## Testing

• Use pytest to test:
o WebSocket data ingestion
o Image Metadata Extraction
o Sentiment analysis
o DOCX report generation

## Technical Stack

• Async: asyncio, websockets, aiohttp
• Testing: pytest


## Example Workflow

1. Connect to WebSocket and receive product data:
{
"name": "Wireless Mouse",
"price": 49.99,
"reviews": ["Great mouse!", "Stopped working after a week."],
"image_url": "https://example.com/mouse.jpg"
}

2. Download image, extract metadata.
   
4. Analyze reviews for sentiment.
   
6. Store all data.
   
8. Generate a DOCX report for each product.
