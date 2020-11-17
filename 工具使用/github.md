本地已经存在的项目如何跟github发生关联
    -git init 
    -git add .
    -git commit -am 'initial commit'
    -git remote add origin git@github.com:dfa/sku.git
    -push -u origin master  #可能需要先pull

github下载超慢
    -尽量避免项目很大，将图片等进行上传
    -在之后pull和push代码应该不会太影响速度     


git remote -v	# 查看当前远程仓库地址
git remote set-url origin <new url>
git config --global --list   // 查看当前git的配置信息

git config --global user.name "username"
git config --global user.email "email"

git fetch --all && git reset --hard origin/master && git pull

git branch --set-upstream-to=origin/remote_branch  your_branch   # 关联分支