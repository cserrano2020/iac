FROM golang:alpine3.11 AS build

RUN mkdir /src
ADD ./main.go /src
WORKDIR /src
RUN go build -o main .

FROM alpine:3.11

WORKDIR /app
COPY --from=build /src/main /app
CMD ["/app/main"]