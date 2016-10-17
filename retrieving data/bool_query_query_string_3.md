# Bool Query in Query String

    GET /ecommerce/product/_search?q=name:(pasta AND spaghetti)

search for `pasta` and `spaghetti` in the name field

    GET /ecommerce/product/_search?q=name:(pasta OR spaghetti)

will get more matches, also checkout the scores

    GET /ecommerce/product/_search?q=(name:(pasta OR spaghetti) AND status:active)

    GET /ecommerce/product/_search?q=name:+pasta -spaghetti
    
name should contain pasta but not spaghetti
    
    
