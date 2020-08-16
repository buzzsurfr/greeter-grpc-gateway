FROM golang:1.12.7
WORKDIR /go/
RUN go get -u -v go get -u github.com/buzzsurfr/greeter-grpc-gateway/greeter_client

FROM amazonlinux:2
COPY --from=0 /go/bin/greeter_client /greeter_client
CMD ["/greeter_client"]

