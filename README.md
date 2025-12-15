# Docker Ubuntu Desktop

Ubuntu Desktop Web Browser Accessible Docker Image

![Ubuntu Desktop Screenshot](screenshot.png)

## Overview

This project enables you to run a full Ubuntu graphical desktop environment within Docker and access it through any web browser. No VNC client software required - just a modern web browser.

## Quick Start

```bash
docker run -it --platform=linux/amd64 -p 6080:6080 atomic677/docker-ubuntu-desktop
```

Then open your browser and navigate to:
- [http://localhost:6080/vnc.html](http://localhost:6080/vnc.html)
- [https://localhost:6080/vnc.html](https://localhost:6080/vnc.html)

## Installation

### Pull from Docker Hub

```bash
docker pull atomic677/docker-ubuntu-desktop
```

### Build Locally

```bash
git clone https://github.com/atomic677/docker-ubuntu-desktop.git
cd docker-ubuntu-desktop
docker build . -t docker-ubuntu-desktop
```

### Run Local Build

```bash
docker run -it --platform=linux/amd64 -p 6080:6080 docker-ubuntu-desktop
```

## Features

- Full Ubuntu Desktop environment
- Web browser accessible (no VNC client needed)
- noVNC web client included
- Easy to deploy and use
- ubuntu 25.04
- 

## Access

Once the container is running, access the desktop via your web browser:

| Protocol | URL |
|----------|-----|
| HTTP | `http://localhost:6080/vnc.html` |
| HTTPS | `https://localhost:6080/vnc.html` |

## Configuration

### Custom Port

To use a different port, modify the `-p` flag:

```bash
docker run -it --platform=linux/amd64 -p 8080:6080 atomic677/docker-ubuntu-desktop
```

Then access via `http://localhost:8080/vnc.html`

### Persistent Storage

To persist data between container restarts:

```bash
docker run -it --platform=linux/amd64 -p 6080:6080 -v ~/ubuntu-data:/home atomic677/docker-ubuntu-desktop
```

## Requirements

- Docker installed on your system
- Web browser (Chrome, Firefox, Safari, Edge, etc.)

## License

MIT License

Copyright (c) 2023

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Author

[atomic677](https://github.com/atomic677)

## Repository

[https://github.com/atomic677/docker-ubuntu-desktop](https://github.com/atomic677/docker-ubuntu-desktop)

