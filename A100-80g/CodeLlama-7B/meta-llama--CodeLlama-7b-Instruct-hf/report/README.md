
Model card for CodeLlama-7b-Instruct-hf on A100-80g
===================================================

# Main metrics


The main metrics are summarized in the following table :   

|Metric|Value|
| :---: | :---: |
|Prompt ingestion speed|~13500 t/s |
|Mean generation speed for 10 parallel requests with a prompt of 1024 tokens and 128 tokens generated|~41 t/s for each request|
|Estimate of the max nb of tokens in KV cache|~100k tokens |

# Total generation speed


The following graph shows the total throughput with respect to the number of parallel queries for different scenarii :

<img src="./total_speed_generation_graph.png" width="800"/>  

# Generation speed and latency


The following graphs shows the throughput for each request with respect to the number of parallel queries. It also shows the time to first token and the corresponding gpu usage. The lines show the median whereas the bars show the 25th and 75th percentile

This graph is for prompt size of roughly 4096 tokens and 128 generated tokens :

<img src="./speed_generation/speed_generation_graph_input_4096_output_128.png" width="800"/>



This graph is for prompt size of roughly 32 tokens and 16 generated tokens :

<img src="./speed_generation/speed_generation_graph_input_32_output_16.png" width="800"/>


# Parameters


The api from happy_vllm was launched using the following arguments :   

|Parameter|Value|
| :---: | :---: |
|model|CodeLlama-7b-Instruct-hf|
|step_live_metrics|0.01|
|max_queries|1000|
|request_rate|0|
|backend|happy_vllm|
|suite_id|2024-07-05, 15:07:29|
|happy_vllm_version|1.1.3|
|vllm_version|0.4.3|
|host|0.0.0.0|
|port|8501|
|model_name|CodeLlama-7b-Instruct-hf|
|app_name|happy_vllm|
|api_endpoint_prefix|/api_vllm/rs|
|explicit_errors|False|
|allow_credentials|False|
|allowed_origins|['*']|
|allowed_methods|['*']|
|allowed_headers|['*']|
|uvicorn_log_level|info|
|ssl_keyfile|None|
|ssl_certfile|None|
|ssl_ca_certs|None|
|ssl_cert_reqs|0|
|root_path|None|
|lora_modules|None|
|chat_template|None|
|response_role|assistant|
|with_launch_arguments|True|
|tokenizer|None|
|skip_tokenizer_init|False|
|revision|None|
|code_revision|None|
|tokenizer_revision|None|
|tokenizer_mode|auto|
|trust_remote_code|False|
|download_dir|None|
|load_format|auto|
|dtype|auto|
|kv_cache_dtype|auto|
|quantization_param_path|None|
|max_model_len|None|
|guided_decoding_backend|outlines|
|distributed_executor_backend|None|
|worker_use_ray|False|
|pipeline_parallel_size|1|
|tensor_parallel_size|1|
|max_parallel_loading_workers|None|
|ray_workers_use_nsight|False|
|block_size|16|
|enable_prefix_caching|False|
|disable_sliding_window|False|
|use_v2_block_manager|False|
|num_lookahead_slots|0|
|seed|0|
|swap_space|4|
|gpu_memory_utilization|0.9|
|num_gpu_blocks_override|None|
|max_num_batched_tokens|None|
|max_num_seqs|256|
|max_logprobs|5|
|disable_log_stats|False|
|quantization|None|
|rope_scaling|None|
|enforce_eager|False|
|max_context_len_to_capture|None|
|max_seq_len_to_capture|8192|
|disable_custom_all_reduce|False|
|tokenizer_pool_size|0|
|tokenizer_pool_type|ray|
|tokenizer_pool_extra_config|None|
|enable_lora|False|
|max_loras|1|
|max_lora_rank|16|
|lora_extra_vocab_size|256|
|lora_dtype|auto|
|long_lora_scaling_factors|None|
|max_cpu_loras|None|
|fully_sharded_loras|False|
|device|auto|
|image_input_type|None|
|image_token_id|None|
|image_input_shape|None|
|image_feature_size|None|
|scheduler_delay_factor|0.0|
|enable_chunked_prefill|False|
|speculative_model|None|
|num_speculative_tokens|None|
|speculative_max_model_len|None|
|speculative_disable_by_batch_size|None|
|ngram_prompt_lookup_max|None|
|ngram_prompt_lookup_min|None|
|model_loader_extra_config|None|
|served_model_name|None|
|engine_use_ray|False|
|disable_log_requests|False|
|max_log_len|None|
|gpu_name|A100-80g|
