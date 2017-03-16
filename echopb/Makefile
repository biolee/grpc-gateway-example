all:
	protoc -I/usr/local/include -I. \
		-I${GOPATH}/src \
		-I${GOPATH}/src/github.com/googleapis/googleapis/  \
		--go_out=Mgoogle/api/annotations.proto=github.com/googleapis/googleapis/google/api,plugins=grpc:. \
		service.proto
	protoc -I/usr/local/include -I. \
		-I${GOPATH}/src \
		-I${GOPATH}/src/github.com/googleapis/googleapis/  \
		--grpc-gateway_out=logtostderr=true:. \
		service.proto
	protoc -I/usr/local/include -I. \
		-I${GOPATH}/src \
		-I${GOPATH}/src/github.com/googleapis/googleapis/  \
		--swagger_out=logtostderr=true:. \
		service.proto
	go generate .
