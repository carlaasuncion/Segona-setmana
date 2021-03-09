<h5>Continuació de generaci&oacute; de certificats de servidor i client.</h5>
<p><img src="https://img.icons8.com/doodle/48/000000/certificate.png" /></p>
<p>-/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"</p>
<p>-sudo apt-get install git</p>
<p>-test -d ~/.linuxbrew && eval $(~/.linuxbrew/bin/brew shellenv)</p>
<p>-test -d /home/linuxbrew/.linuxbrew && eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)</p>
<p>-test -r ~/.bash_profile && echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.bash_profile</p>
<p>-echo "eval \$($(brew --prefix)/bin/brew shellenv)" >>~/.profile</p>
<p>-brew install mkcert</p>

