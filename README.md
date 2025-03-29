## 编辑器字体
#### [下载](/fonts/MapleMonoNormal-NF-CN-SemiBoldItalic.ttf)

# Homebrew下载

[下载官网](https://brew.sh/zh-cn/)

1、`brew install --cask ghostty google-chrome wechat clash-verge-rev raycast qq bob aldente rectangle stats pearcleane jordanbaird-ice keka wetype`

2、`brew install fnm zsh-syntax-highlighting zsh-completions`

3、在GitHub下载deeplx翻译

## 通过Homebrew安装本地下载的dmg文件,以网易邮箱大师为例
1 、编写mailmaster.rb文件

<pre>
cask "mailmaster" do
  version "1.0.0"  # 替换为实际版本
  sha256 "..."     # （通过 `shasum -a 256 /path/to/file.dmg` 获取）
  url "file:///Users/xx/Downloads/mail5.dmg"  # 本地路径，或替换为实际下载 URL
  name "网易邮箱大师"
  desc "Email client"
  homepage "https://www.example.com"  # 替换为官网
  app "Mailmaster.app"
end
</pre>
2 、`brew install --cask ./mailmaster.rb`


# 新Mac访问GitHub访问不到的解决办法
1、通过[IPaddress](https://www.ipaddress.com/)查询Github的IP地址，如140.82.114.4

2、编辑/etc/hosts文件添加一行 `140.82.114.4    github.com`

3、执行`sudo killall -HUP mDNSResponder`刷新dns