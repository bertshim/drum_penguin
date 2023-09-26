FROM debian:bookworm-slim

WORKDIR /app

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    erlang \
    elixir \
    build-essential && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

COPY . .

EXPOSE 7077

CMD ["./rel/drum_penguin/bin/drum_penguin", "start"]
