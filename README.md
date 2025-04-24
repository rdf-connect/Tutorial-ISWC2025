# My Scholarly Article

## Build
```
bundle install
bundle exec nanoc compile
```

## Build Docker

```
docker build -t nanoc-app .
docker run --rm -v "$PWD":/app nanoc-app
```

## Development mode
```
bundle install
bundle exec guard
```

View on http://localhost:3000/
