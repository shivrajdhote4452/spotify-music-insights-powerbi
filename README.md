# Spotify Artist & Track Analytics – Power BI Dashboard

This project is a Power BI dashboard built on a Spotify-style songs dataset to analyze artists, tracks, and audio features such as energy, tempo, and danceability.[file:1]

---

## 🎯 Project Overview

The **Spotify Artist & Track Analytics** dashboard allows you to:

- Monitor total tracks and overall audio profile of the dataset  
- Identify top artists by number of tracks  
- See which tracks are most popular and most danceable  
- Explore how keys and tempo are distributed across songs[file:1]

The report uses a dark theme with Spotify-inspired colors and is intended as a portfolio / learning project.

---

## 📂 Dataset

**File:** `dataset.csv`[file:1]

Key columns:

- Identification: `track_id`, `track_name`, `artists`, `album_name`  
- Performance: `popularity`  
- Audio features: `energy`, `danceability`, `tempo`, `mode`, `key`  
- Categories: `track_genre`, `explicit`, `time_signature`[file:1]

> The dataset contains audio feature metadata only (no personal listener data).

---

## 📊 Dashboard Contents

Main elements on the report page:

### KPI Cards
- **TotalTracks** – total number of tracks in the dataset  
- **AVG_Energy** – average value of `energy`  
- **AVG_Popularity** – average track popularity  
- **Avg_Danceability** – average value of `danceability`[file:1]

### Slicers
- `track_genre` – filter by genre  
- `artists` – filter by artist

### Visuals
- **Bar chart:** Count of `track_name` by `artists` (top artists by track count)  
- **Bar chart:** Sum of `popularity` by `track_name` (most popular tracks)  
- **Donut chart:** Count of `track_name` by `key` (distribution of musical keys)  
- **Line/area chart:** Sum of `tempo` by `track_name`  
- **Bar chart:** Sum of `danceability` by `track_name`[file:1]

---

## 🧮 DAX Measures

Example measures used in the report:

```DAX
TotalTracks = COUNT('dataset'[track_id])

AVG_Energy = AVERAGE('dataset'[energy])

AVG_Popularity = AVERAGE('dataset'[popularity])

Avg_Danceabilitye = AVERAGE('dataset'[danceability])
