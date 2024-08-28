# utools_find_macos
因为我之前一直用自己写的Linux端的搜索文件的插件，习惯了，所以这里搬过来。

## 安装

1. 在utools插件商店搜索 “find for macOS” 安装
2. 或在这里下载安装包，拖动安装包时打开utools窗口即可拖进去，点击安装

## 使用

请务必安装[fd-find](https://github.com/sharkdp/fd#installation)，安装方式:

```shell
brew install fd
```

brew自行安装

## 常用配置

- 配置文件在`.config/findlinux/find.sh`
- 设置fd-find的参数，修改配置文件中的`result`字符串
- 指定搜索的根目录，默认是`~/Documents`。多个搜索根目录就写多个`--search-path`，例如：
  
  ```shell
  result=$($cmd --search-path ~/笔记 --search-path ~/Documents --search-path ~/Desktop -Fa $1)
  ```

## 问题排查

- 搜索无结果：可能是因为搜索目录下文件太多了，比如`~` (用户的家目录)。需要调整`--search-path` 
