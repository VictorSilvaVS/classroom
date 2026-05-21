{
  "name": "Classroom Dev Environment",
  "image": "mcr.microsoft.com/devcontainers/base:ubuntu",
  "features": {
    // Instala o Python 3 e o pip automaticamente de graça
    "ghcr.io/devcontainers/features/python:1": {
      "version": "latest"
    },
    // Instala o compilador C (GCC), g++ e make automaticamente
    "ghcr.io/devcontainers/features/common-utils:2": {
      "configureZshAsDefaultShell": true
    }
  },
  "updateContentCommand": "sudo apt-get update && sudo apt-get install -y build-essential",
  "customizations": {
    "vscode": {
      // Já deixa as extensões instaladas para eles não precisarem procurar na loja
      "extensions": [
        "ms-python.python",
        "ms-vscode.cpptools"
      ]
    }
  }
}
