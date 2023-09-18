# ElectroSearch

This project is a Flask-based web application that uses Elasticsearch to search through electronics data and display results to the user.

## Features:

1. **Home Page**: Displays all the data present in the Elasticsearch index.
2. **Search Functionality**: Allows users to search for electronics products based on name, brand, and categories.
3. **Sorting**: Provides sorting options based on price and date added.
4. **Data Population**: Provides an endpoint to populate the Elasticsearch index with data from a CSV file.

## Dependencies:

- Flask
- Flask-RESTful
- Elasticsearch

## Setup:

1. **Setup Virtual Environment** (Recommended)
```bash
python3 -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
```

2. **Install Dependencies**
```bash
pip install Flask Flask-RESTful elasticsearch
```

3. **Run the Application**
```bash
python main.py
```

## Routes:

1. **/**: The home route that displays all the data.
2. **/search**: Route to handle search queries.
3. **/osearch**: Route to handle search queries with sorting.
4. **/populate**: Endpoint to populate the Elasticsearch index.

## Elasticsearch Configuration:

Make sure to have Elasticsearch running locally on port `9200` with the credentials `elastic` and your password. Adjust the configurations in the `EsManagement` class if your setup is different.

## Usage:

1. Visit the home page to view all data.
2. Use the search form to filter results based on name, brand, and categories.
3. Click on the "Sort by Price" button to sort the results by price.

## Data Source:

The data is read from `ElectronicsData.csv`. Make sure this file is present in the root directory.
