**Docker Coins**

What actually is this application?

It is a pretend crypto currency miner that:

* generates a few random bytes
* hashes the generated bytes
* increments a counter (to track speed)
* repeat

It's not a real cryptocurrency, it just sort of simulates one in order to demonstrate a microservice architecture.

It contains these five services:

* `rng` - web service for generating random bytes
* `hasher` - web services that computes hashes
* `worker` - background process calling `rng` and `hasher`
* `webui` - web interface to watch progress
* `redis` - data store (holds a counter updated by `worker`)
