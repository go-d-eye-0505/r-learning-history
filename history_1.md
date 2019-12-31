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

### R commanderの起動

```
$ R
R version 3.6.2 (2019-12-12) -- "Dark and Stormy Night"
Copyright (C) 2019 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)

R は、自由なソフトウェアであり、「完全に無保証」です。
一定の条件に従えば、自由にこれを再配布することができます。
配布条件の詳細に関しては、'license()' あるいは 'licence()' と入力してください。

R は多くの貢献者による共同プロジェクトです。
詳しくは 'contributors()' と入力してください。
また、R や R のパッケージを出版物で引用する際の形式については
'citation()' と入力してください。

'demo()' と入力すればデモをみることができます。
'help()' とすればオンラインヘルプが出ます。
'help.start()' で HTML ブラウザによるヘルプがみられます。
'q()' と入力すれば R を終了します。

>
```

### R commanderの終了
```
> q()
Save workspace image? [y/n/c]: # Yes or No or Cancel
```

## R studioのインストール

* ダウンロードサイト
  * https://rstudio.com/products/rstudio/download/#download

## 参考サイト

* CRAN
  * https://cran.r-project.org/bin/linux/ubuntu/README.html
