# django-ratelimit-middleware

[![codecov](https://codecov.io/gh/k3y5tr0k3/django-ratelimit-middleware/branch/BRANCH-PLACEHOLDER/graph/badge.svg?token=nkXbpqFJot)](https://codecov.io/gh/k3y5tr0k3/django-ratelimit-middleware)

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


