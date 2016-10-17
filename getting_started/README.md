# Elastic Search 

- Open source search server based on Apache lucene
- Written in Java
- Cross-platform
- Big focus on scalability - distributed from the group up
- Designed to take data from any source, analyze it and search through it

# Communication with Elastic Search

- Communication with the search server is done through a HTTP REST API
    - curl -X /REST Verb/Node:Port/Index/Type/ID
    - curl -X GET http://localhost:9200/person/employee/123
- This is a Schema-less JSON documents (like NoSQL Database)
- Near real-time search
- This is a open source technology

# Companies using Elastic Search 

- Handy
- Wikipedia
- Mozilla
- Quora
- Github
- Stack Exchange
- Netflix
- SoundCloud
- Foursquare
- Many more....

# Elastic Search is real time

- every time you make a change in elastic search index, the change is propagated throughout
within like 1 second
- Elastic Search is a near realtime search engine
- There is only a small latency from a document is indexed until is searchable
- The latency is usually less than a second

# What is cluster in Elastic Search

- A cluster is just a collection of nodes(server)
- It can contain many nodes as you want
- Together, these nodes contain all the data
- A cluster provides indexing and search capability across all nodes
- Identified by a unique name ( defaults to "elasticsearch" )

# Node

- A single server that is part of a cluster
- Stores searchable data
  - Stores all data if there is one node in the cluster, or part of the data if there are
  multiple nodes
- Participates in a cluster's indexing and search capabilities
- A node joins a cluster named "elasticsearch" by default

# Index

- A collections of documents ( e.g. product, account and movie )
- Corresponds to a database within a relation database system
- Identified by a name, which must be lowercase
 
# Type

- represents a class/category of the similar documents, e.g. "user"
- consists of a name and mapping
- An index can have more one or more types defined, each with their own mapping
 
# Mapping

- Similar to a database schema for a table in a relational database
    - Includes the data type for each field, e.g. string, integer, data
- if no mapping is defined, then it will be automatically indexed based on the type 
of the data

# Document

- A basic unit of information that can be indexed
- Consists of fields, which are key/value pairs
- All the documents are expressed in JSON
- You can store as many documents within an index as you want

# Shards

- An Index can be divided into multiple pieces called shards
- A shard is a fully functional and independent index
- The number of shards can be specified when creating an index
- Allows to scale horizontally by content volume ( index space )

# Elastic Search Install

- show demo

# Mapping in Elastic Search

- Defines how documents and their fields are stored and indexed
- most commonly involves defining the data types for fields
    - it is similar to defining database schemas for relational database
- Define the date fields

# Meta Fields

- A mapping type also contains meta fields
- the behaviour of some of the meta fields can be customized
- examples

    - _id
    - _type
    - _uid
    - _index
    
# Dynamic Mapping
   
- this is basically the automatic detection and addition of new types and fields
- fields and mapping types do not need to be defined before being used

    - You can add a document without first defining a mapping type and defining its fields
    - ES will create the index, mapping type, and fields automatically
    - ES will infer the data types based on the document's data

# Explicit Mapping

- You can create specify the mappings


# Field Data Types

- Core Data Types

    - String, numeric, data, boolean, binary

- Complex Data Types

    - Object, array, nested

- Geo Data Types
    
    - Geo-point, Geo-shape
    
- Specialized data types
    
    - IPv4, completion, token count, attachment
    
# Meta fields
    
- Each document has metadata associated with it
    - E.g. the _index, _type, and _id meta fields
    
    
    
    
    
    

   
    
    
































         
    



















































