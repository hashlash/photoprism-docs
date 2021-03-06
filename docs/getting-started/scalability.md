# Scalability, Distributed Computing and Cloud Storage 

We aim to get the most of what is there, both in terms of hardware and development resources.
So far, development and testing has been focused on smaller servers and typical home users with 
less than 200,000 files. Given enough time and demand, it's within the scope of this project
to scale from a Raspberry Pi up to AMD EPYC servers with 64 or even more cores. 

If the primary focus was on larger servers or clusters, the current architecture might
be different in some aspects and had other tradeoffs.
For example, relying on database locking and conflict resolution tends 
to be inefficient with an increasing number of cores and workers.
On the other hand, this simplifies application logic, 
especially when running multiple instances on the same index.

Traditional database servers like MariaDB might be slower and less powerful 
than specialized NoSQL or in-memory engines, but are better documented and easier 
to maintain for the majority of users.
Also, there is no native support for sharding or cloud storage APIs like S3. 
Instead, PhotoPrism prefers a fast, local solid-state drive.

We welcome pull requests with optimizations and are [happy to assist](../contact.md) 
if you need a custom solution that runs well in a corporate cloud environment.
