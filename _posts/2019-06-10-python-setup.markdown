---
layout: post
title:  "Python setup"
date:   2019-06-09 01:25:21 +0530
categories: python terminal ubuntu
---


python3 should be on ubuntu by default, install pip
```
sudo apt install -y python3-pip
```

No sure why needed but install following as well:
```
sudo apt install build-essential libssl-dev libffi-dev python-dev
```

Install virtual environment
```
sudo apt install -y python3-venv
```

Create virtual environment by running venv module:
```
python3 -m venv my_env
```

Use following to activate and deactivate the environment:
```
source my_env/bin/activate
source pyenvs/base/bin/activate
deactivate
```

Conda may be better in long run to manage the environment and installing packages (?)

Add conda to the path
```
export PATH=~/anaconda3/bin:$PATH
```

Create a conda env:
```
conda create --name my_env
```


Experimental but working with anaconda3 -- add conda to the bash shell
```
conda init bash
```
