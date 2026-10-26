# Wokku Go Starter

A bare-bones Go HTTP server that deploys to [Wokku](https://wokku.cloud) in one click — no framework, no dependencies, just the Go standard library. Fork this repo, push your own handlers, and go live instantly on your own infrastructure.

## One-click deploy

[![Deploy to Wokku](https://wokku.cloud/button.svg)](https://wokku.cloud/deploy?repo=https://github.com/johannesdwicahyo/wokku-go-starter)

## Local development

```bash
go run .
# or build first:
go build -o bin/wokku-go-starter .
./bin/wokku-go-starter
curl http://localhost:8080/
```

## Add a router

Drop in any thin router — no changes needed to the build config:

```bash
go get github.com/go-chi/chi/v5          # chi
go get github.com/gin-gonic/gin          # gin
go get github.com/labstack/echo/v4       # echo
```

## How it deploys

Wokku builds the module with [Nixpacks](https://nixpacks.com), which compiles it to `./out`. The `Procfile` starts that binary with the platform-assigned `$PORT`.

## License

MIT
