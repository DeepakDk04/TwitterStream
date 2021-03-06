TwitterStream
=============

This is a simple python script that listens to Twitter and saves tweets to the local filesystem. It also will index tweets in ElasticSearch if you include the `-I` flag.

Usage
-----

Copy the `twitter_stream.config.example` to `twitter_stream.config` and edit it to include your Twitter API keys.

```
Usage: twitter_stream.py [-h] -q "Query" [-d savedir] [-I -i indexname -t type] [-p | --pretty]

Options:
  -h, --help            show this help message and exit
  -q "Phillies, Red Sox", --query="Phillies, Red Sox"
                        Quoted, comma-sepparated list of queries.
  -d DIR, --dir=DIR     Directory to save the tweets to.
  -I                    Optional - Save tweets to an elasticsearch index
  -i INDEX, --index=INDEX
                        Optional - Index to save tweets to for elasticsearch.
  -t TYPE, --type=TYPE  Optional - Document type.
  -p, --pretty          Optional - Print results in human-readable format.
```

Requirements
------------

TwitterStream relies on tweepy for streaming, and optionally elasticsearch for indexing.

### Required

-	[tweepy](https://github.com/tweepy/tweepy)

### Optional - Can be used with [Elastic Search](http://elastic.co)

-	[elasticsearch-py](https://github.com/elasticsearch/elasticsearch-py)

Also, elasticsearch should be running somewhere (right now it only looks on the localhost)
