# NoSQL Challenge: UK Food Standards Analysis

## Overview

The `nosql-challenge` repository contains analysis of the UK Food Standards Agency's hygiene ratings for various establishments across the United Kingdom. This project helps journalists and food critics from the food magazine, Eat Safe, Love, focus their future articles on establishments based on their hygiene standards.

## Repository Structure

- `Resources/`: Contains the `establishments.json` data file to be imported into the MongoDB database.
- `NoSQL_Setup.ipynb`: Jupyter Notebook for initializing and setting up the database.
- `NoSQL_Analysis.ipynb`: Jupyter Notebook for performing exploratory analysis on the database.
- `README.md`: This file, providing an overview and instructions for the project.

## Getting Started

### Initial Setup

1. Clone this repository to your local machine.
2. Navigate to the cloned repository folder in your terminal.


### Setup Requirements

- MongoDB installed and running on your system.
- PyMongo, pprint and pandas libraries imported.


### Importing the Data

Run the following command to import the `establishments.json` file into your MongoDB database:

```sh
mongoimport --type json -d uk_food -c establishments --drop --jsonArray --file ./Resources/establishments.json
```

## Performing Analysis

Open the `NoSQL_Analysis.ipynb` file in Jupyter Notebook.
Follow the instructions within the notebook to complete the analysis of the MongoDB database.

## Part 1: Database Verification

- List all databases and confirm the existence of `uk_food`.
- List all collections within `uk_food` and check for `establishments`.
- Display one document from the `establishments` collection using `pprint`.

## Part 2: Database Updates

- Add a new halal restaurant in Greenwich to the collection.
- Retrieve and assign the correct `BusinessTypeID` for "Restaurant/Cafe/Canteen".
- Update the new restaurant document with the retrieved `BusinessTypeID`.
- Remove establishments within the Dover Local Authority.
- Convert string values of latitude and longitude to decimal numbers using `update_many`.

## Part 3: Exploratory Analysis

- Identify establishments with a hygiene score equal to 20.
- Find establishments in London with a `RatingValue` greater than or equal to 4 using `$regex`.
- Determine the top 5 establishments with a `RatingValue` of '5', sorted by the lowest hygiene score, nearest to "Penang Flavours".
- Aggregate the number of establishments with a hygiene score of 0 by Local Authority, sorting the results from highest to lowest.

## Support

For any additional help or clarification, please open an issue in the repository and the maintainers will assist you.

## Author
- [Elcin Kobya Imanci](https://github.com/ELCINKOBYAIMANCI)

