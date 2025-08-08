FROM python:3.13-bookworm

# Set working directory
WORKDIR /python-app

# Copy source code
COPY python-app/ .

ENV UV_PROJECT_ENVIRONMENT=/usr/local

# Install system dependencies and Python tools
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    curl \
    libmagic-dev \
    poppler-utils \
    tesseract-ocr \
    libgl1 \
    ocrmypdf

RUN pip install --upgrade pip \
    && pip install uv \
    && apt-get clean && rm -rf /var/lib/apt/lists/* \
    && pip install ipykernel -U --user --force-reinstall

