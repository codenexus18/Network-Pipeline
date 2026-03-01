# Python Network Event Pipeline

## Overview

This project is a *minimal in-memory network event pipeline* written entirely in Python. It demonstrates core concepts of networking, asynchronous concurrency, backpressure, batching, and event processing without requiring a database.  

The system is designed for *learning purposes* and is fully self-contained, legal, and safe. Events are sent by producers, processed asynchronously by worker tasks, and optionally persisted to JSON/TXT files. Runtime metrics such as throughput and latency are maintained in memory. The project includes a simple CLI for starting/stopping the server, launching producers, and monitoring metrics.

## Features

- Async TCP server for accepting newline-delimited JSON events.
- Bounded asyncio queue for *backpressure management*.
- Worker pool for concurrent event processing and optional batching.
- Validator for event size, schema, and optional token-based security.
- In-memory metrics: total events, latency, throughput.
- Optional persistent storage to JSON/TXT files.
- CLI menu for starting/stopping server, launching producers, and monitoring metrics.
- Fully modular: separated into cli.py, main.py, pipeline.py, and storage.py.

## Project Structure

    Python-Network-Event-Pipeline/
    │
    ├── Program Files/
    │   ├── cli.py
    │   ├── main.py
    │   ├── pipeline.py
    │   └── storage.py
    │
    ├── Test Cases/   
    │   │   ├── sample_events_1.json
    │   │
    │   └── Results/
    │       └── performance_summary.csv
    │
    ├── Docs/
    │   ├── Software Design Document.pdf
    │
    └── README.md