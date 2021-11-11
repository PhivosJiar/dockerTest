# <img src="https://cdn.icon-icons.com/icons2/2107/PNG/512/file_type_docker_icon_130643.png" width="50"/>Docker with VSCode Remote Container

## About Docker
什麼是 Docker？- https://aws.amazon.com/tw/docker/ <br>
Visual Studio Code 使用 Remote Container 建立專案開發環境- https://www.tpisoftware.com/tpu/articleDetails/2575#id6 <br>
[ 前端新手技能樹 ] #1 VS Code、Docker 與開發環境建置- https://www.youtube.com/watch?v=CxNm-3EedyA

## What do I need to prepare

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2d/Visual_Studio_Code_1.18_icon.svg/1024px-Visual_Studio_Code_1.18_icon.svg.png" width="50"/>&nbsp;
<img src="https://microsoft.github.io/vscode-remote-release/images/remote-containers-blue.svg" width="50"/>&nbsp;
<img src="https://cdn.icon-icons.com/icons2/2107/PNG/512/file_type_docker_icon_130643.png" width="50"/>


## How to add angular cli in image
Add this row in dockerfile. <br>
``` dockerfile
RUN npm install -g @angular/cli@yourversion 
```
Complete docker file.

``` dockerfile
# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.205.2/containers/typescript-node/.devcontainer/base.Dockerfile

# [Choice] Node.js version (use -bullseye variants on local arm64/Apple Silicon): 16, 14, 12, 16-bullseye, 14-bullseye, 12-bullseye, 16-buster, 14-buster, 12-buster
ARG VARIANT="16-bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/typescript-node:0-${VARIANT}

RUN npm install -g @angular/cli@13.0.1
# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# [Optional] Uncomment if you want to install an additional version of node using nvm
# ARG EXTRA_NODE_VERSION=10
# RUN su node -c "source /usr/local/share/nvm/nvm.sh && nvm install ${EXTRA_NODE_VERSION}"

# [Optional] Uncomment if you want to install more global node packages
# RUN su node -c "npm install -g <your-package-list -here>"
```

Set VSCode extensions
``` json
{
	"extensions": [
		"extensionsCode"
	],
}
```
