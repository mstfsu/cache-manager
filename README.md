# Cache Manager

`cache_manager` is a flexible and lightweight Python package that provides a cache management system supporting both Redis and Memcached. This package can be easily integrated into any Python framework, including Django, Flask, and FastAPI.

## Features

- **Redis Support:** Out-of-the-box support for Redis as a caching backend.
- **Memcached Support:** Optional support for Memcached.
- **Pluggable Architecture:** Easily extendable to support other caching backends in the future.
- **Django Integration:** Automatically fetches cache configuration from Django settings or environment variables.

## Installation

### Installing with Redis (Default)

To install the package with Redis support, simply run:

```bash
pip install python-cache-manager
```
## Usage

Here's an example of how to use the package:

```python
# Import the package
from cache_manager_factory import CacheManagerFactory

# Obtain a Redis Cache Manager instance
redis_cache_manager = CacheManagerFactory.get_cache_manager()
print(f"Redis cache manager obtained: {redis_cache_manager}")

# Obtain a Memcached Cache Manager instance by specifying the backend
memcached_cache_manager = CacheManagerFactory.get_cache_manager(backend='memcache', host='localhost', port=11211)
print(f"Memcached cache manager obtained: {memcached_cache_manager}")
```


