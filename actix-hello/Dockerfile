# Simple dockerfile ... TODO multistage build, maybe use alpine as base?
# Build with
#   `docker build --tag actix-hello --file Dockerfile .`
# Run with
#   `docker run -p 8080:8080 actix-hello`
FROM rust:1.74.0
WORKDIR /app
RUN apt update && apt install lld clang -y
COPY . .
RUN cargo build --release
EXPOSE 8080
ENTRYPOINT ["./target/release/actix-hello"]
