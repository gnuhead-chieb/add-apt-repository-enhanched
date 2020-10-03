# add-apt-repository-enhanched
シェルスクリプトで記述された高機能なadd-apt-repositoryです。

昔OS標準のadd-apt-repositoryがバグって動かなくなったときに代用品として自作したものですがこのまま闇に埋もれてしまうのは哀しいですので公開します。

## インストール
```
wget https://github.com/gnuhead-chieb/add-apt-repository-enhanched/raw/main/add-apt-repository
sudo mv /usr/bin/add-apt-repository /usr/bin/add-apt-repository.bak
sudo cp ./add-apt-repository /usr/bin/
sudo chmod +x /usr/bin/add-apt-repository
```

## 使用法
```
add-apt-repository [options] repository

Options:
  -h, --help        このヘルプを表示して終了します。
  -y, --yes         全ての確認を同意したものとみなしてそのまま続行する。
  -r, --remove      指定されたリポジトリを消去する。
  -e, --exc-src     ppaリポジトリでソースコードを登録しない。
  -v, --ppaver=ARCH ppaリポジトリでバージョンを個別に指定する。 （未実装）
  -u, --update      リポジトリを追加/削除したあとにパッケージリストの更新を行う
  ```
  
  
  ## 今後やること
  - -v オプションの実装
  - Debian系だがUbuntu系でないディストリビューションでppaリポジトリが追加できない問題の修正
  - 多言語化
  
