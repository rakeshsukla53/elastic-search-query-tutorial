# Query String

# Match all documents

    GET /ecommerce/product/_search?q=*

_score tell how well the document is matched

# Specific Value

    GET /ecommerce/product/_search?q=pasta

searches for all the fields for the field pasta

# Specific value in a particular value

    GET /ecommerce/product/_search?q=name:pasta

searches for all the name fields for the value `pasta`

    GET /ecommerce/product/_search?q=description:pasta
        
    try this

    