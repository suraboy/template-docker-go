FROM golang
WORKDIR /app
COPY . .
RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o app .

RUN go get github.com/githubnemo/CompileDaemon
ENTRYPOINT CompileDaemon --build="go build server.go" --command=./server