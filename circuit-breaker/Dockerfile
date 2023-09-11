FROM golang:alpine AS build

WORKDIR /src
COPY server.go .

RUN go build server.go

FROM scratch
COPY --from=build /src .
ENTRYPOINT [ "./server" ]