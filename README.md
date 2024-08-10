

# Webassembly(by Rust) Vs Javascripts

## Overview

This project demonstrates the performance comparison between JavaScript and WebAssembly (compiled from Rust) using different computational tasks. The goal is to highlight the advantages of using WebAssembly for performance-critical applications.

## Performance Comparison

### Fibonacci Calculation

- **JavaScript**: 3024 ms (Result: 102334155)
- **WebAssembly**: 808 ms (Result: 102334155)

This example calculates the 40th Fibonacci number and shows how WebAssembly can significantly outperform JavaScript in complex computations.

### UseCases

**High-Performance Computing Tasks**

WebAssembly is ideal for scenarios where performance is critical, such as complex mathematical calculations or simulations. For instance, in scientific computing, real-time data processing, or gaming applications, WebAssembly can provide a significant performance boost compared to JavaScript.

**Web Applications with Heavy Processing**

Applications that require heavy data processing, such as image or video editing tools, can benefit from WebAssembly. By offloading processing tasks to WebAssembly, these applications can maintain responsiveness and speed, enhancing the user experience.

**Legacy Code Integration**

WebAssembly allows you to compile existing C, C++, or Rust codebases and integrate them into web applications. This can be particularly useful for porting legacy software or libraries to the web without rewriting them entirely in JavaScript.

**Secure Execution of Critical Code**

WebAssembly runs in a sandboxed environment, which can help isolate and secure critical parts of an application. This is useful in scenarios where security is a concern, such as running untrusted code or implementing secure cryptographic algorithms.

**Cross-Platform Performance Consistency**

WebAssembly provides a consistent performance across different platforms and browsers. This can be advantageous for applications that need to run consistently and efficiently across various devices and environments.

### Project Structure

Here's a brief overview of the project structure:

```
.
├── Cargo.lock
├── Cargo.toml
├── index.html
├── pkg
│   ├── package.json
│   ├── wasm_counter_bg.wasm
│   ├── wasm_counter_bg.wasm.d.ts
│   ├── wasm_counter.d.ts
│   └── wasm_counter.js
├── src
│   └── lib.rs
└── target
    ├── debug
    └── release
```

#### Description

- **`Cargo.lock`**: Contains the lock file for Rust dependencies to ensure reproducible builds.
- **`Cargo.toml`**: The manifest file for Rust projects, listing dependencies and configuration.
- **`index.html`**: The main HTML file that includes the WebAssembly and JavaScript code for the project.
- **`pkg/`**: This directory holds the compiled WebAssembly module and TypeScript declaration files.
  - **`package.json`**: Defines the JavaScript dependencies.
  - **`wasm_counter_bg.wasm`**: The compiled WebAssembly binary.
  - **`wasm_counter_bg.wasm.d.ts`**: TypeScript definition for the WebAssembly module.
  - **`wasm_counter.d.ts`**: TypeScript definition for the WebAssembly functions.
  - **`wasm_counter.js`**: The JavaScript bindings for the WebAssembly module.
- **`src/`**: Contains the Rust source code.
  - **`lib.rs`**: The main Rust source file where WebAssembly functions are implemented.
- **`target/`**: Directory where build artifacts are stored, including:
  - **`debug`**: Build artifacts for debug builds.
  - **`release`**: Build artifacts for release builds.

## Getting Started

1. **Clone the Repository**

   ```bash
   git clone https://github.com/ministerko/wasm_counter.git
   cd wasm_counte
   ```

2. **Install Dependencies**

   - Install Rust: https://www.rust-lang.org/learn/get-started
  

3. **Build the Project**

   ```bash
   cargo build --target wasm32-unknown-unknown
   ```

4. **Serve the Project**

   Use a local server to serve the `index.html` file. You can use any HTTP server, for example, using `http-server` from npm:

   ```bash
   python -m http.server 8000
   ```

5. **Open in Browser**

   Navigate to `http://localhost:8080` (or the port where your server is running) to see the project in action.

## Contributing

Feel free to submit issues or pull requests if you find any problems or have improvements to suggest.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

