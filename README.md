# linkshortener-stack
Link Shortner Stack based on shlink and matomo.

## Overview

This repository contains a Docker Compose setup for deploying Shlink, an open-source URL shortener service with QR code generation capabilities.
The service is fully configured including a MariaDB instance and a the web client for Shlink.

## Features

- URL shortening service
- QR code generation
- Management interface for configuration
- Matomo for advanced visit analytics

# Usage

## Deployment

To deploy the service, use the provided docker-compose.yml file with:

```bash
docker-compose up -d
```

Ensure you have configured your application gateway (if any) properly for HTTPS support if using the external access point.


## Service URLs

- **shlink**: http://YourIP:8080/
- **shlink-web-client**: http://YourIP:8081/


## API Key Management

To generate a new API key:
```bash
shlink api-key:generate
```

Note: Generating a new API key will replace the existing one, requiring all users to update their configurations.

---

# References, Documentation & Links

## 🔗 Related Docker Images
The solution uses the following Docker images:

- [shlinkio/shlink](https://hub.docker.com/r/shlinkio/shlink/) - The core URL shortener service

- [shlinkio/shlink-web-client](https://hub.docker.com/r/shlinkio/shlink-web-client/) - Web client for Shlink

- [matomo/matomo](https://hub.docker.com/_/matomo/) - Matomo Official Docker Image

## 📚 Additional Documentation & Resources

- Shlink Deployment guide: [Shlink.io - Modern open-source URL shortener running via Docker](https://www.blackvoid.club/shlink-io-modern-open-source-url-shortener-running-via-docker/)

- A practical tutorial on self-hosting Matomo analytics using Docker: [davquar.it - Matomo Docker Guide](https://davquar.it/post/self-hosting/matomo-docker/)

- Official repository of Docker Compose examples showing various Matomo deployment scenarios: (Matomo Docker Examples)[https://github.com/matomo-org/docker/tree/master/.examples]

- Official Shlink documentation detailing the environment variables needed to configure Matomo analytics integration with Shlink URL shortener: (Shlink Matomo Integration Docs)[https://shlink.io/documentation/environment-variables/#matomo-integration]

- Discussion thread about Matomo integration implementation in Shlink, including feature requests and technical considerations for the analytics integration: (Shlink GitHub Issue #1798)[https://github.com/shlinkio/shlink/issues/1798]

# 🤝 How to Contribute
Every contribution to improve this project is welcome! Here’s how you can help:


## 💻 Code & Documentation Improvements
1) Fork the repository
2) Create a new branch (`git checkout -b feature/your-feature`)
3) Commit your changes (`git commit -m "Comment your improvements"`)
4) Push to the branch (`git push origin feature/your-feature`)
5) Open a Pull Request
