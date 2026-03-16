# 🗺️ TweetMap

> Real-time geospatial visualization of live Twitter streams plotted on an interactive Leaflet.js map.

![Python](https://img.shields.io/badge/Python-3.6+-3776AB?style=flat-square&logo=python&logoColor=white)
![Leaflet](https://img.shields.io/badge/Leaflet.js-interactive_map-199900?style=flat-square)
![Twitter API](https://img.shields.io/badge/Twitter-Streaming_API-1DA1F2?style=flat-square&logo=twitter&logoColor=white)

---

## 📖 Overview

TweetMap streams live tweets via the Twitter Streaming API, extracts geolocation coordinates, and renders them as interactive markers on a Leaflet.js map — all in your browser. Watch the world tweet in real time across any topic you choose.

## 🏗️ Architecture

```
[Twitter Streaming API]
        │
        ▼
[twitter_streaming.py] ──► [tweets.json]
        │
        ▼
[Geocoder.py] ──► Extract lat/lng coordinates
        │
        ▼
[writeintojs.py] ──► Inject into JS data variable
        │
        ▼
[geomap.html] ──► Leaflet.js map in browser
```

## ✨ Features

- **Real-time streaming** — Live tweet ingestion via Twitter's Streaming API
- **Geocoding** — Automatic extraction of lat/lng from tweet metadata
- **Interactive map** — Leaflet.js-powered map with clickable markers
- **Filterable** — Track any keyword, hashtag, or topic
- **Sample dataset** — Includes 85 MB sample tweet dataset (`tweets.json`)

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Data Ingestion | Python, Twitter Streaming API (Tweepy) |
| Geocoding | Python custom Geocoder |
| Visualization | Leaflet.js |
| Data Storage | JSON flat file |

## 🚀 Quick Start

```bash
# Install dependencies
pip install tweepy

# Add your Twitter API credentials in twitter_streaming.py
# Then stream live tweets
python twitter_streaming.py

# Geocode the collected tweets
python Geocoder.py

# Write data into JS format
python writeintojs.py

# Open the map in your browser
open geomap.html
```

## 📂 Repo Structure

```
├── twitter_streaming.py   # Twitter API streamer
├── Geocoder.py            # Coordinate extraction
├── writeintojs.py         # JS data writer
├── geomap.html            # Leaflet map UI
├── leaflet/               # Leaflet.js library assets
└── tweets.json            # Sample tweet dataset (85 MB)
```

## 💡 Use Cases

- Track trending topics geographically
- Real-time event monitoring
- Social media research & journalism
- Sentiment mapping across regions

---

<p align="center">Made with ❤️ by <a href="https://github.com/durveshvedak">Durvesh Vedak</a></p>
