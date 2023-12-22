# README: IMDb Comparisons and Visualizations

## Overview

This notebook presents a detailed analysis of IMDb movie data aiming to explore and visualise various aspects of film and TV shows to derive insights and understand audience and industry trends. It combines data handling, visualization, and analytical techniques to provide a comprehensive view of the film industry.

_Note: This is a breakaway investigation and analysis done by me (Shouvik) as a personal project inspired by this project._

## Data Source

The investigation uses the "IMDb Extensive Dataset" from [Kaggle](https://www.kaggle.com/datasets/ngochieunguyen/imdb-extensive/), which includes a wealth of information on movie details, ratings, cast, and crew.

## Libraries Used

The notebook employs several key Python libraries, including pandas, numpy, matplotlib, seaborn, and files. The aforementioned libraries aided in data manipulation, statistical analysis, and visualization.

## Key Features and Design Notes

The `clean_currency_column` function in the IMDb dataset analysis aided in cleaning and standardizing currency data, which helped provide an accurate financial analysis. It does so by checking the data type, and using regular expression to strip away non-numerical values/characters like dollar signs and commas. `pd.to_numeric`with `errors='coerce'` ensures that any unconvertible strings get changed to NaN. These provide a secure analysis, maintaining data integrity and enabling a uniform format for easy insight retrieval.

This order of merging the datasets was done particularly to extract insights relevant to our scope of investigation. By merging movie details and ratings first using an "inner" join we could focus on films with appropriate and essential information as well as a more credible understanding of audience reception. Expanding this dataset with cast and crew data with the "outer" joins (left/right), provides for a comprehensive, multi-layered analysis base that captures not only the films but the people that brought them to life as well. 

### Visualizations

- **Visualization 1:** Employs a violin plot to showcase the distribution of votes across different age groups (18-29, 30-44, 45+) in the IMDb dataset. The bandwidth parameter is finely tuned for emphasizing denser areas, helping us see the variation in the voting patterns amongst different age groups. 
  
- **Visualization 1.1:** Utilises a boxplot (box-and-whisker) to represent the votes by age distribution from the dataset. It offers a zoomed-in view that highlights the central tendency of the dataset and its variation accurately, allowing for further examination and collection of insights. 
  
- **Visualization 2:** Barplot which showcases the frequency of various genres from the top 250 movies in the dataset. This plot considers an expanded dataset where genres are separated and counted individually — for example: The Wolf of Wall Street (Biography, Comedy, Crime, Drama) adds 4 genres to the dataset for each to be counted individually — helping identify some of the most common genres and their popularity amongst some of the most renowned films.
  
- **Visualization 3:** Exploring further, a barplot is used here to compare different genres against their average votes within the top 250 movies, offering insights into how various genres are rated. The plot — coming from the average votes calculated for each genre — illustrates the relationship between movie genres and audience ratings, highlighting which genres tend to be more well-received.
  
- **Visualization 4:** Scatterplot that reveals contrasts in the count of votes against the average ratings for movies and TV shows, separated by male and female members. This visualization has an alpha of 0.5 to allow for clarity amongst overlapping data points. The plot paints a picture on some gender-based differences in voting patterns and preferences in movie ratings. 
  
- **Visualization 5:** Barplot depicting the top 20 countries by movie and TV show production. With countries on the y-axis and the production count on the x-axis, it provides a visual indication of which countries have the most movie and TV show output. 

- **Visualization 6:** Barplot that ranks the top 20 directors based on their films' average ratings. With directors on the y-axis and their average ratings on the x-axis, it highlights the success and popularity of a director's overall body of work in the film industry. 

- **Visualization 7:** Compares film budgets to worldwide gross incomes to test and study the theory of whether higher budgets necessarily mean higher gross incomes. In this scatterplot we have an unfiltered view including all data points, with budgets on the x-axis and worldwide gross incomes on the y-axis.

- **Visualization 8:** Explores the theory mentioned above with the caveat of filtering to exclude entries with zero budgets or gross income, in hopes of ensuring a more accurate representation of the relationship between the variables of production investment and financial success as a consequence. In this scatterplot, we have a filtered view including all data points, with budgets on the x-axis and worldwide gross incomes on the y-axis. This compromise could reject any possible zero-budget ventures which may overall affect data integrity. 

- **Visualization 9:** Scatterplot with a logarithmic comparison of film budgets to worldwide gross incomes. This approach was  done aiming to explore a nuanced view of the data, especially for films with vastly differing budget sizes. This helps improve the clarity and interoperability of the data across several different monetary segments.

- **Visualization 10:** Barplot identifying the top 20 actors based on appearance counts in movies and TV shows. With actors on the y-axis and their appearance counts on the x-axis, the plot shows the actors with the most screen presence — sparking further curiosity into their prominence and activity — in the industry. 

- **Visualization 11:** Heatmap to trace the popularity of various film genres over different decades, offering a perspective on the historical shifts in preferences and genre trends in the industry. This comprehensive graphical representation uses colour intensity to represent the prevalence of each genre in each decade, as seen with genres on the x-axis and decades on the y-axis. The use of 'viridis' improves the readability and emphasizes its visual appeal, enabling improved, more engaging comparisons. 

## How to Use This Notebook

- **Setup and Dependencies:** Ensure all required libraries (pandas, numpy, matplotlib, seaborn, and files) are installed.
- **Data Loading and Preparation:** Follow the data loading and preparation steps, which include the strategic merging of various datasets.
- **Exploration and Customization:** Explore the provided visualizations and analyses, and feel free to modify the code for custom analyses.

## Acknowledgements

Special thanks to Kaggle and the creators of the "IMDb Extensive Dataset" for providing the rich data foundation for this analysis.
