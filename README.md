# export-excel

<h2>Getting started - base dependencies</h2> 
<p>First, make sure these packages are installed on your machine:</p>
<ul>
<li>Python -  to check type <code>python3 --version</code>. if that doesn’t work then try <code>python --version</code>. Then test the python shell by typing either <code>python3</code> or <code>python</code> depending on the version installed.</li>
<li>Pip - comes bundled with python3, but does not come with python 2.7 and needs to be installed seperately : <a href="https://pip.pypa.io/en/stable/installing/">Installation instructions here</a></li>
<li>Git - to check if it’s installed, type: <code>git --version</code>. If it needs to be installed, it can be downloaded from here: https://git-scm.com/downloads 
<br>See also - https://help.github.com/articles/set-up-git/</li>
<li>Vagrant - download from: https://www.vagrantup.com/downloads.html</li>
<li>VirtualBox - download from: https://www.virtualbox.org/</li>
</ul>

<p>Once everything is installed, make sure you are in the directory that you would like the app to live (i.e. ~/Desktop) then clone this repo by typing:
<pre><code>git clone https://github.com/ktully23/export-excel.git</code></pre></p> 

<h3>Starting the vagrant server</h3>
<p>The Vagrantfile that is needed to initialize the vagrant vm is already included in the git repo. 
To create the server, type <code>vagrant up</code>.
Once the server is finished downloading, login by typing <code>vagrant ssh</code></p>

<p><b>Next, install these packages: </b><br>
<pre><code>sudo apt-get -y update
sudo apt-get -y install python3 python3-venv python3-dev
sudo apt-get -y install mysql-server supervisor nginx git</code></pre>
Everything will install unattended except for the mysql server, it will ask a few questions before it is finished installing.</p>

<h3>Installing the application</h3>
To download the application to the server, run:
<pre><code>git clone https://github.com/ktully23/export-excel.git
cd export-excel
</code></pre>

<p>Next, create a virtual environment and populate it with all the package dependencies by running:
<pre><code>
$ python3 -m venv venv
$ source venv/bin/activate
(venv) $ pip install -r requirements.txt
</code></pre>
</p>
<p>One additional package needs to be installed:
<pre><code>(venv) $ pip install gunicorn</code></pre>
  </p>
