# <img src="https://cdn.icon-icons.com/icons2/2107/PNG/512/file_type_docker_icon_130643.png" width="50"/>Docker with VsCode Remote Container

## About Docker
什麼是 Docker？- https://aws.amazon.com/tw/docker/ <br>
Visual Studio Code 使用 Remote Container 建立專案開發環境- https://www.tpisoftware.com/tpu/articleDetails/2575#id6 <br>
[ 前端新手技能樹 ] #1 VS Code、Docker 與開發環境建置- https://www.youtube.com/watch?v=CxNm-3EedyA

## What do I need to prepare

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2d/Visual_Studio_Code_1.18_icon.svg/1024px-Visual_Studio_Code_1.18_icon.svg.png" width="50"/>&nbsp;
<img src="https://microsoft.github.io/vscode-remote-release/images/remote-containers-blue.svg" width="50"/>&nbsp;
<img src="https://cdn.icon-icons.com/icons2/2107/PNG/512/file_type_docker_icon_130643.png" width="50"/>


## How to add angular cli in image
add this row in dockerfile <br>
``` dockerfile
RUN npm install -g @angular/cli@yourversion 
```

