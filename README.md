AtivaData Platform Core
(https://img.shields.io/badge/built%20with-Rust-red)](https://www.rust-lang.org)

AtivaData is a high-performance, warehouse-native Data Activation Platform designed to orchestrate marketing data at scale.

Unlike traditional CDPs that create data silos, AtivaData acts as an intelligent activation layer directly on top of the Data Warehouse (Snowflake, BigQuery), leveraging Agentic AI to automate audience segmentation and syncs.

🚀 Architectural Highlights
This repository contains the core infrastructure components built in Rust to ensure memory safety, zero-cost abstractions, and predictable latency under high throughput.

Components
Gateway (/src/gateway): A high-performance reverse proxy built on top of Cloudflare Pingora. It implements the Strangler Fig Pattern to seamlessly route traffic between legacy ingestion pipelines and next-gen Rust workers.

Ingestion Worker (/src/ingestion): (In Progress) Kafka consumer utilizing rdkafka and polars for batch processing of analytics events > 100k events/sec.

Semantic Layer: A definition engine to map warehouse schemas to business logic, enabling LLM-to-SQL translation.

🛠️ Technology Stack
Language: Rust 🦀 (for Data Plane), Go (for Control Plane)

Proxy Framework: Pingora

Stream Processing: Polars & Apache Arrow

Queue: Redpanda / Kafka
