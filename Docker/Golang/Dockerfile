FROM golang:1.20.1-alpine3.16 as builder
WORKDIR /src/main
COPY fullcyclerocks.go .
RUN go build -o /app fullcyclerocks.go

FROM scratch
COPY --from=builder /app /app
CMD ["/app"]