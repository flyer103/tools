# Dockerfiles

This repository is a collection of Dockerfiles for my daily used development tools and environments. It serves as a centralized place to maintain and version control various Docker configurations that I frequently use.

## Contents

- `ubuntu20.04-dev`: Development environment based on Ubuntu 20.04
- `ubuntu22.04-dev`: Development environment based on Ubuntu 22.04

## Purpose

The main purposes of this repository are:

1. Maintain consistent development environments across different machines
2. Version control Docker configurations for various tools and environments
3. Make it easy to recreate development environments when needed
4. Share common development setups with team members

## Usage

Each directory contains a `Dockerfile` with specific configurations. To build and use these images, navigate to the desired directory and run:

```bash
docker build -t <image-name> .
docker run -it <image-name>
```