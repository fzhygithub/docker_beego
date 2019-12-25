echo "# docker_beego" >> README.md
git init
git add *
git commit -m "first commit"
git remote add origin https://github.com/fzhygithub/docker_beego.git
git push -u origin master

#https://yq.aliyun.com/articles/57247?spm=a2c4e.11153940.0.0.ab4b4fa4qYacsH
#docker run -it --name my-go-web-demo -p 8080:8080  -v /app/go/src/go-web-demo:/go/src/go-web-demo -w /go/src/go-web-demo go-web-demo
#接下来，我们对执行的命令做一些简单的解释：
docker run命令可用于通过镜像运行容器
-it标记使用交互式模式启动该容器
--name my-go-web-demo 将容器命名为my-go-web-demo
-p 8080:8080将容器8080端口映射到主机8080端口上，最终我们可以通过主机的8080端口访问容器里的内容
-v /app/go/src/go-web-demo:/go/src/go-web-demo，使用volume将/app/go/src/go-web-demo从计算机映射至容器的/go/src/go-web-demo目录
-w /go/src/go-web-demo 设置容器的工作目录
go-web-demo 指定了容器使用的镜像名称
当容器启动以后，我们可以通过访问http://localhost:8080来验证容器是否运行正常。
