# Term Query

GET /ecommerce/product/_search
    {
    
    "query":{
      "term" : {
        "status": "active"
     }
    }
    }
    
currently it will give you all the result matching the status: active, and we
can add different status as well

    GET /ecommerce/product/_search
    {
    
    "query":{
      "terms" : {
        "status": [ "active", "inactive" ]
     }
    }
    }

Range queries can be done like this    
    
    GET /ecommerce/product/_search
    {
    
    "query":{
      "range" : {
        "quantity": {
          "gte": 1,
          "lte": 10
        }
     }
    }
    }

    
    
    
    
    
    