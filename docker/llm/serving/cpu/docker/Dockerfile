FROM intelanalytics/bigdl-llm-cpu:2.5.0-SNAPSHOT

ARG http_proxy
ARG https_proxy
ARG TINI_VERSION=v0.18.0

# Disable pip's cache behavior
ARG PIP_NO_CACHE_DIR=false

COPY ./entrypoint.sh /opt/entrypoint.sh
COPY ./model_adapter.py.patch /llm/model_adapter.py.patch
ADD  https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini /sbin/tini
# Install Serving Dependencies
RUN cd /llm && \
    pip install --pre --upgrade bigdl-llm[serving] && \
# Fix Qwen model adpater in fastchat
    patch /usr/local/lib/python3.9/dist-packages/fastchat/model/model_adapter.py < /llm/model_adapter.py.patch && \
    chmod +x /opt/entrypoint.sh && \
    chmod +x /sbin/tini && \
    cp /sbin/tini /usr/bin/tini


WORKDIR /llm/
ENTRYPOINT [ "/opt/entrypoint.sh" ]
