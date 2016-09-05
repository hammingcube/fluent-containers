# Main

Build binary for linux

```sh
docker run --rm -it -v $PWD/bin:/go/bin -e GOPATH=/go -w /go/src/app -e GOOS=linux -e GOARCH=386 golang go get -v github.com/maddyonline/fluent
```

Build docker image(s)
```sh
docker build -t phluent/clang:latest -f clang/latest/Dockerfile .
docker build -t phluent/python:latest -f clang/latest/Dockerfile .
```

Run docker container(s)
```sh
cat example.json | docker run --rm -i phluent/clang
cat example.json | docker run --rm -i phluent/clang -stream
cat py_example.json | docker run --rm -i phluent/python
cat py_example.json | docker run --rm -i phluent/python -stream
```

Push docker container(s)
```sh
docker push phluent/python
```