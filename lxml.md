## lxml 的安装

lxml 是 Python 的一个解析库，支持 HTML 和 XML 的解析，支持 XPath 解析方式，而且解析效率非常高，本节我们了解下它的安装方式，分为Windows、Linux、Mac 三大平台来介绍。

## 相关链接

* 官方网站：[http://lxml.de](http://lxml.de)
* GitHub：[https://github.com/lxml/lxml](https://github.com/lxml/lxml)
* PyPi：[https://pypi.python.org/pypi/lxml](https://pypi.python.org/pypi/lxml)

## 安装方法

### Windows 下的安装

Windows 下可以先尝试利用 pip3 安装，直接执行如下命令即可：

```
pip3 install lxml
```

如果没有任何报错则证明安装成功。

如果出现报错，比如提示缺少 libxml2 库等信息，可以采用 wheel 方式安装。

推荐直接到这里下载对应的 wheel 文件，链接为：[http://www.lfd.uci.edu/~gohlke/pythonlibs/#lxml](http://www.lfd.uci.edu/~gohlke/pythonlibs/#lxml)，找到本地安装 Python 版本和系统对应的 lxml 版本，例如 Windows 64 位 Python3.6 就选择 lxml‑3.8.0‑cp36‑cp36m‑win_amd64.whl，将其下载到本地。

然后利用 pip3 安装即可，命令如下：

```
pip3 install lxml‑3.8.0‑cp36‑cp36m‑win_amd64.whl
```

这样我们就可以成功安装好 lxml 了。

### Linux 下的安装

在 Linux 平台下安装问题不大，同样可以先尝试 pip3 安装，命令如下：

```
pip3 install lxml
```

如果报错，可以尝试下方的解决方案。

#### CentOS、RedHat

对于此类系统，报错主要是因为缺少必要的库。

执行如下命令安装所需的库即可：

```
sudo yum groupinstall -y development tools
sudo yum install -y epel-release libxslt-devel libxml2-devel openssl-devel
```

主要是 libxslt-devel libxml2-devel 这两个库，lxml依赖于它们。安装好了之后重新尝试 Pip 安装即可。

#### Ubuntu、Debian、Deepin

报错的原因同样可能是缺少了必要的类库，执行如下命令安装：

```
sudo apt-get install -y python3-dev build-essential libssl-dev libffi-dev libxml2 libxml2-dev libxslt1-dev zlib1g-dev
```

安装好了之后重新尝试 pip 安装即可。

### Mac 下的安装

在 Mac 平台下，仍然可以首先尝试 pip3 安装，命令如下：

```
pip3 install lxml
```

如果产生错误，可以执行如下命令将必要的类库安装：

```
xcode-select --install
```

之后再重新运行 pip3 安装就没有问题了。

lxml 是一个非常重要的库，比如 BeautifulSoup、Scrapy 框架都需要用到此库，所以请一定安装成功。

## 验证安装

安装完成之后，可以在 Python 命令行下测试。

```
$ python3
>>> import lxml
```

如果没有错误报出，则证明库已经安装好了。
