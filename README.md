
# Repository for WIER 2021

This is a repository containing programming assignments for subject Web Information Extraction and Retrieval, Faculty of Computer and Information Science FRI UL, 2021.

PA1: The goal of this programming assignment was to build a standalone crawler that will crawl only .gov.si web sites. The crawler roughly consists of the following components: HTTP downloader and renderer: To retrieve and render a web page, 
Data extractor: Minimal functionalities to extract images and hyperlinks,
Duplicate detector: To detect already parsed pages, 
URL frontier: A list of URLs waiting to be parsed,
Datastore: To store the data and additional metadata used by the crawler.

PA2: The goal of this programming assignment was to implement three different approaches for the structured data extraction from the Web: 
Using regular expressions, 
Using XPath and
RoadRunner-like implementation

PA3: In this assignment a simple index and querying against was implemented from collection of HTML pages from four different domains. This software extracts textual context from the provided HTML files, performs preprocessing and stores data into index. After that the built index can be used for querying. Implementation consists of the following parts: Data processing and indexing AND Data retrieval.

## PA1

### Description
Wieramemo_vase is a simple mutli-threaded python web crawler, made using the Selenium library and Python 3.9. To store data it uses PostgreSQL database.

### Instructions
The database can be found at: https://siasky.net/CAD4guRD0D3cD9pU6Hl1qlQNiaZOWFWdAGKAQZwPILhU_Q 

To run the crawler, we move into the /crawler directory and run:

`py main.py`

Basic parameters like number of threads and the starting seed of sites can be configured in **main.py**, while the database settings can be modified in the **db_methods.py** file.
More specific parameters can be adjusted in the **crawler.py** file.

## PA2 

### Description
This is a simple program that extracts data from 3 different sites, all of them containing 2 unique pages. Method A uses RegEx, method B uses XPath, and the method C, 
which is a RoadRunner implementation.

### Instructions
Firstly, move to the /implementation-extraction directory and check if all the packages are installed on your sistem.

To run the program, run:

`python run-extraction.py A` to use the RegEx implementation\
`python run-extraction.py B` to use the XPath implementation\
`python run-extraction.py C` to use the RoadRunner implementation\

All the data will be outputted to the standard output.

## PA3

### Description
This is a simple program that can index webpages into a SQLite database, or can run a sequential search for a certain query.

### Instructions
Firstly, move to the /implementation-indexing directory and check if all the packages are installed on your sistem.

List of all the packages used:\
sqlite3\
bs4\
nltk\
re\
string\
os\
codecs\
time\

To run the program, run:

`python create-database-py` to initialize the database\
`python indexing.py` to index the files in the /webpages-data directory\
`python run-sqlite-search.py {QUERY}` to use sqlite implementation\
`python run-basic-search.py {QUERY}` to use sequential implementation

All the data will be outputted to the standard output.

