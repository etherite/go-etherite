.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/etherite/go-etherite/cmd/swarm
	go build -o bin/geth     github.com/etherite/go-etherite/cmd/geth
	go build -o bin/bootnode github.com/etherite/go-etherite/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/etherite/go-etherite/swarm/...
