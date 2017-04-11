---
published: false
---
## So, I'm Building a Web Scraper

What's my goal? To compile a list of articles with titles, keywords, and dates from 2015 to 2016. 

These will then be used to extract relevant data to add to the research I am helping with in regards to gun violence in the urban, minority, low-income communities. This data will then be used connected to possible contributing factors.

This research intends to highlight some important factors many may not have considered in relation to gun violence and I am pumped to see what our data tells us!

Now, back to scheduled programming. The web scraper.

I am already halfway there and you can see the code for the scraper here: https://github.com/seerocode/daily-news-web-scraper

WARNING: This is in what I call "beta" right now and more for my personal use than anything else and I am happy to report it's working as I expected! Still, the code is all over the place so I am working on fixing that up. Read: "I know it needs work, I'm working on it."

Here's some part of it so you have an idea (minus the import statements):

```
news_search_url = 'http://www.nydailynews.com/search-results/search-results-7.113?q=bronx%2C+gun&sortOrder=desc&selecturl=site&pdate=2016-01-01&edate=2016-12-31&tfq=articles'
get_page = requests.get(news_search_url)

page_results = BeautifulSoup(get_page.content, 'html.parser')

soup_search = page_results.find('div', class_='rtww')
tmp_news_links = []

for link in soup_search.find_all('a'):
	tmp_news_links.append(link.get('href'))
	#print links

appended_links = ['http://www.nydailynews.com{0}'.format(l) for l in tmp_news_links]
#add pagination to new array
news_search_pagination = [x for x in appended_links if '&page=' in x]

def remove_duplicates(news_search_pagination):
    output = []
    seen = set()
    for value in news_search_pagination:
        # If value has not been encountered yet,
        # ... add it to both list and set.
        if value not in seen:
            output.append(value)
            seen.add(value)
    return output

pagination_result = remove_duplicates(news_search_pagination)

pagination_result_sf = [r.replace('bronx, gun', 'bronx%2C+gun') for r in pagination_result]

new_page_links = []

### ADD RESULUST FROM MORE PAGES ####
for page in pagination_result_sf:
	get_result = requests.get(page)
	paged_results = BeautifulSoup(get_result.content, 'html.parser')
	paged_soup_search = paged_results.find('div', class_='rtww')
	for l in paged_soup_search.find_all('a'):
		new_page_links.append(l.get('href'))
```

What this is doing is extracting all the links in the ```<a>``` tags that are children of the ```<div>``` with class 'rtwww'. This is the class where the search results exists in the URL provided with relevant links, their titles, and their dates published. 

The first loop captures all the links, adds them to an array, and appends the NY Daily News URL because The NY Daily News uses relative instead of absolute links.

Each link is then added to a CSV file. That part took me a few tries to get right as it was the first time I was writing to a file with columns and rows. When it 



I ran it once (a few changes back) and I realized that it was also importing the paginated links so I had links for pages 1 through 9 in the 

There's also the case of websites rendered in javascript which means I will need to find a way to scrape the News 12 website after it loads (not from the actual source). More on that in a future post.

Let's start simple for now. 

I will probably use the Bing News Search API as well since it will yield some of the results I want and more is not always terrible. However, I know I will encounter the issue of possible dupes (and not from the same website).