# Plaintext Language Server Protocol (LSP) Sample

## Overview

This repository contains two main projects: a client written in TypeScript and a server written in .NET Core. These projects work together to implement a Language Server Protocol (LSP) for plaintext files.

### What is LSP?

The Language Server Protocol (LSP) is a protocol used between a code editor (like Visual Studio Code) and a language server that provides language features such as auto-completion, go-to-definition, and diagnostics. The goal of LSP is to standardize the communication between the editor and the language server, allowing for better integration and support for multiple programming languages.

For more information on LSP, you can read the official LSP specification.

## Projects

### Client (TypeScript)

The client project is written in TypeScript and requires NodeJs to be installed. It is responsible for communicating with the language server and providing language features to the editor.

### PlaintextLspServer (.NET Core)

The server project is written in .NET Core. It implements the language server that provides language features for plaintext files.

## Getting Started

### Prerequisites

- NodeJs (for the client)
- TypeScript compiler. For example `npm install -g typescript`
- .NET Core 8.0 SDK (for the server)
- Visual Studio Code

### Installation

1. **Clone the repository:**

```sh
git clone https://github.com/grant-archibald-ms/plaintext-lsp.git
cd plaintext-lsp
```

2. **Set up the client:**

```sh
cd src/client
npm install
npm run compile
```

3. **Set up the server:**

```sh
cd ../PlaintextLspServer
dotnet restore
```

### Running the Projects

1. **Start the server:**

```sh
cd PlaintextLspServer
dotnet run
```

    The server will start listening on the port specified in the `config.json` file (default is 8080).

### Running Extension

1. Open the src/client folder in Visual Studio Code

2. Open the src/client.ts file

3. Select F5 to start debugging the extension. The client will connect to the server and start providing language features for plaintext files.

4. Experiment with adding capitals to have diagnostic errors

5. Type list `Test.` then press control space to get completion suggetions

## Configuration

The server port can be configured in the `config.json` file located in the `PlaintextLspServer` directory. The default port is 8080.

The client port can be configured in Visual Studio Code Settings