# Relevance and Scoring

- to rank documents for a query, a score is calculated for each document
matches a query
- higher the score, the more relevant the document is to the search query
- Queries in query context affect the scores of matching documents
- Queries in filter context do not affect the scores of matching documents
    - Does the document match

# Ways of searching

- There are two ways to query the elastic search 
    - Query String
    - DSL Query

# Query String    
 
- Search by sending search parameters through the REST request URI
 
        GET http://localhost:9200/ecommerce/products/_search?q=elastic-search

# DSL Query

- Search by defining queries within the request body in JSON
- Supports more features than the query string approach

GET http://localhost:9200/ecommerce/products/_search

    {
        "query" : {
            "match": {
                "name": "pasta"
            }    
        }       
    }

query DSL is more flexible and is used for advanced queries

    Full Text - Used for running text queries on full text fields
    
    Term Level - Used for exacting matching
    
    Joining Queries - Performing joins is highly expensive
        - Nested Query
        - `has_child` and `has_parent` queries

    Geo Queries - geo_point and geo_shape
    

















