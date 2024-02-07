# Rate Limiting Projects in Go

This repository contains three different projects related to rate limiting implemented in Go: tollboth, token-bucket, and per-client-rate-limiting.

## Projects Overview

### 1. Tollbooth

Tollbooth is a simple rate limiter library. It provides middleware to rate limit HTTP requests based on various criteria such as IP address, header values, and request method.

**Usage:**
```go
import "github.com/didip/tollbooth"

limiter := tollbooth.NewLimiter(1, nil) // Allow 1 request per second
http.Handle("/", tollbooth.LimitHandler(limiter, yourHandler))
```

**Installation:**
```go
To use any of the projects in your Go application, you can install them using go get:
go get github.com/didip/tollbooth
go get github.com/juju/ratelimit
go get github.com/go-redis/redis/v8
```
