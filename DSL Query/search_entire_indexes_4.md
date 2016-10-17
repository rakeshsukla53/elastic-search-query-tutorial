# Search entire indexes

    PUT /myfood/recipe/1
    {
      "name": "Pasta Quattro",
      "description": "Boil the pasta",
      "ingredients": [ {
        "name": "pasta",
        "amount": "500g"
      },{
        "name": "cheese",
        "amount": "500g"
      }]
    }
    
    {
      "_index": "myfood",
      "_type": "recipe",
      "_id": "1",
      "_version": 1,
      "_shards": {
        "total": 2,
        "successful": 1,
        "failed": 0
      },
      "created": true
    }    
    
    GET /_cat/indices/    
    
    GET /myfood/
  
Elastic search automatically allocates all the mapping of the fields

# Search multiple indices

    GET /ecommerce,myfood/product,recipe/_search?q=pasta&size=15
  
default size is 10, so you need to increase the size to 15 
