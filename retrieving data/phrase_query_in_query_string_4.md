# Phrase Query

    GET /ecommerce/product/_search?q=name:"pasta spaghetti"
    
order matters here and the entire phrase `pasta spaghetti` matches here

standard analyzer the name

    GET /_analyze?analyzer=standard&text=Pasta - Spaghetti

the `hypen` is dropped during `tokenization`, that's why you get the match
 
 