# Final Project - Sampling Techniques and Data Wrangling

## 📋 Student Information

**Name:** Gregorio Vianney Putra  
**NRP:** 5052231019 

---

## 📖 Project Description

This final project provides hands-on experience in cleaning, standardizing, wrangling, and analyzing real-world data using Python. By building a data cleaning pipeline from start to finish and compiling a main analysis notebook including Exploratory Data Analysis (EDA)

This project analyzes the **Spotify Songs** dataset, which contains approximately 5000 songs from 6 main categories (EDM, Latin, Pop, R&B, Rap, & Rock). This dataset was collected using the `spotifyr` package and contains various audio features from the Spotify API such as danceability, energy, valence, tempo, and others  


### Analysis Objectives
1. **Popularity Drivers Analysis**: Identify factors that influence song popularity
2. **Audio Features Exploration**: Understand the characteristics of music from various genres
3. **Data Cleaning & Transformation**: Clean and process data for accurate analysis
4. **Data Visualization**: Generate insights through informative visualizations

---

## 🗂️ Project File Structure

```
final-project/
│
├── data/
│   ├── raw/                         
│   │   └── spotify_songs.csv         # Raw Dataset
│   └── processed/                 
│       └── spotify_cleaned.csv       # Cleaned Dataset
│
├── notebooks/
│   └── final_project.ipynb           # Main Analysis Notebook
│
├── requirements.txt                  # List of Python packages used
└── README.md                         # Project Documentation
```

---

## 🚀 How to Restart a Project

### 1. Environment Setup

#### Option A: Using pip

```bash
# Clone or download this repository
# Create a virtual environment (optional but recommended)
python -m venv venv

# Activate the virtual environment
# For Windows:
venv\Scripts\activate

# For Linux/Mac:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

#### Option B: Using conda

```bash
# Create a conda environment
conda create -n spotify-analysis python=3.9

# Activate the environment
conda activate spotify-analysis

# Install dependencies
pip install -r requirements.txt
```

### 2. Data Preparation

Make sure the folder structure is correct:

```bash
# Create the necessary folders
mkdir -p ../data/raw
mkdir -p ../data/processed
```

Download the dataset `spotify_songs.csv` from [Dataset Source](https://github.com/neni1705/FinalProject_DataWrangling_2025/tree/488de37a5a559275194d62baa48812ce69d2307c/Dataset/Spotify%20Genre%20dataset) and place it in the folder `../data/raw/`

### 3. Running the Notebook

```bash
# Run Jupyter Notebook
jupyter notebook

