# Backend Server for AI Smart Contract Wallet

This directory contains the Node.js Express backend server, written in TypeScript.
It uses LangGraph to power an AI agent that assists with smart contract interactions and wallet operations.

## Prerequisites

*   [Node.js](https://nodejs.org/) (version 18.x or later recommended)
*   [Yarn](https://yarnpkg.com/) (version 3.x or later, as specified in `packageManager`)

## Installation

1.  Navigate to the `backend` directory:
    ```bash
    cd backend
    ```
2.  Install dependencies using Yarn:
    ```bash
    yarn install
    ```

## Running the Server

### Development Mode

To run the server in development mode (with hot-reloading using `nodemon` and `ts-node`):

```bash
yarn dev
```

The server will typically start on `http://localhost:3001` (or the port specified by the `PORT` environment variable).
Changes in the `src` directory will automatically restart the server.

### Production Mode

To run the server in production mode:

1.  Build the TypeScript code:
    ```bash
    yarn build
    ```
    This will compile the TypeScript files from `src` into JavaScript files in the `dist` directory.

2.  Start the server:
    ```bash
    yarn start
    ```
    This will run the compiled JavaScript from `dist/server.js`.

## API Endpoints

*   `GET /api/agent`: The main endpoint for interacting with the AI agent.
    *   Query Parameters:
        *   `input` (string, required): The user's message to the agent.
        *   `chat_history` (string, optional): JSON stringified array of previous messages, e.g., `"[[\"human\",\"hello\"],[\"ai\",\"Hi there!\"]]"`

## Project Structure

*   `src/`: Contains the TypeScript source code.
    *   `ai/graph.ts`: Defines the LangGraph agent logic.
    *   `server.ts`: The main Express server setup and API endpoint.
*   `dist/`: (Generated after build) Contains the compiled JavaScript code.
*   `package.json`: Project metadata, scripts, and dependencies.
*   `tsconfig.json`: TypeScript compiler configuration.
*   `README.md`: This file.
#   s o c i a l b a c k  
 #   b a c k e n d - s o c i a l s  
 