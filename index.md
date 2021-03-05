<h5>Solucio a problema</h5>
<p>Jo personalment he tingut molts problemes amb el curl fins que vaig averiguar que el problema era un error del docker-compose.yml</p>
<p><img src="https://user-images.githubusercontent.com/71402147/110096160-ef1e2600-7d9d-11eb-8e68-419c5b82d80b.png" alt="Cat"></p>
<p>Per solucionar-ho el que vaig fer es restaurar la màquina i despres fer les comandes que poso a continuacio:</p>
<p>-sudo curl -L "https://github.com/docker/compose/releases/download/1.26.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose</p>
<p>-sudo chmod +x /usr/local/bin/docker-compose</p>
<p>-docker-compose --version</p>
<p>Al fer la comanda anterior es te que mostrar la versio 1.26.0</p>
<p>-mkdir ~/compose-demo</p>
<p>-cd ~/compose-demo</p>
<p>-mkdir app</p> 
<p>-nano app/index.html</p>
<p>Dins d'aqui posem:</p>
<p><img src="https://user-images.githubusercontent.com/71402147/109990050-576ef800-7d09-11eb-81de-7f1ae5ac9cde.png" alt="Cat"></p>
<p>-nano docker-compose.yml</p>
<p>Dins posem:</p>
<p><img src="https://user-images.githubusercontent.com/71402147/109989281-a5cfc700-7d08-11eb-8a3c-0254337c1148.png" alt="Cat"></p>
<p>Ara instalarem docker per aixo farem les següents comandes</p>
<p>-sudo apt update</p>
<p>-sudo apt install apt-transport-https ca-certificates curl software-properties-common gnupg2</p>
<p>-curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -</p>
<p>-sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"</p>
<p>-sudo apt update</p>
<p>-sudo apt install docker-ce</p>
<p>Ara si nosaltres fem la comanda surt:</p>
<p>-docker-compose up -d</p>
<p><img src="https://user-images.githubusercontent.com/71402147/109988562-f135a580-7d07-11eb-9fa1-c9781eddaa9e.png" alt="Cat"></p>
<p>Ara hens asegurarem de tenir l'ultima versio de imatges</p>
<p>-docker pull docker.io/joaniznardo/ubuntum7base</p>
<p>-docker pull docker.io/joaniznardo/ubuntum7tftp1</p>
<p>-docker volume create lab30_dadesserver</p>
<p>-docker run --name helper -v lab30_dadesserver: / fecha alpine true</p>
<p>-docker cp server.ini helper: / fecha</p>
<p>-docker rm helper</p>

A PARTIR DE AQUI NO ESTOY SEGURA

<h5>Creació d'un compte REST API</h5>
<p>-curl -v -k -u admin@carla.org:123 -d 'name=nestorisback&email=nestor@elmeuprimerdomini.org&passwordPlaintext=peasovacances' https://demo.poste.io/admin/api/v1/domains</p>
<h5>Creació d'un domini</h5>
<p>-curl -v -k -u admin@carla.org:123 -d 'name=unaltredominiqualsevol.edu' https://demo.poste.io/admin/api/v1/domains</p>
<p><img src="https://user-images.githubusercontent.com/71402147/110120492-68794100-7dbd-11eb-8412-5b2388b85d5a.png" alt="Cat"></p>
<h5>Desactivacio o activacio de compte administratiu</h5>
<p>-curl -v -k -u admin@carla.org:123 --header "Content-Type: application/json" -X "PATCH" --data '{"superAdmin":true}' https://demo.poste.io/admin/api/v1/domains </p>


