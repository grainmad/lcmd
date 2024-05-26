# 生成leetcode题解模板


## docker 部署

### methon1 手动构建镜像并运行
``` shell
# build image
docker build -t gg/leetcode-md:v1 .

# run image
docker run --name leetcode -p 1760:1760 -d gg/leetcode-md:v1
```

### methon2 docker-compose 一键部署
``` shell
# 当前目录下，启动
docker compose up -d

# 停止
docker compose down
```

## 提供接口

``` txt
# 获取json
http://你的ip:1760/json?link=n-queens

# 获取文件
http://你的ip:1760/file?link=n-queens

```

``` shell
# eg:
wget --content-disposition "http://你的ip:1760/file?link=https://leetcode.cn/problems/maximum-sum-of-subsequence-with-non-adjacent-elements/description/"
```