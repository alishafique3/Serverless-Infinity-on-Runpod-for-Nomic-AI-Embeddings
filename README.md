# Serverless Infinity on Runpod for Nomic AI Embeddings

[In Progress]

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
Upon successful execution, the script will output a summary of the processed tasks and the total time taken. You'll see confirmation of how many tasks were completed successfully, along with a sample of the first successful result. For 240 page PDF document, I got following results.
```
Completed 168/168 tasks
time taken 8.864368915557861
Total: 168, Successful: 168

First successful result:
{'delayTime': 4769, 'executionTime': 395, ...}
```

## Conclusion

This project demonstrates a robust and efficient solution for generating text embeddings at scale using **RunPod's serverless infrastructure** and the **Infinity API** with the **Nomic AI Nomic Embed Text v1.5 model**. By combining PDF text extraction, intelligent text chunking, and asynchronous API calls, we've created a workflow that can process large documents and retrieve embeddings quickly and cost-effectively.

This setup is ideal for applications requiring on-demand text vectorization, such as building custom RAG systems, powering semantic search functionalities, or performing large-scale data analysis. The flexibility and scalability offered by RunPod Serverless, coupled with the performance of Infinity, provide a powerful foundation for your NLP projects.

## References:
- Infinity Github: [https://docs.vllm.ai/en/latest/](https://github.com/michaelfeil/infinity)
- Runpod Infinity: [https://github.com/runpod-workers/worker-infinity-embedding](https://github.com/runpod-workers/worker-infinity-embedding)
