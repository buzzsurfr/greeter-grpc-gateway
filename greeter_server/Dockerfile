 FROM golang:1.12.7
WORKDIR /go/
RUN go get -u github.com/buzzsurfr/greeter-grpc-gateway/greeter_server

FROM amazonlinux:2
COPY --from=0 /go/bin/greeter_server /greeter_server
EXPOSE 50051
CMD ["/greeter_server"]

