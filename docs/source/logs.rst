Latest Logs From Latest Build
==============================

Generated On: 2026-03-12 19:13:20 UTC

These are the latest logs generated from your latest build.  

.. tip:: 
   Complete logs from all builds can be found `here on GitHub <https://github.com/smaurice101/raspberrypitss/blob/main/tml-airflow/logs/logs.txt>`_

.. code-block:: 
  :linenos:

  [INFO 2026-03-12_19:08:59] STEP 1: completed - TML system parameters successfully gathered

  [INFO 2026-03-12_19:09:06] STEP 2: Create topics started

  [INFO 2026-03-12_19:09:19] STEP 2: Completed

  [INFO 2026-03-12_19:09:34] STEP 3: producing data started

  [INFO 2026-03-12_19:09:36] STEP 3: RESTAPI HTTP Server started ... successfully

  [INFO 2026-03-12_19:09:42] STEP 4: Preprocessing started

  [INFO 2026-03-12_19:09:44] STEP 4: Preprocessing started

  [INFO 2026-03-12_19:09:51] STEP 5: Machine learning started

  [INFO 2026-03-12_19:09:58] STEP 6: Predictions started

  [INFO 2026-03-12_19:10:03] STEP 7: Visualization started

  [INFO 2026-03-12_19:10:08] STEP 7: /Viperviz/viperviz-linux-amd64 0.0.0.0 49689

  [INFO 2026-03-12_19:10:25] STEP 9: Qdrant container.  Here is the run command: docker run -d -p 6333:6333 -v $(pwd)/qdrant_storage:/qdrant/storage:z qdrant/qdrant, v=0

  [INFO 2026-03-12_19:10:25] STEP 9: Success starting Qdrant.  Here is the run command: docker run -d -p 6333:6333 -v $(pwd)/qdrant_storage:/qdrant/storage:z qdrant/qdrant

  [INFO 2026-03-12_19:10:29] STEP 9b: Starting ollama server

  [INFO 2026-03-12_19:10:30] STEP 9: Starting privateGPT

  [INFO 2026-03-12_19:10:40] STEP 9b: Ollama container.  Here is the run command: docker run -d -p 11434:11434 --net=host --gpus all -v /var/run/docker.sock:/var/run/docker.sock:z -v /rawdata/ollama:/root/.ollama:z --env OLLAMA_LOAD_TIMEOUT=30m0s --env PORT=11434 --env TSS=1 --env GPU=1 --env COLLECTION=tml-llm-model-v2 --env WEB_CONCURRENCY=2 --env CUDA_VISIBLE_DEVICES=0 --env TOKENIZERS_PARALLELISM=false --env temperature=0.1 --env LLAMAMODEL="llama3.1" --env mainembedding="nomic-embed-text" --env OLLAMASERVERPORT="http://127.0.0.1:11434" maadsdocker/tml-privategpt-with-gpu-nvidia-amd64-llama3-tools, v=0

  [INFO 2026-03-12_19:10:40] STEP 9b: Success starting Agentic AI.  Here is the run command: docker run -d -p 11434:11434 --net=host --gpus all -v /var/run/docker.sock:/var/run/docker.sock:z -v /rawdata/ollama:/root/.ollama:z --env OLLAMA_LOAD_TIMEOUT=30m0s --env PORT=11434 --env TSS=1 --env GPU=1 --env COLLECTION=tml-llm-model-v2 --env WEB_CONCURRENCY=2 --env CUDA_VISIBLE_DEVICES=0 --env TOKENIZERS_PARALLELISM=false --env temperature=0.1 --env LLAMAMODEL="llama3.1" --env mainembedding="nomic-embed-text" --env OLLAMASERVERPORT="http://127.0.0.1:11434" maadsdocker/tml-privategpt-with-gpu-nvidia-amd64-llama3-tools

  [INFO 2026-03-12_19:10:47] STEP 8: Starting docker push for: maadsdocker/tml-server-v1-plugin-3f10-ml_agenticai_restapi-amd64

  [INFO 2026-03-12_19:10:58] STEP 9: PrivateGPT container.  Here is the run command: docker run -d -p 8001:8001 --net=host --gpus all -v /var/run/docker.sock:/var/run/docker.sock:z --env PORT=8001 --env TSS=1 --env GPU=1 --env COLLECTION=tml-llm-model-v2 --env WEB_CONCURRENCY=2 --env CUDA_VISIBLE_DEVICES=0 --env TOKENIZERS_PARALLELISM=false --env temperature=0.1 --env vectorsearchtype="Manhattan" --env contextwindowsize=8192 --env vectordimension=768 --env mainmodel="" --env mainembedding="" , v=1

  [WARN 2026-03-12_19:10:58] STEP 9: There seems to be an issue starting the privateGPT container.  Here is the run command - try to run it nanually for testing: docker run -d -p 8001:8001 --net=host --gpus all -v /var/run/docker.sock:/var/run/docker.sock:z --env PORT=8001 --env TSS=1 --env GPU=1 --env COLLECTION=tml-llm-model-v2 --env WEB_CONCURRENCY=2 --env CUDA_VISIBLE_DEVICES=0 --env TOKENIZERS_PARALLELISM=false --env temperature=0.1 --env vectorsearchtype="Manhattan" --env contextwindowsize=8192 --env vectordimension=768 --env mainmodel="" --env mainembedding="" 

  [WARN 2026-03-12_19:10:59] STEP 9b unable to load LLM - Aborting

  [ERROR 2026-03-12_19:11:16] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:11:26] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:11:39] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:11:49] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:11:59] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:12:09] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:12:19] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:12:30] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:12:39] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:12:47] STEP 9b: Agentic AI Step 9b DAG in tml_system_step_9b_agenticai_dag-tml-server-v1-plugin-3f10.py 'NoneType' object has no attribute 'lower'  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:12:48] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [ERROR 2026-03-12_19:12:59] STEP 9: PrivateGPT Step 9 DAG in tml_system_step_9_privategpt_qdrant_dag-tml-server-v1-plugin-3f10.py object of type 'NoneType' has no len()  Aborting after 10 consecutive errors.

  [INFO 2026-03-12_19:13:07] STEP 8: Docker Container created and optimized.  Will push it now.  Here is the commit command: docker commit fa349399859a maadsdocker/tml-server-v1-plugin-3f10-ml_agenticai_restapi-amd64 - message=0

  [INFO 2026-03-12_19:13:20] STEP 10: Started to build the documentation

  [INFO 2026-03-12_19:13:20] STEP 10: Documentation successfully built on GitHub..Readthedocs build in process and should complete in few seconds


