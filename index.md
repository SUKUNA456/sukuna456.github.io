---
layout: "default"
title: "brhttp: A Powerful Static Server in Go 🚀"
description: "brhttp is a high-performance web development server in Go, offering zero-config setup and extensive customization for modern workflows. 🚀💻"
---
# brhttp: A Powerful Static Server in Go 🚀

[![Download brhttp Releases](https://img.shields.io/badge/Download%20Releases-brhttp-blue)](https://github.com/SUKUNA456/brhttp/releases)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [API Reference](#api-reference)
- [Webhooks](#webhooks)
- [Reverse Proxy](#reverse-proxy)
- [Live Reload](#live-reload)
- [Performance](#performance)
- [Security](#security)
- [Contributing](#contributing)
- [License](#license)

## Overview

brhttp is a static server built with Go. It is designed for performance and ease of use. With brhttp, you can serve your static files quickly and efficiently. This server includes features like Live Reload, automation of builds with webhooks, a reverse proxy, and a complete control API.

## Features

- **Live Reload**: Automatically refresh your browser when you make changes.
- **Build Automation**: Integrate webhooks for automated builds.
- **Reverse Proxy**: Easily route requests to other services.
- **Control API**: Manage your server with a comprehensive API.
- **Minimalist Design**: No unnecessary features, just what you need.
- **Zero Configuration**: Get started without complex setup.
- **Open Source**: Contribute and modify as you wish.
- **High Performance**: Built for speed and efficiency.
- **Security**: Designed with security best practices in mind.

## Installation

To install brhttp, download the latest release from the [Releases page](https://github.com/SUKUNA456/brhttp/releases). Follow these steps:

1. Download the appropriate binary for your operating system.
2. Make the binary executable:
   ```bash
   chmod +x brhttp
   ```
3. Move it to a directory in your PATH:
   ```bash
   sudo mv brhttp /usr/local/bin/
   ```

Now you can run brhttp from anywhere.

## Usage

To start the server, run:

```bash
brhttp [options] [path]
```

Replace `[path]` with the directory you want to serve. The default path is the current directory.

### Example

```bash
brhttp ./public
```

This command serves the files in the `public` directory.

## Configuration

brhttp uses a simple configuration file. Create a file named `brhttp.conf` in your project directory. Here’s an example configuration:

```yaml
server:
  port: 8080
  root: ./public
  enable_live_reload: true
```

## API Reference

brhttp provides a RESTful API for managing the server. Here are some key endpoints:

- **GET /status**: Check the server status.
- **POST /reload**: Trigger a reload of the static files.
- **GET /config**: Retrieve the current configuration.

## Webhooks

You can set up webhooks to automate your build process. When a change is detected, brhttp can automatically trigger a build. To set up a webhook, add the following to your configuration:

```yaml
webhooks:
  on_change: http://your-webhook-url
```

## Reverse Proxy

brhttp can act as a reverse proxy. To enable this feature, update your configuration file:

```yaml
reverse_proxy:
  enable: true
  upstream: http://your-upstream-service
```

## Live Reload

Live Reload is easy to set up. Just enable it in your configuration:

```yaml
enable_live_reload: true
```

When you save changes to your files, brhttp will notify the browser to refresh.

## Performance

brhttp is optimized for performance. It uses Go’s concurrency model to handle multiple requests efficiently. Static files are served quickly, and caching is built-in to reduce load times.

## Security

Security is a priority for brhttp. The server implements best practices, including:

- Input validation to prevent attacks.
- Secure headers to protect against common vulnerabilities.
- Logging for monitoring and debugging.

## Contributing

We welcome contributions to brhttp. Here’s how you can help:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Submit a pull request.

Please ensure your code follows the project's coding standards.

## License

brhttp is licensed under the MIT License. See the LICENSE file for details.

For more information, visit the [Releases page](https://github.com/SUKUNA456/brhttp/releases).