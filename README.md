# LLM Quickstart

A few minimal examples for tinkering around with LLMs.

-  `Docker`: Deploys a server to run Llama Index locally.
   -  Be sure Docker is running (in Windows, launch Docker Desktop).
   -  To deploy: `docker compose up -d`.
   -  To turn down: `docker compose down`.
   -  To recreate (sometimes necessary if you modify the Dockerfile) `docker-compose up --build --force-recreate`.

- `API`: Examples for calling to OpenAI API and HuggingFace's InferenceAPI.

## Examples and Use Cases
- [Examples from Llama Index.](https://github.com/jerryjliu/llama_index/tree/main/examples)
- [Use Cases - Llama Index docs.](https://gpt-index.readthedocs.io/en/latest/end_to_end_tutorials/use_cases.html) 
- [Web application starter packs.](https://github.com/logan-markewich/llama_index_starter_pack)
  
## Other alternatives to running local models
- [Llama Index - Private setup.](https://colab.research.google.com/drive/16QMQePkONNlDpgiltOi7oRQgmB8dU5fl?usp=sharing#scrollTo=d8e02c06)
- [GPT4All.](https://github.com/nomic-ai/gpt4all)
- [PrivateGPT.](https://github.com/imartinez/privateGPT)
