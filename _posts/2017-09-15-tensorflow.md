---
layout: post
title: Tensorflow howto
tags: numpy pandas scikit-learn matplotlib tensorflow
---

<!-- vim-markdown-toc GFM -->
* [Installation](#installation)

<!-- vim-markdown-toc -->
# Installation
1. Python: 
```
brew install python3 pip3
```

2. Virtual env 
If you want to use virtual environments use venv param in the folder with the project: 
```
python3 -m venv xxx 
cd xxx
source bin/activate
```
NOTE: There are other alternatives as virtualenv, but I couldn't use it with the current configuration on my mac.

3. numpy, pandas,...
```
pip3 install --upgrade numpy scipy scikit-learn pandas jupyter matplotlib pydot
```

4. tensorflow
```
pip3 install --upgrade tensorflow
```

