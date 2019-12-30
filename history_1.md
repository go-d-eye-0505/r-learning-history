Installation R Language
===

## インストールするにあたって

* Rのインストール
  * ゲストOSのubuntuに直接インストール
  * (余裕ができたらdockerで)
* RのIDEであるR stucioのインストール
  * ホストOSのmacにダウンロード&インストール
    * と思ったらできなかったからゲストOSに入れる

## Rのインストールコマンド

```
$ echo -e "\n## For R package"  | sudo tee -a /etc/apt/sources.list
$ echo "deb https://cran.rstudio.com/bin/linux/ubuntu $(lsb_release -cs)-cran35/" | sudo tee -a /etc/apt/sources.list
$ deb https://cran.rstudio.com/bin/linux/ubuntu bionic-cran35/
$ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
$ gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
$ gpg -a --export E298A3A825C0D65DFD57CBB651716619E084DAB9 | sudo apt-key add -
$ sudo apt update
$ sudo apt install r-base
```

## R studioのインストール

* ダウンロードサイト
  * https://rstudio.com/products/rstudio/download/#download

## 参考サイト

* CRAN
  * https://cran.r-project.org/bin/linux/ubuntu/README.html
