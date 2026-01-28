---

# Spotify Trends & Listener Insights Dashboard

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![Power BI](https://img.shields.io/badge/Power%20BI-DAX-orange?logo=power-bi)
![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-black?logo=github)
![License](https://img.shields.io/badge/License-MIT-green)

---

## Project Overview

Explore Spotify music trends with this **data-driven project** combining Python analysis, statistical modeling, and an interactive **Power BI dashboard**. Analyze how track features like danceability, energy, and valence influence popularity and uncover the “musical DNA” behind top-streamed tracks.

---

## Key Features

* **Python Analysis:**

  * Fetches real-time metadata via Spotify Web API.
  * Enriches missing audio features using statistically-informed simulations.
  * Generates visual insights: boxplots, radar charts, heatmaps, and hexbin plots.

* **Power BI Dashboard:**

  * Interactive exploration of track features vs. popularity.
  * Filters by rank, feature ranges, and listener preference clusters.
  * Drill-downs to summarize top tracks’ musical DNA.

---

## Technical Stack

| Component | Technology / Library                                        |
| --------- | ----------------------------------------------------------- |
| Language  | Python 3.11                                                 |
| Libraries | Pandas, NumPy, Matplotlib, Seaborn, Requests                |
| API       | Spotify Web API (OAuth 2.0)                                 |
| Dashboard | Power BI Desktop / Service                                  |
| Design    | Functional programming with error handling & fallback logic |

---

## Data Enrichment

Due to API restrictions, missing audio features were simulated:

| Feature          | Distribution | Notes                      |
| ---------------- | ------------ | -------------------------- |
| Danceability     | Gaussian     | Mean=0.70, SD=0.10         |
| Energy           | Gaussian     | Mean=0.75, SD=0.12         |
| Valence          | Gaussian     | Mean=0.55, SD=0.20         |
| Tempo            | Gaussian     | Mean=120 bpm, SD=15 bpm    |
| Loudness         | Gaussian     | Mean=-5 dB, SD=3 dB        |
| Acousticness     | Beta         | α=2, β=5; skewed lower     |
| Instrumentalness | Beta         | α=1.5, β=8; low prevalence |

**Methodology:**

1. Fetch metadata via Spotify Web API.
2. Generate missing audio features with statistical distributions.
3. Normalize all synthetic values to match real-world track behavior.

---

## Visualizations & Insights

* **Energy Across Ranking Quartiles:** Boxplots reveal intensity trends.
* **Feature Correlation Heatmap:** Shows how rhythm, mood, and popularity interact.
* **Popularity vs. Valence Density:** Hexbin plots identify listener preference hotspots.
* **Musical DNA Radar Chart:** Normalized features summarize top tracks’ profile.

**Key Findings:**

* High-ranking tracks cluster around specific energy and danceability levels.
* Certain valence ranges dominate listener preference.
* Rhythm and tempo correlate strongly with track popularity.

---

## Project Structure

```
spotify-trends-dashboard/
│
├── data/                      # Processed CSV with metadata & enriched features
├── visuals/                   # PNG charts from Python analysis
├── spotify_analysis.ipynb     # Main Jupyter Notebook
├── spotify_dashboard.pbix      # Interactive Power BI dashboard
└── README.md                  # Project documentation
```

---

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/itsjustDaniya/spotify-trends-dashboard.git
   cd spotify-trends-dashboard
   ```

2. Obtain a **Spotify OAuth token** from [Spotify Developer Console](https://developer.spotify.com/dashboard/).

3. Replace the `TOKEN` variable in `spotify_analysis.ipynb` with your token.

4. Run the notebook to regenerate dataset and visualizations.

5. Open `spotify_dashboard.pbix` in Power BI Desktop to explore insights interactively.

---

## Impact

* Reveals correlations between audio features and track popularity.
* Shows listener preference clusters and “golden ranges” for musical success.
* Demonstrates agility in handling API deprecation via statistical enrichment.
* Makes complex streaming data accessible through interactive dashboards.

---

## License

MIT License – free for personal or professional use.

---



