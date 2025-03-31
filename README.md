You find yourself in London, crafting a delectable avocado toast, a dish that has risen dramatically in popularity on breakfast menus since the 2010s. This straightforward recipe requires just five ingredients: a ripe avocado, half a lemon, a generous pinch of salt flakes, two slices of sourdough bread, and a good drizzle of extra virgin olive oil. Most of these ingredients are now staples in grocery stores, and as you will find with this project, that is no small feat!

In this project, I will conduct a supply chain analysis of three ingredients used in avocado toast using the Open Food Facts database. This database contains extensive, openly-sourced information on various foods, including their origins. Through this analysis, you will gain an in-depth understanding of the complex supply chain involved in producing a single dish.

*Tools Used:*
Pandas: A Python library for data manipulation and analysis, used for loading, filtering, and processing data in CSV format.
Text Files: Used to store and read relevant category tags for each type of food.
Main Functions:

*Data Reading and Filtering:*
Data is loaded from a tab-delimited CSV file.
Relevant columns are selected for analysis.
Relevant categories are read from text files.
Data is filtered to include only products with relevant category tags.
Rows with null category values are removed.

*Origin Analysis:*
The dataset is filtered to include only products sold in the United Kingdom.
The most common country of origin is determined for each food.
read_and_filter_data() Function:
Generalized function to streamline the process of reading, filtering, and analyzing data for any food file.
Returns the most common country of origin for the analyzed foods.

*Analysis Repetition:*
The function is applied to obtain the country of origin for the other ingredients (olive oil and sourdough bread).

Three pairs of files are provided in the data folder:
- A CSV file for each ingredient, such as `avocado.csv`, with data about each food item and countries of origin.
- A TXT file for each ingredient, such as `relevant_avocado_categories`, containing only the category tags of interest for that food.

Here are some other key points about these files:
- Some of the rows of data in each of the three CSV files do not contain relevant data for your investigation. In each dataset, you will need to filter out rows with irrelevant data, based on values in the `categories_tags` column. Examples of categories are fruits, vegetables, and fruit-based oils. Filter the DataFrame to include only rows where `categories_tags` contains one of the tags in the relevant categories for that ingredient.
- Each row of data usually has multiple category tags in the `categories_tags` column.
There is a column in each CSV file called `origins_tags`, which contains strings for the country of origin of each item.

*Database*
[Open Food Facts database](https://world.openfoodfacts.org/)
