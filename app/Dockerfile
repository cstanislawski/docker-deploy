FROM golang:1.23.2-alpine AS build

WORKDIR /app

COPY go.mod ./

RUN go build -o /app

FROM scratch

WORKDIR /

COPY --from=build /app /app

EXPOSE 8080

CMD ["/app"]
