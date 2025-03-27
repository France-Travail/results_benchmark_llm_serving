
Model card for Mistral-Small-3.1-24B-Instruct-2503 on H100
==========================================================

# Main metrics


The main metrics are summarized in the following table :   

|Metric|Value|
| :---: | :---: |
|Prompt ingestion speed|~8500 t/s |
|Mean generation speed for 10 parallel requests with a prompt of 1024 tokens and 128 tokens generated|~36 t/s for each request|
|Estimate of the max nb of tokens in KV cache|~150k tokens|

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
|model|Mistral-Small-3.1-24B-Instruct-2503|
|step_live_metrics|0.01|
|max_queries|1000|
|request_rate|0|
|backend|happy_vllm|
|suite_id|2025-03-26, 13:43:50|
|model_name|Mistral-Small-3.1-24B-Instruct-2503|
|happy_vllm_version|1.2.4|
|vllm_version|0.8.2|
|host|0.0.0.0|
|port|8501|
|extra_information|None|
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
|enable_ssl_refresh|False|
|ssl_cert_reqs|0|
|root_path|None|
|lora_modules|None|
|chat_template|None|
|chat_template_content_format|auto|
|response_role|assistant|
|with_launch_arguments|True|
|return_tokens_as_token_ids|False|
|max_log_len|None|
|prompt_adapters|None|
|disable_frontend_multiprocessing|False|
|enable_request_id_headers|False|
|enable_auto_tool_choice|False|
|tool_call_parser|None|
|tool_parser_plugin||
|disable_fastapi_docs|False|
|enable_prompt_tokens_details|False|
|enable_server_load_tracking|False|
|disable_uvicorn_access_log|False|
|task|auto|
|tokenizer|None|
|hf_config_path|None|
|skip_tokenizer_init|False|
|revision|None|
|code_revision|None|
|tokenizer_revision|None|
|tokenizer_mode|mistral|
|trust_remote_code|False|
|allowed_local_media_path|None|
|download_dir|None|
|load_format|mistral|
|config_format|mistral|
|dtype|auto|
|kv_cache_dtype|auto|
|max_model_len|32768|
|guided_decoding_backend|xgrammar|
|logits_processor_pattern|None|
|model_impl|auto|
|distributed_executor_backend|None|
|pipeline_parallel_size|1|
|tensor_parallel_size|1|
|enable_expert_parallel|False|
|max_parallel_loading_workers|None|
|ray_workers_use_nsight|False|
|block_size|None|
|enable_prefix_caching|None|
|disable_sliding_window|False|
|use_v2_block_manager|True|
|num_lookahead_slots|0|
|seed|None|
|swap_space|4.0|
|cpu_offload_gb|0.0|
|gpu_memory_utilization|0.8|
|num_gpu_blocks_override|None|
|max_num_batched_tokens|None|
|max_num_partial_prefills|1|
|max_long_partial_prefills|1|
|long_prefill_token_threshold|0|
|max_num_seqs|None|
|max_logprobs|20|
|disable_log_stats|False|
|quantization|None|
|rope_scaling|None|
|rope_theta|None|
|hf_overrides|None|
|enforce_eager|False|
|max_seq_len_to_capture|8192|
|disable_custom_all_reduce|False|
|tokenizer_pool_size|0|
|tokenizer_pool_type|ray|
|tokenizer_pool_extra_config|None|
|limit_mm_per_prompt|None|
|mm_processor_kwargs|None|
|disable_mm_preprocessor_cache|False|
|enable_lora|False|
|enable_lora_bias|False|
|max_loras|1|
|max_lora_rank|16|
|lora_extra_vocab_size|256|
|lora_dtype|auto|
|long_lora_scaling_factors|None|
|max_cpu_loras|None|
|fully_sharded_loras|False|
|enable_prompt_adapter|False|
|max_prompt_adapters|1|
|max_prompt_adapter_token|0|
|device|auto|
|num_scheduler_steps|1|
|use_tqdm_on_load|True|
|multi_step_stream_outputs|True|
|scheduler_delay_factor|0.0|
|enable_chunked_prefill|None|
|speculative_config|None|
|speculative_model|None|
|speculative_model_quantization|None|
|num_speculative_tokens|None|
|speculative_disable_mqa_scorer|False|
|speculative_draft_tensor_parallel_size|None|
|speculative_max_model_len|None|
|speculative_disable_by_batch_size|None|
|ngram_prompt_lookup_max|None|
|ngram_prompt_lookup_min|None|
|spec_decoding_acceptance_method|rejection_sampler|
|typical_acceptance_sampler_posterior_threshold|None|
|typical_acceptance_sampler_posterior_alpha|None|
|disable_logprobs_during_spec_decoding|None|
|model_loader_extra_config|None|
|ignore_patterns|[]|
|preemption_mode|None|
|served_model_name|None|
|qlora_adapter_name_or_path|None|
|show_hidden_metrics_for_version|None|
|otlp_traces_endpoint|None|
|collect_detailed_traces|None|
|disable_async_output_proc|False|
|scheduling_policy|fcfs|
|scheduler_cls|vllm.core.scheduler.Scheduler|
|override_neuron_config|None|
|override_pooler_config|None|
|compilation_config|None|
|kv_transfer_config|None|
|worker_cls|auto|
|worker_extension_cls||
|generation_config|auto|
|override_generation_config|None|
|enable_sleep_mode|False|
|calculate_kv_scales|False|
|additional_config|None|
|enable_reasoning|False|
|reasoning_parser|None|
|disable_cascade_attn|False|
|disable_log_requests|False|
|engine_use_ray|False|
|gpu_name|H100|
