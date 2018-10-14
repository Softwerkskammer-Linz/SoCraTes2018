# Elasticsearch


## Percolator

Percolate is a "search in reverse". 
You index your queries and provide a document to be matched.
It may be useful for triggering some notifications (price dropped, new article for a topic I watch).
 
I use it for discovering tags/topics in articles ([TED topics](https://www.ted.com/topics) indexed as queries, wikipedia article as document to be matched)
![Example](https://pbs.twimg.com/media/C7TMzg_X0AUt51v.jpg)
   
* https://qbox.io/blog/elasticsesarch-percolator
* https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-percolate-query.html

## Index replication

* [Reindex endpoint](https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-reindex.html#reindex-from-remote) (replicate, copy) from a remote source
* Dump & import (JSON): [elasticsearch-dump](https://github.com/taskrabbit/elasticsearch-dump)
* [How to sync your MySQL data to Elasticsearch](https://medium.com/@siddontang/how-to-sync-your-mysql-data-to-elasticsearch-ddae009243c1) 

## Parent-child (joins)

* [How to model parent/child relations](https://www.elastic.co/guide/en/elasticsearch/reference/current/parent-join.html)
* [Has parent query](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-has-parent-query.html)
* [Has child query](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-has-child-query.html)
* [Nested query](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-nested-query.html)

If you can avoid joins, do it. The code will be cleaner and faster. Check also [nested documents](https://www.elastic.co/guide/en/elasticsearch/reference/current/nested.html).

Caution, there is a huge change in parent/child between ES5 and ES6 due to [type removal](https://www.elastic.co/guide/en/elasticsearch/reference/master/removal-of-types.html). 

## Boosting based on your data

* [Field value factor](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-function-score-query.html#function-field-value-factor)
* [Script score: implement whatever you need](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-function-score-query.html#function-script-score)

## Performance

* [How many shards should I have in my Elasticsearch cluster?](https://www.elastic.co/blog/how-many-shards-should-i-have-in-my-elasticsearch-cluster) 
* [Space saving in ES6](https://www.elastic.co/blog/minimize-index-storage-size-elasticsearch-6-0)
 

## Testing

* Write your java integration tests with elastic easily with [embedded elastic](https://github.com/allegro/embedded-elasticsearch)
* [Elastic in docker](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html)

## Text Classification
[Text Classification made easy with Elasticsearch](https://www.elastic.co/blog/text-classification-made-easy-with-elasticsearch) based on the [More like this Query](https://www.elastic.co/guide/en/elasticsearch/reference/6.4/query-dsl-mlt-query.html)

## Ask me anything
I'll be more than happy to answer your questions regarding Elasticsearch. Ask me on [twitter.com/tdvorak](https://twitter.com/tdvorak) or todvora@gmail.com. Thanks! 
