# Serverless Infinity on Runpod for Nomic AI Embeddings

This repository demonstrates how to leverage a Runpod Serverless Endpoint running Infinity for efficient and scalable text embeddings using the nomic-ai/nomic-embed-text-v1.5 model. Infinity is a high-throughput, low-latency REST API designed for serving various models, including text embeddings.

## Project Overview
This project provides a complete example of:

1. PDF Text Extraction: Using `PyMuPDF` to extract text from a PDF document.
2. Text Chunking: Employing `langchain_text_splitters` to divide large texts into manageable chunks.
3. Runpod Serverless Endpoint Interaction:
   - Warming up the Infinity endpoint.
   - Asynchronously submitting text chunks for embedding to the Runpod endpoint.
   - Polling for job completion and retrieving embedding results.

(In progress)

## References:
- Infinity Github: [https://docs.vllm.ai/en/latest/](https://github.com/michaelfeil/infinity)
- Runpod Infinity: [https://github.com/runpod-workers/worker-infinity-embedding](https://github.com/runpod-workers/worker-infinity-embedding)
