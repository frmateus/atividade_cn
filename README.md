Primeira atividade - Computação em Nuvem

Dockerfile

No arquivo Dockerfile vou explicar oque cada linha faz:

1- FROM python:3.9-slim: Escolhe uma versão leve do Python 3.9 para começar.
2- WORKDIR /app: Define que o contêiner vai trabalhar na pasta /app.
3- COPY . /app: Copia todos os arquivos da pasta atual para a pasta /app no contêiner.
4- RUN pip install --no-cache-dir flask: Instala o Flask sem salvar arquivos desnecessários.
5- EXPOSE 8080: Diz que o contêiner vai usar a porta 8080.
6- ENV FLASK_APP=index.py: Configura o arquivo index.py como o principal do Flask.
7- CMD ["python", "index.py"]: Roda o arquivo index.py com Python quando o contêiner iniciar.

Comandos que foram usados para execução da atividade:

1- mkdir atividade / O comando foi usado para criar uma pasta.
2- cd atividade / entramos na pasta criada.
3- nano index.py / abre o editor de texto Nano para criar ou editar o arquivo index.py
4- nano Dockerfile / O comando nano Dockerfile abre o editor de texto Nano para criar ou editar o arquivo Dockerfile
5- sudo docker build -t atividade . / O comando Docker cria uma imagem chamada atividade a partir do Dockerfile no diretório atual (representado pelo ponto .) O -t define a tag (nome) da imagem.
6- sudo docker run -p 8080:8080 atividade / Esse comando inicia um contêiner a partir da imagem atividade e mapeia a porta 8080 do contêiner para a porta 8080 do host.
