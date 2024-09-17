# Primeira Atividade - Computação em Nuvem

## Dockerfile

No arquivo `Dockerfile`, cada linha é responsável por uma etapa na configuração do ambiente Docker. Veja a seguir o que cada linha faz:

1. **`FROM python:3.9-slim`**  
   Escolhe uma versão leve do Python 3.9 para começar.

2. **`WORKDIR /app`**  
   Define que o contêiner vai trabalhar na pasta `/app`.

3. **`COPY . /app`**  
   Copia todos os arquivos da pasta atual para a pasta `/app` no contêiner.

4. **`RUN pip install --no-cache-dir flask`**  
   Instala o Flask sem salvar arquivos desnecessários.

5. **`EXPOSE 8080`**  
   Declara que o contêiner vai usar a porta 8080.

6. **`ENV FLASK_APP=index.py`**  
   Configura o arquivo `index.py` como o principal do Flask.

7. **`CMD ["python", "index.py"]`**  
   Executa o arquivo `index.py` com Python quando o contêiner iniciar.

## Comandos Usados para Execução da Atividade

Aqui estão os comandos utilizados para a execução da atividade:

1. **`mkdir atividade`**  
   Cria uma pasta chamada `atividade`.

2. **`cd atividade`**  
   Navega para a pasta `atividade`.

3. **`nano index.py`**  
   Abre o editor de texto Nano para criar ou editar o arquivo `index.py`.

4. **`nano Dockerfile`**  
   Abre o editor de texto Nano para criar ou editar o arquivo `Dockerfile`.

5. **`sudo docker build -t atividade .`**  
   Cria uma imagem Docker chamada `atividade` a partir do `Dockerfile` no diretório atual (`.`). A opção `-t` define a tag (nome) da imagem.

6. **`sudo docker run -p 8080:8080 atividade`**  
   Inicia um contêiner a partir da imagem `atividade` e mapeia a porta 8080 do contêiner para a porta 8080 do host.
