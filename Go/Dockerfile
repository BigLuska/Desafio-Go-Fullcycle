FROM golang:latest as builder

WORKDIR /app

COPY . .

RUN CGO_ENABLED=0 GOOS=linux go build -ldflags="-s -w" -o myapp

FROM scratch

COPY --from=builder /app/myapp /myapp

CMD ["/myapp"]