## Author

**Dhyanendra Tripathi**  
Roll Number: 221010218

# Movie Semantic Search Assignment

This folder contains my solution for the Assignment-I of AI systems development course - Semantic search on movie plots assignment using **SentenceTransformers**.

## Project Overview

This project implements a semantic search engine that finds movies based on plot descriptions using AI embeddings. The system uses the **all-MiniLM-L6-v2** model from SentenceTransformers to create vector representations of movie plots and then retrieves the most relevant movies for a given query using **cosine similarity**.

## Features

- **Semantic Search**: Finds movies based on meaning, not just keywords
- **SentenceTransformers**: Uses the efficient `all-MiniLM-L6-v2` model
- **Cosine Similarity**: Ranks results by semantic similarity scores
- **Easy to Use**: Simple search function with pandas DataFrame output

## Setup Instructions

### Prerequisites

- Python 3.9 or higher
- Git

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Fresh04/AI-Systems-Development.git
cd AI-Systems-Development
cd movie-search-assignment
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run the Jupyter notebook:
```bash
jupyter notebook movie_search_solution.ipynb
```

## Usage

### Using the Python Module

```python
from movie_search import search_movies

# Search for movies
results = search_movies('spy thriller in Paris', top_n=5)
print(results)
```

### Using the Jupyter Notebook

Open `movie_search_solution.ipynb` and run all cells to see the implementation and examples.

## Testing

Run the unit tests to verify correctness:

```bash
python -m unittest tests/test_movie_search.py -v
```

The tests check:
- Correct output format (DataFrame with required columns)
- Proper handling of top_n parameter
- Similarity scores sorted in descending order
- Relevant results for queries

## File Structure

```
movie-search-assignment/
├── movie_search.py              # Main Python module
├── movie_search_solution.ipynb  # Jupyter notebook solution
├── movies.csv                   # Movie dataset
├── requirements.txt             # Python dependencies
├── tests/
│   └── test_movie_search.py     # Unit tests
└── README.md                    # This file
```

## Implementation Details

1. **Data Loading**: Loads movie data from CSV file
2. **Model Initialization**: Loads SentenceTransformers all-MiniLM-L6-v2 model
3. **Embedding Creation**: Converts movie plots into embeddings
4. **Search Function**: Computes cosine similarity and returns top results

## Dependencies

```
sentence-transformers==2.2.2
pandas==2.1.4
scikit-learn==1.3.2
numpy==1.24.4
jupyter==1.0.0
```

## Assignment Requirements Met

- Uses SentenceTransformers (all-MiniLM-L6-v2)
- Implements semantic search on movie plots
- Returns DataFrame with title, plot, and similarity_score
- Handles top_n parameter correctly
- Includes unit tests
- Complete Jupyter notebook implementation
