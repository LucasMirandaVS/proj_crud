# Use uma imagem base com Python
FROM python:3.12-slim

# Instale o Poetry
RUN pip install poetry

# Copie os arquivos necessários para o container
WORKDIR /app
COPY pyproject.toml poetry.lock /app/

# Instale as dependências
RUN poetry install --no-root

# Copie o restante dos arquivos
COPY . /app

# Exponha a porta da aplicação
EXPOSE 8000

# Comando para iniciar a aplicação
CMD ["poetry", "run", "python", "main.py"]
