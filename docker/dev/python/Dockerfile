FROM python:3.13-bookworm

# Set working directory
WORKDIR /python-app

# Copy source code
COPY python-app/ .

ENV UV_PROJECT_ENVIRONMENT=/usr/local

# Install build tools and Python packages
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    curl \
    && pip install --upgrade pip \
    #dev libraries
    && pip install uv\
    && apt-get clean && rm -rf /var/lib/apt/lists/*