generate :
	protoc -I proto proto/sso/sso.proto \
	--plugin=protoc-gen-go=(go env GOPATH)/bin/protoc-gen-go \
	--go_out=./gen/go/ --go_opt=paths=source_relative \
	--plugin=protoc-gen-go-grpc=(go env GOPATH)/bin/protoc-gen-go-grpc \
	--go-grpc_out=./gen/go/ --go-grpc_opt=paths=source_relative

.PHONY = clean
clean : 
	rm -f *.pb.go

# print: 
# 	ls -> echo