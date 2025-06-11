FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye

# Install Ollama
RUN curl -fsSL https://ollama.com/install.sh | sh

# Copy requirements and install Python dependencies
COPY ../requirements.txt /tmp/requirements.txt
RUN pip3 install -r /tmp/requirements.txt \
    && rm /tmp/requirements.txt

# Expose Ollama's default port (if needed)
EXPOSE 11434

# Start Ollama by default (optional, can be handled in devcontainer.json)
# CMD ["ollama", "serve"]