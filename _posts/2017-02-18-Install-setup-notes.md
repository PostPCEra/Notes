## Setup & Installation Notes for MasteryLearn
+ Install Node JS
+ Install Virtual Environment
+ Intall Bottle (HTTP Webserver)
+ Install Application MasteryLearn

### 1  Install Node JS
+ follow steps below to install [Node JS Version 6](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions)
+ curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
+ sudo apt-get install -y nodejs
+ 

### 2 Install Virual Environment
+ Ubantu 16.04 OS disribution installs both Python 2.7 and Python 3.5 by default, so you get them FREE with Ubantu install
+ Anaconda is creating issues with other pip installs such as 'Bottle', so for now stick with PIP3
+ you can check this with  $ which python  $ which python3
+ now we need to create VIRTUAL Environment so that we keep all the software for  MasteryLearn in that dir
+ 
+ **The venv became standard library from python3 v3.3**. No need to install or download anything before hand, when succeeded, [pip3 will come with the virtualenv just created](http://stackoverflow.com/questions/29934032/virtualenv-python-3-ubuntu-14-04-64-bit/35024841)
+ be in HOME DIR,  mkdir asr-venv , cd asr-venv   # this will hold all INDIVIDUAL virutal environments, you can have many 
+ **2.1 Install Pip3**
  + sudo apt-get install -y python3-pip
  + 
+ **2.2 Create Virtual Env**
  + python3 -m venv py3-mlearn  # execute this when in user HOME DIR , this will create Virtual environment named  py3-mlearn
+ **2.3 To activate the virtualenv**
  + source "<path-to-the-virtualenv>"/bin/activate   # now Prompt will change,  Prompt string contains Virtual Env name
  + then to deactive it:
  + deactive
+
+ to install any additional Packages be in the Virutal env dir

### 3   Intall Bottle (HTTP Webserver)
+ **Bottle : Pyton HTTP Server**[ install steps](https://bottlepy.org/docs/dev/tutorial.html)
  + sudo pip install bottle  # this will install bottle ( Python HTTP server )
  + (py3-mlearn)$ pip install -U bottle  # Install bottle to virtual environment
  + to test bottle install : $ python bottle  # this will show bottle command prompt
  +
+ if installing other packages like PyTest , go insde dir where Virtual Env is creaed then do pip install. So this way 'PyTest works from VSCode itself'
+ sudo pip  install pytest


### 4 Install Application MasteryLearn
+ Install Python Tutor
  + cd ~/asr-venv/py3-mlearn
  + git clone "OPT path.git"  # this will clone OPT Github repo to local dir
  + cd v5-unity 
  + Global **npm dependency installs** (run these commands in the v5-unity/ directory):
    + sudo npm install webpack -g
    + npm link webpack            # link to the local node_modules/ dir
    + sudo npm install webpack-dev-server -g
    + sudo npm install -g typescript
    + npm link typescript         # link to the local node_modules/ dir
    + sudo npm install -g tsd
+
+ Run "npm install" in this directory to install node dependencies
+ Run "tsd install" in this directory to install TypeScript definition files
+
+ **Running OPT server** , 
  + do these 2 steps in different Terminal , but always your terminal should show you are in ACTIVE Virtual Env.
  + npm dev webpack  (To start the Webpack file watching and compilation environment)
  + npm start  ( this will start Bottle HTTP Server )
  + then visit here to load an HTML page in your browser: [http://localhost:8003/visualize.html](http://localhost:8003/visualize.html)

### Learing by Doing first pages 
+ How to introduce to user next to 'Live coding Environment'
+ content & UX samples : Rubymonk , [Programirz](https://www.programiz.com/python-programming)
+ Audio files and  using 'moving INtro JS lib' 

### Website CORE PARTS
+ OPT is uising JQuery , so we use same JQuery
+ next to Live code #
+ Intro JS makes  with Audio makes it so easy to get a point Across table. apply to most the IT infrasture fix

# Tools
+ [Intro JS]( http://introjs.com) A better way for new feature introduction and step-by-step users guide for your website and project.
+ IBM watson Audio
