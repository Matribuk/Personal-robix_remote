# Robix Remote 🤖

A local ChatGPT clone powered by OpenAI's API, featuring a modern React frontend and a Go backend. 

[![License:  MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Go](https://img.shields.io/badge/Go-1.x-00ADD8?logo=go)](https://golang.org/)
[![React](https://img.shields.io/badge/React-18.2.0-61DAFB?logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0.2-3178C6?logo=typescript)](https://www.typescriptlang.org/)

## 📋 Overview

Robix Remote is a self-hosted ChatGPT-like application that allows you to interact with OpenAI's language models through a clean, local web interface. The project demonstrates a full-stack implementation with:

- **Backend**: Go with Gin framework
- **Frontend**: React 18 with TypeScript and Vite
- **Containerization**: Docker and Docker Compose for easy deployment
- **API Integration**: OpenAI API for natural language processing

## ✨ Features

- 💬 Real-time chat interface with OpenAI's GPT models
- 🐳 Fully containerized with Docker
- 🔒 Secure API key management through environment variables
- ⚡ Fast development with Vite and hot module replacement
- 🎨 Modern React architecture with TypeScript
- 🔄 CORS-enabled backend for seamless frontend-backend communication

## 🏗️ Project Structure

```
robix_remote/
├── BackEnd/              # Go backend service
│   ├── controllers/      # Request handlers
│   ├── middlewares/      # CORS and other middlewares
│   ├── routes/          # API route definitions
│   ├── main.go          # Application entry point
│   ├── Dockerfile       # Backend container configuration
│   └── go. mod           # Go dependencies
├── FrontEnd/            # React frontend application
│   ├── src/             # Source code
│   ├── public/          # Static assets
│   ├── package.json     # Node dependencies
│   ├── vite.config.ts   # Vite configuration
│   ├── tsconfig.json    # TypeScript configuration
│   └── Dockerfile       # Frontend container configuration
└── docker-compose.yaml  # Multi-container orchestration
```

## 🚀 Getting Started

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- OpenAI API Key (get one at [platform.openai.com](https://platform.openai.com/))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Matribuk/Personal-robix_remote.git
   cd Personal-robix_remote
   ```

2. **Set up your OpenAI API key**

   **Linux/MacOS:**
   ```bash
   export OPENAI_API_KEY="your-api-key-here"
   ```

   **Windows (Command Prompt):**
   ```cmd
   set OPENAI_API_KEY=your-api-key-here
   ```

   **Windows (PowerShell):**
   ```powershell
   $env: OPENAI_API_KEY="your-api-key-here"
   ```

   > 💡 **Tip**: For persistent configuration, add the export command to your shell profile (`~/.bashrc`, `~/.zshrc`, etc.)

3. **Start the application**
   ```bash
   docker-compose up
   ```

   Or run in detached mode:
   ```bash
   docker-compose up -d
   ```

4. **Access the application**
   
   Open your browser and navigate to: 
   ```
   http://localhost:3000
   ```

## 🛠️ Development

### Running without Docker

**Backend:**
```bash
cd BackEnd
export OPENAI_API_KEY="your-api-key-here"
go run main.go
```
The backend will start on `http://localhost:8080`

**Frontend:**
```bash
cd FrontEnd
yarn install
yarn dev
```
The frontend will start on `http://localhost:3000`

### Building for Production

```bash
# Build both services
docker-compose build

# Run in production mode
docker-compose up -d
```

## 🔧 Configuration

### Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `OPENAI_API_KEY` | Your OpenAI API key | *Required* |
| `REACT_APP_BACKEND_URL` | Backend API URL | `http://backend:8080` |

### Port Configuration

- **Frontend**: `3000`
- **Backend**: `8080`

Modify ports in `docker-compose.yaml` if needed.

## 📚 Tech Stack

### Backend
- **Language**: Go
- **Framework**: [Gin](https://github.com/gin-gonic/gin)
- **API**:  OpenAI API

### Frontend
- **Library**: React 18.2.0
- **Language**: TypeScript 5.0.2
- **Build Tool**: Vite 4.3.0
- **HTTP Client**: Axios 1.3.6
- **Linting**: ESLint with TypeScript support

## 🤝 Contributing

Contributions are welcome! Feel free to: 

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 👤 Author

**Antonin Leprest** ([@Matribuk](https://github.com/Matribuk))

[![GitHub](https://img.shields.io/badge/GitHub-Matribuk-181717?logo=github)](https://github.com/Matribuk)

## 🙏 Acknowledgments

- Built with [OpenAI's GPT models](https://platform.openai.com/docs/models)
- Inspired by ChatGPT's conversational interface

## ⚠️ Disclaimer

This project uses the OpenAI API which may incur costs based on usage. Please review OpenAI's [pricing](https://openai.com/pricing) before use.

---

<div align="center">
Made with ❤️ by <a href="https://github.com/Matribuk">Antonin Leprest</a>
</div>
