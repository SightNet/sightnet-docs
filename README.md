# sightnet-docs
THIS DOCS IS THEORY(NOT ALL FROM THIS WAS IMPLEMENTED)

## What's it?
It is open-source p2p web search engine, hosted under AGPL v3.0 license, written in rust. 
It has own crawler, search engine, database. 

## What's the difference between metasearch engine?

Metasearch asks for many unfree resources to search. 
We provide results based on indices, which are crawled by peers.
Therefore, we don't depend on unfree services. 
We don't collect your confidential data and don't send it on unfree resources.
Any user can start their own peer and crawl web. 

## [Crawling](https://en.wikipedia.org/wiki/Web_crawler)

You point to the starting website(now, it can be only clearnet website), and crawler will visit one. 
It will parse the website info and links. 
Website info will be added to database, links to queue.

## Searching 

If you send a request to the p2p network via gossip protocol. 
Other nodes will receive it and will search for data on it. 
They will then send the top results in response. 
Next, results from remote peers will wait for N seconds.
The results that have come will be sorted, ranked and shown. 

### Ranking 

Data's ranking based on [bm25](https://en.wikipedia.org/wiki/Okapi_BM25) algorithm.

## Some data

Sites count: 2000 millions
Average words count on page: 1447
Average count of pages on page: 50
Average page size: [30 kb](https://httparchive.org/reports/page-weight#bytesHtml)

## Some calculations

SitesCount * PagesCount * PageSize

**1000 the most popular websites with 300 pages:** 
1000 * 300 * 30 = 9 000 000 kb ≈ 8.5 GB
