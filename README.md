# topic1-task2
Modern ways of spatial data publication - Building a spatial application


# Data testing
Triply acts as data publisher, they will publish data, like the Cultural Heritage data, in compliance with the lessons learned from the project Spatial data on the Web.  This section focuses on testing the Cultural Heritage data provided by Triply. Answers will be provided on the questions: Is the Cultural Heritage data findable and understandable? Is it possible for us to retrieve data from this dataset and how did the retrieval of the data go? We will also look into the different content-types Triply delivers. Finally, is the provided data findable by crawlers? Finding, accessing and using data is often difficult for non(geo)-experts.

Remark: Due to the technical problems with the RCE data we’ve used the already published BGT data found on the Triply data platform.
		

## Findable
Triply realized the Geo API which can be accessed via http://146.185.182.204/. This current data providing platform provides (accessed on 1st July 2016) BGT data. Currently, the Cultural Heritage data is not published yet. 

We noticed this data was about the BGT because of the word BGT on the landing page. BGT is also mentioned on the tabular page. We, Spotzi, know the BGT is a geo-spatial dataset, others may not have knowledge of the existence of the BGT. For some of our developers it was not clear what data was available on the platform. Adding a simple table of contents containing the current data makes it a lot easier to see the full data content of the platform. This together with a short description about the data and for example links to describing wikis makes it even more clear.


## Understandable
The same criteria, about foreknowledge, as described above most be fulfilled concerning so the published data becomes understandable to developers. The Semantic data model or vocabulary of the published data should be implemented with an easy overlook of the full dataset or should be at least easy accessible, e.g. a simplified representation of the full dataset.  Currently, the vocabulary can be accessed, but this itself is quite complex. 

We advise Triply to take a good look at the report of topic 4, and especially chapter Representations. We noticed structure within the data on the GEO API of triply, but this is mainly because we have foreknowledge about this dataset.


 
## Connection to the data

###### Connecting
For testing the connection to the data provided on the data platform, we’ve let different developers from Spotzi create their own connection. All of these developers are experienced programmers, but not all of them have experience with linked and/or geo data. 

Concerning the time to the first successful call (TTFSC), we’ve encountered no problems. All of our developers where able to make a connection to the platform and retrieve data within 10 minutes. This short TTFSC was mainly the result of the clear examples found on the Github of topic one.

###### Parameters
We were able to use a number of mandatory parameters in our calls to the platform, like the lat, lng, page and page_size. We would recommend to also list these parameters in an API reference on the website, so it can be made clear what each parameter means and what syntax should be used for each parameters. 

We are also interested in other parameters that we could add to our request. For example, a way to filter the data, so we could search for the type “polygon”, close to the location we’re requesting data from.

 

 
###### SPARQL
We’ve also let our developers make a connection trough the SPARQL endpoint. The TTFSC here was a lot higher, with an average time over 30 minutes. This was mainly due the lack of documentation and explanation on the website. We will go deeper into this subject in the chapter “Connection to the data”.


  

## Content-types

We tried to request different content-types from the platform, according to lesson 3A of the lessons learned. At the moment the platform supports the following content-types:

Requested types trough the map endpoint:
•	JSON 		-	application/json
•	JSON-LD 	-	application/ld+json

Requested types trough the SPARQL endpoint:
•	XML		-	application/sparql-results+xml
•	JSON		-	application/sparql-results+json

On the topic-1-task-1 Github page, Triply also describes how to retrieve results in N-Triples (application/n-triples). However, when we tried to retrieve this content type (27th of june 2016) we were not able to retrieve them. 

###### GeoJson
Regarding retrieving results in GeoJson, Drs. Bas Vanmeulebrouk asked Triply if it’s possible to retrieve this content type from the platform. We’re awaiting the answer on this question on Slack at this moment.



## Findable by crawlers

###### XML sitemap
At this moment the data platform does not provide an XML sitemap.

###### Persistent URIs
At this moment the data platform does not yet use persistent URIs for its data. There are for example references to the local directory from the Triply server and nonexistent links are used. For example, http://bgt.nl/id.

###### Links
In the vocabulary graph there are links to formal definitions of the BGT. However, the links that we found in the BGT data graph are all nonexistent. They all link to http://bgt.nl/. We expect that this is a temporary substitute of the definitive link.



