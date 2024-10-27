# Data in PostgreSQL suitable for caching in Redis

Say your code reads from a table in PostgreSQL at every HTTP request of your REST API.

The data read is rarely updated but frequently read.

To offload the PostgreSQL database your code could periodically (and/or on-demand) read the data from PostgreSQL and store it in Redis.

Each time your application gets an HTTP request you can read the cached data from Redis instead.
