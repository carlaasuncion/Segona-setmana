<h5>Continuació de generaci&oacute; de certificats de servidor i client.</h5>
<p><img src="https://img.icons8.com/doodle/48/000000/certificate.png" /></p>
<p>-/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"</p>
<p>-sudo apt-get install git</p>
<p>-test -d ~/.linuxbrew && eval $(~/.linuxbrew/bin/brew shellenv)</p>
<p>-test -d /home/linuxbrew/.linuxbrew && eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)</p>
<p>-test -r ~/.bash_profile && echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.bash_profile</p>
<p>-echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.profile</p>
<p>-brew install mkcert</p>
<p><img src="https://user-images.githubusercontent.com/71402147/110442432-2270f580-80bb-11eb-957b-f98b4bee943d.png" alt="Cat"></p>
<p>Per crear la clau i el certificat</p>
<p>-mkcert example.com "*example.com" example.test inte 10.5.2.14</p>
<p>Ara vull canviar el nom de example.com per un nom amb mes sentit per aixo fem aquestes dues comandes:</p>
<p>-mv example.com+4-key.pem clau.pem</p>
<p>-mv example.com+4.pem certificat.pem</p>
<p>Un cop fet tot aixo ens anem a https://10.5.2.14/login (sense que estigui en inte perque la clau i certificat l'hem creat a base)</p>
<p>Ens loguem</p>
<p>Anem a "System settings", "TLS certificate"</p>
<p>Ara dins de "Browse" primer posem la clau i en els dos ultims els certificats</p>
<p><img src="https://user-images.githubusercontent.com/71402147/110687600-f8195800-81e0-11eb-910b-4e8f0ae5bb6b.png" alt="Cat"></p>
<p>En inte</p>
<p>-docker start error404</p>
<p><img src="https://user-images.githubusercontent.com/71402147/110686205-7bd24500-81df-11eb-8d32-1ff586eb044f.png" alt="Cat"></p>





