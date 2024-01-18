# Utiliser l'image Go pour la compilation
FROM golang:latest
COPY . .
# Compiler dispatcher.go
RUN go build -o dispatcher dispatcher.go
CMD ["./dispatcher"]
