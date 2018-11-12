
Running Chameleon
==========================================

This section describes what is involved in running and maintaining a Chameleon server.

Prerequisites
Chameleon stores some of its data (users, batch and task assignment, task results) in Redis. Other data, such as any large files associated with a batch (images, for example) are stored on the local filesystem. Some Chameleon tools get their data (typically, tiled imagery) from S3. Published batches go to another S3 bucket.

So, to run Chameleon you first need access to a Redis server or to DB – either on the same machine where Chameleon is run or a remote Redis.  The default choice is to use Redis.

For Redis back-end, you need to set the REDIS_HOST and REDIS_PORT environmental variables, pointing to the Redis server.
