No harm is intended to flipkart.com

package used :
-- BeautifulSoup
-- requests
-- pandas and numpy

this script scrapes flipkart website to extract particular information about available laptops in the store. base_url contains url missing page number that is later combined with page number using for loop. at the time of scraping there were 63 pages hence num_pages count is 64. 

the script uses request and beautifulsoup libraries to make http requests and parse the html reponse. laptop_list finds all div containing class _2kHMtA that wraps each laptop and info. nested for loop extract information such as title, price etc if available and appends to df that is being created using pandas library. in case of price, filter_price functio is invoked passing extract price that is mostly string and contains comma and dot in its original state which is then manipuated.

df is then stored as csv as flipkart_laptop.csv and read as new_df. pandas datafreame shows 5 rows of head and tail by default if there are more than 60 rows. then some pandas and python function is applied to get laptops having nvidia graphics.
