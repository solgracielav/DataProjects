# Pokemon Go! Analytics – DSA 8640 Final Term Project

## Overview  
This project focuses on analyzing the **Pokémon Go!** app by extracting user ratings from the **Google Play Store** and **Apple App Store** using web scraping. The collected data is structured into a **Pandas DataFrame** and stored in **CSV** and **Excel** formats for further analysis.

## Project Objectives  
1. **Web Scraping**: Extract relevant rating metrics from **HTML files** using **BeautifulSoup**:
   - **iOS Data:**
     - Number of ratings for the **current version** (`ios_current_ratings`).
     - Number of ratings for **all versions** (`ios_all_ratings`).
   - **Android Data:**
     - **Average rating** (`android_avg_rating`).
     - **Total number of ratings** (`android_total_ratings`).
     - **Breakdown of ratings (1 to 5 stars)** (`android_ratings_1` to `android_ratings_5`).

2. **Data Organization**:
   - Store extracted data in a **Python dictionary**, using `datetime` as the key.
   - Convert the dictionary into a **Pandas DataFrame**, with `datetime` as the index.
   - Save the structured data as **pokemon.csv** and **pokemon.xlsx**.

## Dataset Description  
- **Source:** The dataset consists of **HTML files** containing Pokémon Go! rating data, collected from **July 21 to July 31, 2016**.
- **File Naming Format:** `HH_MM_pokemon_PLATFORM.html`, where:
  - `HH_MM` represents the **hour and minute**.
  - `PLATFORM` is either `android` or `ios`.
- **Data Collection Frequency:** Every **10 minutes**, resulting in up to **144 HTML files per day** per platform.

## Implementation Details  
- **Python 3.x** is used for web scraping and data processing.
- **BeautifulSoup** is used for parsing HTML files.
- **Pandas** is used for structuring and saving the dataset.

## File Structure  
```
/pokemon-go-analytics
│── data/                   # Contains HTML files (not included in repo)
│── pokemon_analysis.py      # Python script for scraping & processing
│── pokemon.csv              # Final dataset (CSV format)
│── pokemon.xlsx             # Final dataset (Excel format)
│── README.md                # Project summary
```

## Results & Insights  
- The dataset provides insights into how Pokémon Go!’s **user ratings** evolved over time.
- The structured data can be used for **trend analysis** and further exploration of **user engagement**.

## Requirements  
To run the script, install the necessary dependencies:
```bash
pip install beautifulsoup4 pandas
```

## How to Run  
1. **Place the extracted HTML files** inside the `data/` directory.
2. **Run the Python script**:
   ```bash
   python pokemon_analysis.py
   ```
3. The extracted data will be **saved as** `pokemon.csv` and `pokemon.xlsx`.

## References  
- **BeautifulSoup Documentation:** [https://www.crummy.com/software/BeautifulSoup/](https://www.crummy.com/software/BeautifulSoup/)
- **Pandas Documentation:** [https://pandas.pydata.org/](https://pandas.pydata.org/)

---
**Author:** Sol Vloebergh  
**Date:** December 2025

