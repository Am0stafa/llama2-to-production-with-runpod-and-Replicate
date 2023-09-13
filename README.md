# Deploying Llama-2 on RunPod

This repo contains a sample for deploying the [Llama-2](https://github.com/facebookresearch/llama) conversational AI model on [RunPod](https://runpod.io/), to quickly spin up an inference server.

## Overview

The main steps are:

- Install the RunPod Python SDK
- Authenticate with your RunPod API key  
- Launch a GPU pod with the Llama container
- Make requests to the pod's endpoint to generate text

The notebook provides examples using:

- The RunPod API directly  
- The `requests` library
- The Hugging Face `text-generation` client

It shows both synchronous requests and streaming.

## Usage

To use the notebook:

1. Clone this repo
2. Install the requirements
3. Add your RunPod API key  
4. Run the notebook cells to launch a pod and make requests

The pod will remain running until terminated, so you can experiment with different prompts. 

When finished, run the last cell to terminate the pod and avoid continued charges.

## Customization

The notebook can be adapted by:

- Using different GPU types or regions
- Launching multiple GPUs for faster inference
- Modifying the prompt formatting
- Switching Llama models like `TheBloke/Llama-7b-chat`

See the RunPod and Hugging Face docs for more options.

## References

- [RunPod Python SDK](https://docs.runpod.io/docs/python-sdk-overview)
- [Llama Models](https://huggingface.co/models?sort=downloads&search=llama)
- [text-generation Client](https://docs.huggingface.co/text-generation/index.html)

# Deploying Llama-2-13b on Replicate with LangChain

This repo contains a sample for deploying the large 13 billion parameter [Llama-2-13b](https://huggingface.co/TheBloke/Llama-2-13b) model on [Replicate](https://replicate.com/) using [LangChain](https://github.com/hwchase17/langchain) to build a conversational agent.

## Overview

The main steps are:

- Install LangChain and Replicate SDKs
- Create Replicate account and set API token
- Import Llama-2-13b model 
- Initialize a LangChain agent with the Replicate LLM 
- Run conversations by calling the agent

## Usage

To run the conversational agent:

1. Clone this repo
2. Install requirements
3. Set your Replicate API token  
4. Run the cells to deploy the model and initialize the agent
5. Call `agent_chain.run()` to have a conversation 

Stop the model when finished to avoid charges.

## Customization

The agent can be customized by:

- Using different Llama models
- Modifying the temperature, top-p, etc  
- Adding different tools like a Human or SQL tool
- Switching agent architectures

See the LangChain docs for options.

## References

- [LangChain](https://langchain.readthedocs.io)
- [Replicate Python SDK](https://docs.replicate.com/docs/python-sdk)
- [Llama Models](https://huggingface.co/models?sort=downloads&search=llama)

