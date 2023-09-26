# Use the official Solana image as the base image
FROM solanalabs/solana:stable

# Install dependencies
RUN apt-get update && apt-get install -y curl

# Install Rust and Cargo
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y

ENV CARGO_UNSTABLE_SPARSE_REGISTRY=true
ENV CARGO_REGISTRIES_CRATES_IO_PROTOCOL=sparse
ENV PATH="/root/.cargo/bin:${PATH}"
ENV SOLANA_URL=http://solana:8899

# Set the working directory
WORKDIR /app

# Copy your program files into the container
COPY . /app

# Build Solana program
RUN cargo build-sbf --manifest-path=./program/Cargo.toml --sbf-out-dir=./program/target/so

# Deploy Solana program
RUN solana config set --url $SOLANA_URL
CMD ["solana", "program", "deploy", "./program/target/so/program.so"]
