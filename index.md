<h5>Gestió de comptes de domini</h5>
<p>Jo personalment he tingut molts problemes amb el curl fins que vaig averiguar que el problema era un error del docker-compose.yml</p>

<p>Per solucionar-ho el que vaig fer es restaurar la màquina</p>
<p>-sudo curl -L "https://github.com/docker/compose/releases/download/1.26.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose</p>
<p>-sudo chmod +x /usr/local/bin/docker-compose</p>
<p>-docker-compose --version</p>
<p>Al fer la comanda anterior es te que mostrar la versio 1.26.0</p>
<p>-mkdir ~/compose-demo</p>
<p>-cd ~/compose-demo</p>
<p>-mkdir app</p> 
<p>-nano app/index.html</p>
<p>Dins d'aqui posem:</p>
<p><!doctype html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Docker Compose Demo</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/kognise/water.css@latest/dist/dark.min.css">
</head>
<body>

    <h1>This is a Docker Compose Demo Page.</h1>
    <p>This content is being served by an Nginx container.</p>

</body>
</html></p>
<p>-nano docker-compose.yml</p>
<p>Aqui dins posem:</p>
<p>version: '3.7'
services:
  web:
    image: nginx:alpine
    ports:
      - "8000:80"
    volumes:
      - ./app:/usr/share/nginx/html</p>
<p>Ara instalarem docker per aixo farem les següents comandes</p>
<p>Aqui dins posem:</p>
<p>-sudo apt update</p>
<p>-sudo apt install apt-transport-https ca-certificates curl software-properties-common gnupg2</p>
<p>-curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -</p>
<p>-sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"</p>
<p>-sudo apt update</p>
<p>-sudo apt install docker-ce</p>
<p>Ara si nosaltres fem la comanda surt:</p>
<p>-docker-compose up -d</p>
<p><img src="https://user-images.githubusercontent.com/71402147/109988562-f135a580-7d07-11eb-9fa1-c9781eddaa9e.png" alt="Cat"></p>
<p>Per veure el menú de curl utilitzarem la comanda:/p>
<p>-man curl</p>
