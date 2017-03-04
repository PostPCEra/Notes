##  Install & Setup Notes

### 1.1  Install Node.JS on Ubantu
+ follow steps below to install [Node JS Version 6](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions)
+ curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
+ sudo apt-get install -y nodejs
+ 

### 1.2  Python Virual environment on Ubantu
+ Ubantu 16.04 OS install disribution install both Python 2.7 and Python 3.5
+ you can check this with  $ which python  $ which python3
+ now we need to create VIRTUAL Environment so that we keep all the software for  MasteryLearn in that dir
+ The venv became standard library from python3 v3.3. No need to install or download anything before hand, when succeeded, pip3 will come with the virtualenv just created
+ python3 -m venv <path-or-name-of-virtualenv>  # execute this when in user HOME DIR , this will create Virtual env
+ To active the **virtualenv**
  + source <path-to-the-virtualenv>/bin/active   # now Prompt will change,  Prompt string contains Virtual Env name
  + then to deactive it:
  + deactive

### Python Virual environment on Ubantu
+ [simple stack notes](http://stackoverflow.com/questions/29934032/virtualenv-python-3-ubuntu-14-04-64-bit)
+ Have Python3 installed on Ubantu machine
+ be in a diretroy where ALL Virtual Env are stored , mostly ~/asr-VirtualEnvs, and issue following 2 commands
+ python3 -m venv "name-of-virtualenv"  # this create 
+ source "path-to-the-virtualenv"/bin/active  #To active the virtualenv
+ deactive  #  then to deactive it, while you are in the venv dir
+
+ if installing other packages like PyTest , go insde dir where Virtual Env is creaed then do pip install. So this way 'PyTest works from VSCode itself'
+ sudo pip  install pytest

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
