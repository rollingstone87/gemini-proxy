# Gemini-OpenAI-Proxy

Gemini-OpenAI-Proxy is a proxy designed to convert the OpenAI API protocol to the Google Gemini protocol. This enables applications built for the OpenAI API to seamlessly communicate with the Gemini protocol, including support for Chat Completion, Embeddings, and Model(s) endpoints.

---

## Table of Contents

- [Gemini-OpenAI-Proxy](#gemini-openai-proxy)
  - [Table of Contents](#table-of-contents)
  - [Build](#build)
  - [Deploy](#deploy)
  - [Usage](#usage)
  - [Compatibility](#compatibility)
  - [License](#license)

---

## Build

To build the Gemini-OpenAI-Proxy, follow these steps:

```bash
git clone
cd
docker build -t gemini-proxy .
```

---

## Deploy

We recommend deploying Gemini-Proxy using Docker for a straightforward setup. Follow these steps to deploy with Docker:

   You can do this on the command line:
   ```bash
   docker run -d -p 5556:8080 --memory=500m --memory-swap=500m --restart=unless-stopped --log-driver json-file --log-opt max-size=10m --log-opt max-file=3 -e GEMINI_KEY="key_here" -e DISABLE_MODEL_MAPPING=1 --name gemini-plushchina gemini-proxy:latest
   ```

Adjust the port mapping (e.g., `-p 8080:8080`) as needed, and ensure that the Docker image version (`zhu327/gemini-openai-proxy:latest`) aligns with your requirements.

---

## License

Gemini-OpenAI-Proxy is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
