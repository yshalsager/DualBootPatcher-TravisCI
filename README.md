# DualBootPatcher-TravisCI
DualBootPatcher TravisCI build configuration


[Travis CI](http://travis-ci.org/) is free open-source continues integration service, which simply take your project from GitHub and test / build it for you!
It's amazing solution if you don't have time/free space to test your code.
# How to build DualBootPatcher using TravisCI?
1. You'll need to signup Travis account, go [here](https://travis-ci.org/) and press signup, enter your GitHub account details then approve Travis needed permissions and done. 
2. Now Fork DualBootPatcher [repository](https://github.com/chenxiaolong/DualBootPatcher) to your account and create .travis.yml file in project root.
3. Copy [my Travis configuration](https://github.com/yshalsager/DualBootPatcher-TravisCI/blob/master/.travis.yml)  to your ".travis.yml"
4. Edit [line 8](https://github.com/yshalsager/DualBootPatcher-TravisCI/blob/master/.travis.yml#L46) with your Repository and branch you want to build.

`  - git clone https://github.com/yshalsager/DualBootPatcher -b master ${TRAVIS_BUILD_DIR}/DualBootPatcher/`

5. This simple TravisCI configuration builds apk, utilities.zip and linux version, and deploy them to transfer.sh.
6. Now open Travis and add your DualBootPatcher fork to projects and start building.
7. You'll find built apk md5 and links at the end of Travis log.
8. Build takes about 25 mins.
9. When you add new commits to repository Travis will always build new apk for you !
10. If you want to change something in configuration, always check its syntax to make sure it's valid YAML using this [site](http://yamllint.com/).

* This script is using docker images, originally made by Mr. @[chenxiaolong](https://github.com/chenxiaolong) [here](https://github.com/chenxiaolong/DualBootPatcher/tree/master/docker)
* I have made docker images and uploaded them to [docker hub](https://hub.docker.com/r/yshalsager/dualbootpatcher/)


What is [docker](https://www.docker.com/what-docker)? [in case you don't know it 😮 ]
> Docker is the world’s leading software container platform. Developers use Docker to eliminate “works on my machine” problems when collaborating on code with co-workers. Operators use Docker to run and manage apps side-by-side in isolated containers to get better compute density. Enterprises use Docker to build agile software delivery pipelines to ship new features faster, more securely and with confidence for both Linux, Windows Server, and Linux-on-mainframe apps.
