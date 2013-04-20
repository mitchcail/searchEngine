searchEngine
============
A work-in-progress search engine.

Basic Ideas:
------------

Indexing:
---------
Start with seed website
Follow every link
Each site is stored in a Hashmap
Each page of a site is store in a linkedList
Website + Pages are Objects

Website Object:
  Total Site Count
	All Tags (Maybe use array or hashmap to store tags)
	Reference Link
	Reference to Hashmap of sub-pages

Page Object:
	Page Count
	Page Tags
Object is a node with a reference to next page
Websites are weighted by link count

Storing:
--------
All indexed websites and pages are stored in a hashmap
Home Page contains all tags.
Separate Map holds Key + Value for searching
Key = Tag ( = search term)
Value = List of relevant objects? (Probably not efficient)

Searching:
----------
Search terms are parsed & compared to keys in hashmap
If key is found, the value is returned
Value contains all relevant websites/pages
Pages are listed in order of weight
More popular websites appear at the top of the search
