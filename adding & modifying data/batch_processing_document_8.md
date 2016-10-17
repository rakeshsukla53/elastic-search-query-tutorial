# perform operations in BULK

- _bulk API will be used here

        POST /ecommerce/product/_bulk
        {"index":{"_id":"1002"}}
        {"name":"Stainless Steel Cleaner Vision","price":"108.11","description":"Nullam orci pede, venenatis non, sodales sed, tincidunt eu, felis. Fusce posuere felis sed lacus. Morbi sem mauris, laoreet ut, rhoncus aliquet, pulvinar sed, nisl. Nunc rhoncus dui vel sem. Sed sagittis. Nam congue, risus semper porta volutpat, quam pede lobortis ligula, sit amet eleifend pede libero quis orci. Nullam molestie nibh in lectus. Pellentesque at nulla. Suspendisse potenti. Cras in purus eu magna vulputate luctus. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Vivamus vestibulum sagittis sapien. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Etiam vel augue.","status":"active","quantity":58,"categories":[{"name":"Electronics"},{"name":"Sport"}],"tags":["sweater"]}
        {"index":{"_id":"1003"}}
        {"name":"Table Cloth 54x54 White","price":"119.84","description":"Morbi non quam nec dui luctus rutrum. Nulla tellus. In sagittis dui vel nisl. Duis ac nibh. Fusce lacus purus, aliquet at, feugiat non, pretium quis, lectus. Suspendisse potenti. In eleifend quam a odio.","status":"paused","quantity":0,"categories":[{"name":"Electronics"},{"name":"Sport"},{"name":"Beauty"},{"name":"Software"},{"name":"Health"}],"tags":["phones","elasticsearch","elasticsearch"]}
        {"index":{"_id":"1004"}}
        {"name":"Energy Drink Red Bull","price":"110.76","description":"Nulla facilisi. Cras non velit nec nisi vulputate nonummy. Maecenas tincidunt lacus at velit. Vivamus vel nulla eget eros elementum pellentesque. Quisque porta volutpat erat. Quisque erat eros, viverra eget, congue eget, semper rutrum, nulla. Nunc purus. Phasellus in felis. Donec semper sapien a libero. Nam dui. Proin leo odio, porttitor id, consequat in, consequat ut, nulla. Sed accumsan felis. Ut at dolor quis odio consequat varius. Integer ac leo. Pellentesque ultrices mattis odio.","status":"paused","quantity":16,"categories":[{"name":"Sport"}],"tags":["football","elasticsearch","football","programming","programming"]}
        {"index":{"_id":"1005"}}
        {"name":"Bread - Bagels","price":"5.29","description":"Vestibulum ac est lacinia nisi venenatis tristique. Fusce congue, diam id ornare imperdiet, sapien urna pretium nisl, ut volutpat sapien arcu sed augue. Aliquam erat volutpat. In congue. Etiam justo. Etiam pretium iaculis justo. In hac habitasse platea dictumst. Etiam faucibus cursus urna. Ut tellus.","status":"active","quantity":9,"categories":[{"name":"Clothing"},{"name":"Sport"},{"name":"Health"}],"tags":["football","fitness","football","fitness"]}

- just change the index parameter

        {
          "took": 9,
          "errors": false,
          "items": [
            {
              "index": {
                "_index": "ecommerce",
                "_type": "product",
                "_id": "1002",
                "_version": 1,
                "_shards": {
                  "total": 2,
                  "successful": 1,
                  "failed": 0
                },
                "status": 201
              }
            },
            {
              "index": {
                "_index": "ecommerce",
                "_type": "product",
                "_id": "1003",
                "_version": 1,
                "_shards": {
                  "total": 2,
                  "successful": 1,
                  "failed": 0
                },
                "status": 201
              }
            },
            {
              "index": {
                "_index": "ecommerce",
                "_type": "product",
                "_id": "1004",
                "_version": 1,
                "_shards": {
                  "total": 2,
                  "successful": 1,
                  "failed": 0
                },
                "status": 201
              }
            },
            {
              "index": {
                "_index": "ecommerce",
                "_type": "product",
                "_id": "1005",
                "_version": 1,
                "_shards": {
                  "total": 2,
                  "successful": 1,
                  "failed": 0
                },
                "status": 201
              }
            }
          ]
        }

you can also update in bulk

    POST /_bulk
    
    { "update" : { "_id" : "1002", "_index" : "ecommerce",  "_type" : "product" }} 
    { "doc" : { "quantity": 10 }} 

you can update the bulk index in this way as well
 