# Or use JupyterLab
jupyter lab
```

Open the file `../data/notebooks/final_project.ipynb` and run the cells sequentially from top to bottom.

### 4. Execution Order

1. **Section A**: Introduction - Reading the dataset description and analysis objectives
2. **Section B**: Setup - Importing libraries and defining paths
3. **Section C**: Data Preparation - Loading and inspecting the dataset
4. **Section D**: Data Cleaning - Cleaning the data (duplicates, missing values, outliers)
5. **Section E**: Data Transformation & Analysis - Data transformation and analysis
6. **Section F**: Visualization - Creating visualizations of insights
7. **Section G**: Conclusion - Conclusions from the analysis

---

## 📦 Requirements / Dependencies

### Python Version
- Python 3.7 or higher

### Library yang Digunakan

| Library | Version (minimum) | Function |
|---------|-----------------|--------|
| **pandas** | 1.3.0 | Tabular data manipulation and analysis |
| **numpy** | 1.21.0 | Numerical and array operations |
| **matplotlib** | 3.4.0 | Basic data visualization |
| **seaborn** | 0.11.0 | More attractive statistical visualization |
| **scipy** | 1.7.0 | Statistical functions and scientific computing |
| **jupyter** | 1.0.0 | Interactive notebook environment |

### Requirements.txt file

Create a file named `requirements.txt` with the following contents:

```
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scipy>=1.7.0
jupyter>=1.0.0
```

---

## 📊 Dataset Information

### Dataset Source
- **Primary source**: [GitHub Repository](https://github.com/neni1705/FinalProject_DataWrangling_2025/tree/488de37a5a559275194d62baa48812ce69d2307c/Dataset/Spotify%20Genre%20dataset)
- **Original source**: Spotify API via [`spotifyr` package](https://www.rcharlie.com/spotifyr/)
- **Contributors**: Charlie Thompson, Josiah Parry, Donal Phipps, Tom Wolff

### Dataset Characteristics
- **Total Rows**: ~32,000 songs
- **Total Columns**: 23 columns
- **Genre**: EDM, Latin, Pop, R&B, Rap, Rock
- **Format**: CSV

### Main Features of the Dataset

|variable                 |class     |description |
|:---|:---|:-----------|
|track_id                 |character | Song unique ID|
|track_name               |character | Song Name|
|track_artist             |character | Song Artist|
|track_popularity         |double    | Song Popularity (0-100) where higher is better |
|track_album_id           |character | Album unique ID|
|track_album_name         |character | Song album name |
|track_album_release_date |character | Date when album released |
|playlist_name            |character | Name of playlist |
|playlist_id              |character | Playlist ID|
|playlist_genre           |character | Playlist genre |
|playlist_subgenre        |character | Playlist subgenre|
|danceability             |double    | Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable. |
|energy                   |double    | Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy. |
|key                      |double    | The estimated overall key of the track. Integers map to pitches using standard Pitch Class notation . E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1. |
|loudness                 |double    | The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typical range between -60 and 0 db.|
|mode                     |double    | Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.|
|speechiness              |double    | Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks. |
|acousticness             |double    | A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.|
|instrumentalness         |double    | Predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly "vocal". The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0. |
|liveness                 |double    | Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live. |
|valence                  |double    | A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry). |
|tempo                    |double    | The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration. |
|duration_ms              |double    | Duration of song in milliseconds |

Complete documentation of audio features: [Spotify Audio Features API](https://developer.spotify.com/documentation/web-api/reference/get-audio-features)

---

## 🔍 Analysis Steps

### 1. Data Loading & Inspection
- Import dataset from CSV
- Initial Exploratory Data Analysis (EDA)
- Understanding data structure and characteristics

### 2. Data Cleaning
- **Handling Duplicates**: Identify and remove duplicate data
- **Handling Missing Values**: Detect and treat missing data
- **Handling Outliers**: Identify and treat outliers
- **Data Validation**: Validate value ranges and data consistency

### 3. Data Transformation
- Standardize data formats
- Feature engineering (if necessary)
- Normalize values

### 4. Data Analysis & Visualization
- Descriptive statistical analysis
- Correlation analysis between features
- Analysis of differences between genres
- Visualization of distribution and relationships

---

## 📚 Reference

### Dataset & Tools
1. [Spotify Genre Dataset - GitHub](https://github.com/neni1705/FinalProject_DataWrangling_2025/tree/488de37a5a559275194d62baa48812ce69d2307c/Dataset/Spotify%20Genre%20dataset)
2. [spotifyr Package](https://www.rcharlie.com/spotifyr/)
3. [Spotify Audio Features API Documentation](https://developer.spotify.com/documentation/web-api/reference/get-audio-features)
4. [TidyTuesday - Spotify Songs](https://github.com/rfordatascience/tidytuesday/issues/160)

### Research Papers & Articles
5. [Musical Trends and Predictability of Success in Contemporary Songs](https://royalsocietypublishing.org/doi/10.1098/rsos.171274) - Royal Society Open Science
6. [Measuring the Evolution of Contemporary Western Popular Music](https://www.nature.com/articles/srep00521) - Nature Scientific Reports
7. [Dance Hit Song Prediction](https://ideas.repec.org/p/ant/wpaper/2014003.html) - RePEc
8. [How Consumers' Adoption of Online Streaming Affects Music Consumption and Discovery](https://pubsonline.informs.org/doi/abs/10.1287/mksc.2017.1051) - INFORMS Marketing Science
9. [Music Genre Classification](https://www.researchgate.net/publication/397522001_Music_Genre_Classification) - ResearchGate
10. [Music Mood Detection Based On Audio And Lyrics With Deep Neural Net](https://doi.org/10.48550/arXiv.1809.07276) - arXiv

### Blog Posts & Tutorials
11. [Classifying Songs by Genre - Kaylin Pavlik](https://www.kaylinpavlik.com/classifying-songs-genres/)
12. [Data Cleaning: Langkah Fundamental Sebelum Analisis dan Modeling Data](https://binus.ac.id/bekasi/accounting-technology/2024/12/06/data-cleaning-langkah-fundamental-sebelum-analisis-dan-modeling-data/) - BINUS University
13. [Data Inspection in Python](https://sustainabilitymethods.org/index.php/Data_Inspection_in_Python) - Sustainability Methods

### Technical Documentation
14. [What is Data Cleaning](https://www.ibm.com/id-id/think/topics/data-cleaning) - IBM
15. [Data Transformation](https://www.ibm.com/id-id/think/topics/data-transformation) - IBM
16. [Data Standardization](https://www.sisense.com/glossary/data-standardization/) - Sisense

### Python Libraries Documentation
17. [Pandas Documentation](https://pypi.org/project/pandas/)
18. [NumPy Documentation](https://numpy.org/doc/stable/)
19. [Matplotlib Documentation](https://matplotlib.org/)
20. [Seaborn Documentation](https://seaborn.pydata.org/)
21. [SciPy Documentation](https://pypi.org/project/scipy/)
22. [Jupyter Install](https://jupyter.org/install)
23. [Python os Module](https://docs.python.org/3/library/os.html)

### Data Handling References
24. [Prevention and Handling of Lost Data](https://pmc.ncbi.nlm.nih.gov/articles/PMC3668100/) - PMC
25. [DataFrame dropna() Method](https://www.geeksforgeeks.org/python/python-pandas-dataframe-dropna/) - GeeksforGeeks
26. [Drop Duplicates in Pandas](https://note.nkmk.me/en/python-pandas-duplicated-drop-duplicates/)

### Audio Technical Standards
27. [Algorithms to Measure Audio Programme Loudness and True-Peak Audio Level](https://www.itu.int/rec/R-REC-BS.1770-4-201510-S/en) - ITU-R BS.1770-4
28. [Overload in Signal Conversion](https://www.academia.edu/37431751/Overload_in_Signal_Conversion) - Academia.edu
29. [Tempo Adalah](https://s1sm.fbs.unesa.ac.id/post/tempo-adalah) - UNESA

### Social Media & Community

30. [Charlie Thompson (@_RCharlie)](https://twitter.com/_RCharlie)
31. [Josiah Parry (@JosiahParry)](https://twitter.com/JosiahParry)
32. [Kaylin Pavlik (@kaylinquest)](https://twitter.com/kaylinquest/status/1213138536570015745)
33. [Neal Grantham (@nsgrantham)](https://twitter.com/nsgrantham/status/1213190975113199616)


---

## 💡 Tips & Troubleshooting

### Common Issues

1. **ModuleNotFoundError**: Ensure all libraries are installed with `pip install -r requirements.txt`
2. **FileNotFoundError**: Check the dataset path in the setup cell (`RAW_DATA_PATH`)
3. **Memory Error**: If the dataset is too large, use `pd.read_csv()` with the `chunksize` parameter

### Best Practices
- Run cells sequentially from top to bottom
- Restart the kernel if an unclear error occurs
- Save the data cleaning results to `../data/processed/` for further analysis
- Use a virtual environment to avoid dependency conflicts

---

## 📝 License

This dataset is sourced from Spotify and collected for educational and research purposes. Be sure to comply with the [Spotify Developer Terms of Service](https://developer.spotify.com/terms).

---

## 👤 Contact

If you have any questions or issues, please contact:
- Email: gregorioputra@gmail.com
- GitHub: [artupoir](https://github.com/artupoir)

---

###### Copyright ©2025.  Final Project - Sampling Techniques and Data Wrangling (Spotify Songs Analysis)
