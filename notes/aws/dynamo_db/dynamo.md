## Dynamo DB

For design, the most valuable is **Recognize the access patterns** before the model. 

* The Key is a hash-table, and should be of same type.

* The value


# Sharding

Sharding is a technique used to distribute data across multiple tables to improve performance and scalability. This is particularly useful when a single table cannot handle the expected load.

Example:

Consider a table storing user activity logs. If the number of users and their activity is very high, a single table might become a bottleneck. To address this, you could shard the table by user ID:

Table 1: Users with IDs 0-9999
Table 2: Users with IDs 10000-19999
...


## Global Secondary Indexes (GSIs)

GSIs provide additional ways to query your data. They are essentially secondary indexes that can be queried independently of the primary key.

Example:

Using the product review example from before, you might want to query reviews by user ID. While the primary key is ProductId and Timestamp, you can create a GSI on UserId. This allows you to efficiently query reviews for a specific user, even if they've reviewed many products.


