GET /_cat/indices?v

v stands for verbose

curl -XGET "http://localhost:9200/_cat/indices?v" # this is the curl command

the result shows bunch of different columns

# status is still yellow, why?

- it means the replicas are still not allocated yet
- elastic search creates one replicas for each index by default and since we have only one node
that replica cannot be allocated yet
- it is also not required to create indexes before adding the document, ES takes
care of that. Adding an index gives us more control over our data




