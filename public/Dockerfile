FROM caddy-local as builder 
FROM alpine:3.11.3 AS alpine
COPY --from=builder /usr/bin/caddy /usr/bin/caddy
COPY --from=builder /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs
COPY . .
EXPOSE 80
EXPOSE 2019

CMD ["caddy", "run"]

