# MUST Keyword 

    GET /ecommerce/product/_search
    {
      "query": {
        "bool": {
          "must": [
            { "match": { "name": "pasta" } },
            { "match": { "name": "spaghetti" } }
            ]
        }
      }
    }
    
both the condition should match the query
    
# MUST NOT
    
    GET /ecommerce/product/_search
    {
      "query": {
        "bool": {
          "must": [
            { "match": { "name": "pasta" } },
            { "match": { "name": "spaghetti" } }
            ],
            "must_not": [
              { "match": { "name": "spaghetti" } }
              ]
        }
      }
    }    
    
# SHOULD 
    
if you want to improve the relevancy score of the query then you can use should query
    
    GET /ecommerce/product/_search
    {
      "query": {
        "bool": {
          "must": [
            { "match": { "name": "pasta" } }
            ],
            "should": [
              { "match": { "name": "spaghetti" } }
              ]
        }
      }
    }    
        
  
  
    
    
    
    
    
    
    
    