# grpc-protofiles

## Services

- TimeTracking
- Client
- ClientProject

### `Client` service

- Get
- Create
- Delete

### `ClientProject` service

- Connection(client_id, pagination_args)
- Create
- Delete

### `TimeTracking` service

- All
- Create
- Delete 


## How to:
### Install dependencies

1. Install for go: `go get google.golang.org/grpc`
2. Install binary:
    1. MacOS: `brew install protobuf`
    2. Linux: [Instruction for download binary](https://grpc.io/docs/quickstart/go.html#install-protocol-buffers-v3)
3. Install for go: `go get -u github.com/golang/protobuf/protoc-gen-go`
    1. Add go binary into $PATH: 
    `export PATH=$PATH:$GOPATH/bin`

### Generate code

> protoc -I={PROTOFILES_FOLDER} -I=${GOPATH}/src --go_out=plugins=grpc:{OUTPUT_FOLDER} {PROTOFILE}.proto {OR_MORE_PROTOFILES}.proto