# Serverless Infinity on Runpod for Nomic AI Embeddings

(In progress)

This repository demonstrates how to leverage a Runpod Serverless Endpoint running Infinity for efficient and scalable text embeddings using the nomic-ai/nomic-embed-text-v1.5 model. Infinity is a high-throughput, low-latency REST API designed for serving various models, including text embeddings.

## Project Overview

This project provides a complete example of:

* **PDF Text Extraction**: Using `PyMuPDF` to extract text from a PDF document.
* **Text Chunking**: Employing `langchain_text_splitters` to divide large texts into manageable chunks.
* **RunPod Serverless Endpoint Interaction**:
    * Warming up the Infinity endpoint.
    * Asynchronously submitting text chunks for embedding to the RunPod endpoint.
    * Polling for job completion and retrieving embedding results.

## Serverless Infinity Endpoint on Runpod

Before running the client code, ensure you have the following:

* A **RunPod account** and an **API Key**.
* A **RunPod Serverless Endpoint** configured with **Infinity** and the `nomic-ai/nomic-embed-text-v1.5` model. Remember to replace the `API_URL` and `API_KEY` in the provided code with your actual endpoint URL and API key.

## Client

## Results
Upon successful execution, the script will output a summary of the processed tasks and the total time taken. You'll see confirmation of how many tasks were completed successfully, along with a sample of the first successful result.
```
Completed 168/168 tasks
time taken 8.864368915557861
Total: 168, Successful: 168

First successful result:
{'delayTime': 4769, 'executionTime': 395, ...}
```


## References:
- Infinity Github: [https://docs.vllm.ai/en/latest/](https://github.com/michaelfeil/infinity)
- Runpod Infinity: [https://github.com/runpod-workers/worker-infinity-embedding](https://github.com/runpod-workers/worker-infinity-embedding)
