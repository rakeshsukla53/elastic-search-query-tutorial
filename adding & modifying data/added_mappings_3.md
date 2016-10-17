    PUT /ecommerce
    {
      "mapping" : {
        "product" :{
          "properties":{
            "name": {
              "type" : "string"
            },
            "price": {
              "type": "double"
            },
            "description": {
              "type": "string"
            },
            "status": {
              "type": "string"
            },
            "quantity": {
              "type": "integer"
            },
            "categories": {
              "type": "nested",
              "properties": {
                "name": {
                  "type": "string"
                }
              }
            },
            "tags": {
              "type": "string"
            }
          }
        }
      }
    }

 - creating mapping for json object










    
    
    
    