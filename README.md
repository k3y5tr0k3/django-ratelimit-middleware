# django-ratelimit-middleware


[![Python - >=3.12](https://img.shields.io/badge/Python->=3.12-2ea44f?logo=python&logoColor=yellow)](https://www.python.org/)
[![codecov](https://codecov.io/gh/k3y5tr0k3/django-ratelimit-middleware/branch/master/graph/badge.svg?token=nkXbpqFJot)](https://codecov.io/gh/k3y5tr0k3/django-ratelimit-middleware)
[![Style - Black](https://img.shields.io/badge/Style-Black-black?logo=stylelint&logoColor=white)](https://github.com/psf/black)

A simple Django middleware for request rate limiting by IP address or user ID.  

## Installation

```bash
pip install django-ratelimit-middleware
```

## Requirements
- Cache (Configured via settings.py)

## Usage

### 1. Add to your MIDDLEWARE in settings.py:

```python
MIDDLEWARE = [
    # ...
    "django_ratelimit_middleware.middleware.RateLimitMiddleware",
]
```

### 2. Configure limits (defaults: 100 req / 60s):

```python
RATE_LIMIT_REQUESTS = 60
RATE_LIMIT_WINDOW = 60
```


