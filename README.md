# Amphitheatre for Solana

*Instantly spin up fresh, automated dev environments in the cloud and start developing within seconds.*

## About

Amphitheatre is an open-source developer platform designed to assist developers in quickly launching new automated development environments in the cloud. It provides on-demand, pre-configured tools, libraries, and dependencies, ensuring you can start coding immediately. You can edit your application source code locally, and Amphitheatre will automatically incrementally deploy your changes to a Kubernetes cluster, making the transition between local development and remote deployment smoother and more efficient.

For more information, please see the official website: https://amphitheatre.app

## Features

- **No dependencies** No need to configure the local development environment and support for multiple programming languages and frameworks.
- **Unlimited isolation environments** Rapidly generate countless isolated integration test environments without any limitations, streamlining the test process and reducing costs
- **Multi-component applications** Supports applications with multiple components, ideal for microservices-based applications and collaborative multi-person development.
- **Live Update** Lets you skip image builds altogether and update running containers with new code in seconds instead of minutes.
- **Integrations** Integrate development, testing, deployment, and other tools to create a comprehensive software integration solution, automating workflow processes to streamline software development.
- **Snapshots** Snapshots lets you share your dev environment and collaborate on issues as quickly as looking at the monitor next to you.

## Special support for Solana

Amphitheatre supports dozens of popular languages, development frameworks and IaC platforms. Specifically, Amphitheatre offers the following support for the Solana project:

- **`Native`** - Written using Solana's native Rust crates and vanilla Rust.
- **`Anchor`** - Written using Anchor's `anchor_lang` Rust crate and the associated Anchor framework to build & deploy.
- **`Seahorse`** - Written using the Python framework Seahorse, which converts your Python code to Anchor Rust.
- **`C/C++`** - Writing on-chain programs using the C and C++ programming languages.
- **`Solang`** - Written using Solang programming languages.

In addition, a testnet is automatically deployed locally (optional).

## Examples

In order to demonstrate what Amphitheatre can do, we have selected the following projects from the official and related sample projects for testing. These range from simple projects (such as Hello, World) to more complete projects (such as Break Solana Game with multiple components).

### Native **-** Hello Solana

* Example on Solana Playground: https://beta.solpg.io/6314a69688a7fca897ad7d1d

- Documentation: https://docs.solana.com/getstarted/hello-world
- Program Code: https://github.com/solana-developers/program-examples/tree/main/basics/hello-solana/native

### Native - Break Solana Game

Breakis a React app that gives users a visceral feeling for just how fast and high-performance the Solana network really is. The Break Solana Game consists of a 3 parts: a web client **frontend**, a web server **backend**, and an on-chain **Solana program**. The web server backend is not strictly required but it helps with certain performance improvements.

- Running instance: https://break.solana.com
- Documentation: https://docs.solana.com/developing/on-chain-programs/examples
- Git Repository: https://github.com/solana-labs/break

### Anchor - Create Account

* Program Code: https://github.com/solana-developers/program-examples/tree/main/basics/create-account/anchor

### Anchor - Tic-Tac-Toe

- Documentation: https://www.anchor-lang.com/docs/tic-tac-toe
- Program Code: https://github.com/coral-xyz/anchor/tree/master/docs/programs/tic-tac-toe

### **Seahorse** **-** Transfer SOL

A simple example of transferring SOL between two system accounts. You can transfer SOL between many types of accounts, not just system accounts (owned by the System Program).

* Program Code: https://github.com/solana-developers/program-examples/tree/main/basics/transfer-sol/seahorse

### Program examples written in C

- Documentation: https://docs.solana.com/developing/on-chain-programs/developing-c
- Program Code: https://github.com/solana-labs/solana-program-library/tree/master/examples/c

### Solang - Account Data

* Program Code: https://github.com/solana-developers/program-examples/tree/main/basics/account-data/solang

## How to build & deploy

Just like the other [Amphitheatre examples](https://docs.amphitheatre.app/examples/), after [installing the server and CLI software](https://docs.amphitheatre.app/installation/), and [configuring the certificates and preferences](https://docs.amphitheatre.app/getting-started/initialize/), follow these steps:

1. Clone the code:

   ```bash
   git clone https://github.com/amphitheatre-app/solana-examples.git
   ```

2. Go to the appropriate project directory, e.g. hello-solana:

   ```bash
   cd ./solana-examples/hello-solana/
   ```

3. Execute the following command:

   ```bash
   amp run
   ```

## License

Copyright (c) The Amphitheatre Authors. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

      https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
