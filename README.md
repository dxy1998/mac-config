## fonts
#### [字体](/fonts/MapleMonoNormal-NF-CN-SemiBoldItalic.ttf)

## 输入法配置
#### 使用[Rime](https://rime.im/)自定义输入法

##### 下载方法：
`brew install --cask squirrel`

Rime-config文件夹下所有文件复制到~/Library/Rime文件夹下，然后重新部署

## homebrew
Homebrew下载地址

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

然后下载软件

`brew install --cask clash-verge-rev ghostty wechat`

`brew install --cask raycast qq visual-studio-code snipaste rectangle aldente pearcleaner bob jordanbaird-ice keka neteasemusic stats mos monitorcontrol `


## 通过Homebrew安装本地下载的dmg文件
### 以网易邮箱大师为例
1 、编写mailmaster.rb文件

<pre>
cask "mailmaster" do
  version "1.0.0"  # 替换为实际版本
  sha256 "..."     # 替换为文件的 SHA256 校验码（通过 `shasum -a 256 /path/to/file.dmg` 获取）
  url "file:///Users/xx/Downloads/mail5.dmg"  # 本地路径，或替换为实际下载 URL
  name "网易邮箱大师"
  desc "Email client"
  homepage "https://www.example.com/mailmaster"  # 替换为官网
  app "Mailmaster.app"
end
</pre>
2 、`brew install --cask ./mailmaster.rb`
