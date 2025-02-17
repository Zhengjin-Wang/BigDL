BigDL-LLM LangChain API
=====================

LLM Wrapper of LangChain
----------------------------------------

Hugging Face ``transformers`` Format
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

BigDL-LLM provides ``TransformersLLM`` and ``TransformersPipelineLLM``, which implement the standard interface of LLM wrapper of LangChain.

.. tabs::

    .. tab:: AutoModel

        .. automodule:: bigdl.llm.langchain.llms.transformersllm
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: model_id, model_kwargs, model, tokenizer, streaming, Config

    .. tab:: pipeline

        .. automodule:: bigdl.llm.langchain.llms.transformerspipelinellm
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: pipeline, model_id, model_kwargs, pipeline_kwargs, Config


Native Model
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For ``llama``/``chatglm``/``bloom``/``gptneox``/``starcoder`` model families, you could also use the following LLM wrappers with the native (cpp) implementation for maximum performance.

.. tabs::

    .. tab:: Llama

        .. autoclass:: bigdl.llm.langchain.llms.bigdlllm.LlamaLLM
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: ggml_model, ggml_module, client, model_path, kwargs

            .. automethod:: validate_environment
            .. automethod:: stream
            .. automethod:: get_num_tokens

    .. tab:: ChatGLM

        .. autoclass:: bigdl.llm.langchain.llms.bigdlllm.ChatGLMLLM
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: ggml_model, ggml_module, client, model_path, kwargs

            .. automethod:: validate_environment
            .. automethod:: stream
            .. automethod:: get_num_tokens

    .. tab:: Bloom

        .. autoclass:: bigdl.llm.langchain.llms.bigdlllm.BloomLLM
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: ggml_model, ggml_module, client, model_path, kwargs

            .. automethod:: validate_environment
            .. automethod:: stream
            .. automethod:: get_num_tokens

    .. tab:: Gptneox

        .. autoclass:: bigdl.llm.langchain.llms.bigdlllm.GptneoxLLM
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: ggml_model, ggml_module, client, model_path, kwargs

            .. automethod:: validate_environment
            .. automethod:: stream
            .. automethod:: get_num_tokens

    .. tab:: Starcoder

        .. autoclass:: bigdl.llm.langchain.llms.bigdlllm.StarcoderLLM
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: ggml_model, ggml_module, client, model_path, kwargs

            .. automethod:: validate_environment
            .. automethod:: stream
            .. automethod:: get_num_tokens


Embeddings Wrapper of LangChain
----------------------------------------

Hugging Face ``transformers`` AutoModel
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. automodule:: bigdl.llm.langchain.embeddings.transformersembeddings
    :members:
    :undoc-members:
    :show-inheritance:
    :exclude-members: model, tokenizer, model_id, model_kwargs, encode_kwargs, Config

Native Model
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For ``llama``/``bloom``/``gptneox``/``starcoder`` model families, you could also use the following wrappers.

.. tabs::

    .. tab:: Llama

        .. autoclass:: bigdl.llm.langchain.embeddings.bigdlllm.LlamaEmbeddings
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: ggml_model, ggml_module, client, model_path, kwargs

            .. automethod:: validate_environment
            .. automethod:: embed_documents
            .. automethod:: embed_query

    .. tab:: Bloom

        .. autoclass:: bigdl.llm.langchain.embeddings.bigdlllm.BloomEmbeddings
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: ggml_model, ggml_module, client, model_path, kwargs

            .. automethod:: validate_environment
            .. automethod:: embed_documents
            .. automethod:: embed_query

    .. tab:: Gptneox

        .. autoclass:: bigdl.llm.langchain.embeddings.bigdlllm.GptneoxEmbeddings
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: ggml_model, ggml_module, client, model_path, kwargs

            .. automethod:: validate_environment
            .. automethod:: embed_documents
            .. automethod:: embed_query

    .. tab:: Starcoder

        .. autoclass:: bigdl.llm.langchain.embeddings.bigdlllm.StarcoderEmbeddings
            :members:
            :undoc-members:
            :show-inheritance:
            :exclude-members: ggml_model, ggml_module, client, model_path, kwargs

            .. automethod:: validate_environment
            .. automethod:: embed_documents
            .. automethod:: embed_query
