---
title: How to post to this web site
date: 2018-08-22 09:50:45
tags: [Github,Hexo]
---
#### STEP1

- Email Jing with your Github account to be a collaborator
- After you get response from Jing, go to next steps

#### STEP2

##### 1. 安装git

Depends on your system, pls consult any resource to install git into your system

##### 2.安装node.js

```
wget -qO- https://raw.github.com/creationix/nvm/master/install.sh | sh
nvm install stable
```

#####3. 安装hexo

```
npm install hexo --save
npm install -g hexo-cli
npm install hexo-deployer-git --save
```

#### STEP3

##### 1. Clone hexo branch

```
git clone -b hexo https://github.com/f5se/f5se.github.io.git
```

##### 2.Init Hexo in the folder

```
cd f5se.github.io
npm install
```

All the above steps just need run one time. After the above steps, you have a local hexo repo for posting new post now. 

In the future, you just need follow below steps to enjoy your new post and make sure collaborate with others.

### How to post a new post and make the github source repo be fresh

each time you want to post a new, just (MUST) follow the below command order:

```
cd f5se.github.io
git pull origin hexo
(MUST run the above command first!!! Every important!!!)
hexo new "your new post title"
(Then edit the md file that just created. Once finish, then run below commands, ordered!)
git add source
git commit -m "your-name create new post"
git push origin hexo
hexo clean
hexo g
hexo d
```

After hexo deploy successfully, check https://f5se.io to verify the new post. If you want to edit your post, just run the above command again except the ```hexo new ``` command . 
Anytime, you just need make sure you git pull hexo branch first before you do anything and git push hexo branch after you do anything.
