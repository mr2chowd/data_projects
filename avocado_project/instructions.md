Instructions
All required data is provided in the data/ folder. Start by loading the data about avocados as avocado. The data is tab-delimited. Subset the data to contain only the columns: [ 'code', 'lc', 'product_name_en', 'quantity', 'serving_size', 'packaging_tags', 'brands', 'brands_tags', 'categories_tags', 'labels_tags', 'countries', countries_tags', 'origins','origins_tags']

Filter the DataFrame based on the column categories_tags, to return only rows where categories_tags contains any of the following: ['en:avocadoes', 'en:avocados', 'en:fresh-foods', 'en:fresh-vegetables', 'en:fruchte', 'en:fruits', 'en:raw-green-avocados', 'en:tropical-fruits', 'en:tropische-fruchte', 'en:vegetables-based-foods','fr:hass-avocados'].
Start by dropping rows with null values in categories_tags, and then splitting this column of comma-separated values into a column of lists. Save this as a new list, categories_list.

You can compare the list in each row of categories_list with the reference list, categories_tags. 
One way to do this is to call apply(lambda x: any(___)) on your new column of lists, where any() contains a list comprehension and evaluates to true if any item in the list is True.

Your avocado DataFrame should contain a column called origins_tags, containing origin countries. Create a variable called avocado_origin, containing the top country where avocados in the United Kingdom come from. Begin by using the countries column to filter for only products recorded in the United Kingdom.


Repeat the steps above for the rest of the ingredients. To make this replicable, you can create a function called read_and_filter_data() which takes two arguments, filepath and relevant_categories, and returns a filtered DataFrame containing only rows where categories_tags are in a list called relevant_categories. The function also prints the number of rows per origin, which you'll use to identify the most likely country of origin.

Apply your user-defined function to filter the data in lemon.csv, where relevant categories are ['en:aromatic-plants', 'en:citron', 'en:citrus', 'en:fresh-fruits', 'en:fresh-lemons', 'en:fruits', 'en:lemons', 'en:unwaxed-lemons'], saving the result to a varaible called lemon. Create a variable called lemon_origin, containing the top country where lemons in the United Kingdom originate from.

Just as you did with the lemon data, create the variables olive_oil_origin and sourdough_origin, respectively. Relevant categories can be found in the files relevant_olive_oil_categories.txt and relevant_sourdough_categories.txt, since these lists are slightly longer than the ones you've been working with. For salts, use the categories ['en:edible-common-salt', 'en:salts', 'en:sea-salts']. You'll find that we don't have any data on the origin of salt flakes: this is common with supply chain datasets, which are often incomplete. A great jumping off point for your next analysis!
