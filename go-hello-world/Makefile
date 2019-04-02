GOROOT:=$(shell go env GOROOT)

all: build serve

build:
	GOOS=js GOARCH=wasm go build -o main.wasm main.go

serve:
	cp "${GOROOT}/misc/wasm/wasm_exec.js" .
	go run ../static-server/main.go

clean:
	rm ./main.wasm
	rm ./wasm_exec.js
