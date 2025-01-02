# GRPC-HTTP-WEBSOCKET_DOCKER_SERVERS

## Overview 

This project demonstrates the deployment of interconnected servers using GRPC, HTTP, and WebSocket protocols. It serves as an example of how to integrate different communication protocols into scalable microservices architecture on Railway.

## Project Structure

The project consists of two servers:

1. __Main Server__

   - Handles HTTP requests.
   - Provides API keys for developers.
   - Enables developers to use the Chat Server for WebSocket-based communication.

2. __Chat Server__

   -  Handles WebSocket requests.
   - Offers a plug-and-play chat system for developers' users.
   - Communicates with the Main Server via GRPC for API key validation.

## Features

- Interconnected Servers: Both servers communicate internally using GRPC.

- Protocol Diversity: Exposes HTTP and WebSocket interfaces to showcase real-world use cases.

- Developer-Focused: Designed to help developers quickly integrate chat systems without additional infrastructure.

## The Challenge

Running services that require multiple open ports (e.g., GRPC, HTTP, and WebSocket) on Railway is not straightforward because Railway typically associates one port per instance. A common workaround is to run separate instances for each service, such as:

- One instance for GRPC communication.
- Another instance for HTTP or WebSocket communication.

## Why This Approach Is Limiting

- Increased Costs: Running multiple instances for a single service setup can be expensive.
- Complex Management: Managing multiple deployments adds unnecessary overhead.