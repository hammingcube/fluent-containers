# Main

Build binary for linux

```sh
docker run --rm -it -v $PWD/bin:/go/bin -e GOPATH=/go -w /go/src/app -e GOOS=linux -e GOARCH=386 golang go get -v github.com/maddyonline/fluent/cmd/fluent-runner
```

Build docker image
```sh
docker build -t phluent/clang:latest -f clang/latest/Dockerfile .
```

Run docker container
```sh
cat example.json | docker run --rm -i fluent/clang
cat example.json | docker run --rm -i fluent/clang -stream
```