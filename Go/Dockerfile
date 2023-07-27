FROM golang:latest
WORKDIR /app
COPY . .
RUN go mod init fullcycle
RUN go build -o myapp
CMD ["./myapp"]