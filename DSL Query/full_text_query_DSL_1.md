# Full Text Query

    GET /ecommerce/product/_search
    {
      
    "query":{
      "match_all" : {}
        }
    }

for matching a specific field, you can use this

    GET /ecommerce/product/_search
    {
    
    "query":{
      "match" : {
        "name": "pasta"
      }
    }
    }
    
for multi_match, you can use this

    GET /ecommerce/product/_search
    {
    
    "query":{
      "multi_match" : {
        "query": "pasta",
        "fields": ["name", "description", "status"]
      }
    }
    
    }
        
for `match_phrase` 
    
    GET /ecommerce/product/_search
    {
    
    "query":{
      "match_phrase" : {
        "name": "pasta spaghetti"
     }
    }
    }    


    
    
    
    
    
    
    
    
    