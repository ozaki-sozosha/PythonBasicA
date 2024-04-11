# Python基礎A
## 講義内容
### JupyterLabの使い方(Notobookとコンソール)
- [JupyterLabDesktop](https://github.com/jupyterlab/jupyterlab-desktop "Download") 

#### 日本語化
コンソールの入力欄にpip install jupyterlab-language-pack-ja-JPと入力し、実行(SHIFT+RETURN)。  
日本語ランゲージパックがインストールされます。  
インストール後「Change and relaod」ボタンをクリック。  
Settingsメニュー>LanguageにJapanese(Japan)- 日本語(日本)が追加されます。  
<img src="./images/jupyterlab_tojp.png" width="50%">
<img src="./images/setJapanese.png" width="50%">

#### 作業ディレクトリの設定
右上のハンバーガーメニューのSettings>ServerにDefault Working Directoryの項目があります。  
設定したいディレクトリ(フォルダ)へのPathを入力することでデフォルトの作業ディレクトリを変更出来ます。  

<img src="./images/defaultworkingdir.png" width="50%">

### データ型 

| データ型 | 解説 | 例 |
| ---------------- | ---------------- | ---------------- |
| str(ストラ) | 文字列 | "創造社デザイン専門学校" |
| int(イント) | 小数点を含まなない数値 | 1967 |
| float(フロート) | 小数点を含む数値 | 25.6 |
| bool(ブール) | 真偽値 |True or False | 
```
# データ型を調べるtype関数
print(type("Python"))
print(type(100))
print(type(0.1))
print(type(True))
```

### 変数
    
```
    num = 1
    print(num)
```  
* 変数名のルール  
    - 小文字のアルファベットとアンダースコアを組み合わせる  
    - 数字で始まらない  
    - 複数の単語から成る場合はアンダースコアで区切る(スネークケース)  

### 算術演算子

| 演算子 | 意味 | 例 |
| ---------------- | ---------------- | ---------------- |
| + | 足し算(加算) | 100 + 50 |
| - | 引き算(減算) | 100 - 50 |
| * | 掛け算(乗算) | 100 * 50 |
| / | 割り算(除算) | 100 / 50 | 
| // | 割り算(整数除算) | 100 // 50 | 
| % | 余り算(剰余) | 100 % 50 | 
| ** | べき乗 | 100 ** 2 | 


### コメント  
\# 行末までコメント  
""" ~ """複数行コメント
### print関数、input関数、open関数

```
# print関数(画面に出力)  
print("Python")
# input関数(キーボードから入力)
data = input("お名前を入力してください>>\n")
# open関数(ファイルを開く)
with open("data.txt","w",encoding="utf-8") as f:
    f.write("Python")
```   

### コレクション
* リスト、タプル、辞書
* リスト関数、辞書関数の使い方
* 2次元リスト

### 条件分岐と繰り返し
* 条件とbool型(比較演算子)
* if分岐、if* else分岐、if* elif* else分岐
* whileループ、forループ
* コレクションと繰り返し

### 関数
* 組込関数とユーザー定義関数
* 外部ファイル化と読込
* 標準モジュール(random,datetime,csv)

### エラー例外制御/考査
* エラーと例外処理
* 課題考査(文法の基礎試験)
