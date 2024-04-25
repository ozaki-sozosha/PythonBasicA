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
#### リスト
複数のデータを要素としてまとめて取り扱う  
```
# リストを定義
numbers = [0, 10, 20, 30, 40, 50]
# リストのデータ型を確認
type(numbers)

# 文字列を要素とするリストを定義
fruits = ['apple', 'banana', 'chelly']

# indexはゼロから始まる
fruits[0]

# 要素のスライス
abcd = ['a', 'b', 'c', 'd']
abcd[1:3]
```

#### リスト関数
```
# 要素数を数える
len(numbers)

# 最大値
max(numbers)

# 最小値
min(numbers)

# 合計(要素がintやfloatの場合)
sum(numbers)

# 並べ替え(sort と sorted)

# 新しい要素を末尾に追加
fruits.append('grape')

# リストにリストを追加
fruits.extend(['orange','berry'])

# リストに要素を挿入
fruits.insert(2,'pineapple')

# 要素を指定して削除
fruits.remove('orange')

# indexを指定して削除(indexを省略すると末尾)
fruits.pop(3)

# リストのコピー
new_fruits = fruits.copy()
new_fruits
```

#### タプル
タプルは、リストと同じように複数のデータを取り扱うコレクション。
ただし、一度設定した要素を変更できません。
```
subjects = ("ICT・マーケティング","モノ・コトづくり学科")
subjects[0]

```
#### 辞書(ディクショナリ)
辞書は、キー (key) と値 (value) を対応づけるデータです。 
```
# 辞書を定義
scores = {'english':76, 'math':66, 'japanese':70, 'biology':58, 'geography':80}

# 要素を取得
scores['japanese']
scores.get('japanese')

# 要素を変更
scores['math'] = 76

# 要素を追加
scores['music'] = 80

# 要素を削除
del scores['biology']
```

#### 辞書関数
```
# 全削除
scores.clear()

# 値の一覧をリストで取得
scores.values()

# キーの一覧をリストで取得
scores.keys()
```
#### 2次元リスト
```
[
    [99, 27, 31, 53, 79, 45, 36, 80, 88, 17], 
    [83, 69, 72, 5, 50, 76, 11, 26, 10, 40], 
    [28, 94, 40, 77, 6, 43, 85, 82, 36, 43], 
    [69, 52, 45, 59, 75, 61, 31, 25, 45, 7], 
    [2, 76, 65, 29, 82, 58, 64, 52, 99, 61],
]
```

### 条件分岐と繰り返し

#### 比較演算子
| 演算子 | 意味 | 備考 |
| ---------------- | ---------------- | ---------------- |
| a < b | a は b より小さい |  |
| a <= b | a は b と等しいか小さい |  |
| a > b | a は b より大きい |  |
| a >= b | a は b と等しいか大きい |  | 
| a == b | a と b は等しい |  | 
| a != b | a と b は等しくない |  | 

#### 条件
```
#比較演算子の計算結果(条件)はbool型
print(100 > 80)
```
Falseとみなされる値  
- 0 (int型)  
- 0.0 (float型)  
- "" (空のstr型)  
- [] (要素を持たないlist型)  
- {} (キーも値も持たないdict型)  
- () (要素を持たないタプルやセット)  

Noneかどうかを判断する
- is None (Noneの時にTrue)
- is not None (Noneの時にFalse)

#### 条件分岐
条件により処理を選択する

```
# 条件がTrueになる場合、インデント内の処理を実行する
a = 80
if a < 100:
    print('変数a は 100より小さい値です')

```
Pythonではブロックの代用としてインデントを使用する
if 条件:に続く行はインデントを適切に設定し、条件に当てはまる時に実行される処理を記述する。  
注)インデント内に何も記述がないとIndentErrorが発生する。処理が未確定の時はpassと記述する。

```
# 条件がTrueになる場合、インデント内の処理を実行する。
# Falseの場合はelse:に続くインデント内の処理を実行する。
a = 80
if a < 100:
    print('変数a は 100より小さい値です')
else:
    print('変数a は 100より大きい値です')

# elif文で条件を更に追加出来る。
# 上の条件に当てはまらないが、次の条件にはあてはまる場合に使用。
# elif文はいくつでも追加が可能
a = 85
if a > 100:
    print('変数a は 100より大きい値です')
elif a < 90:
    print('変数a は 90より大きい値です')
elif a < 80:
    print('変数a は 80より大きい値です')
else:
    print('変数a は 100より大きい値です')

```
#### 論理演算子
| 演算子 | 意味 | 備考 |
| ---------------- | ---------------- | ---------------- |
| a < b and a > c | a は b より小さい なおかつ a は c より大きい | 両方True|
| a < b or a > c | a は b より小さい 又は a は c より大きい | どちらか片方がTrue |

#### in と not
```
fruits = ["apple","banana","orange","grape"]
if "banana" in fruits:
    print("バナナは果物に含まれます")

if "beans" not in fruit:
    #not in で含まれない時Trueになる
    print("豆は果物に含まれません");
```
#### While文
```
# while文は条件を満たす間、同じ処理を繰り返す構文。
c = 0
while c < 5 :
    print(c)
    c += 1
```
```
# 繰り返しを強制終了するbreak文
c = 10
while c < 100:
    print(c)
    if c == 15:
        print("繰り返しを終了します。")
        break
```
```
# 繰り返しをスキップするcontinue文
c = 0
while c < 10:
    if c == 2:
        continue
    else:
        print(c)
```
```
# ループ終了後を処理するwhile-else文
c = 0
while c < 10:
    print(c)
    c += 1
else:
    print("繰り返し処理が終了しました。")
```
#### for文
リストなど繰り返し可能なオブジェクトからひとつづつ取り出し処理をする文
```
for i in range(10):
    print(i)
```
breakやcontinueはfor文でも有効
for-elseで繰り返し終了時に処理を記述
```
#range関数
list(range(10)) #出力結果 0,1,2,3,4,5,6,7,8,9
list(range(1,10,2)) #start:1 10未満でステップは2 出力結果 1,3,5,7,9
```
#### enumerate関数
enumerate関数を使用すると繰り返し可能なオブジェクトから要素とインデックスを取り出せます
```
persons = ['マイケル','ビリー','スティービー','ボブ','シンディ']
for i, person in enumerate(persons):
    print(f'{i} 番目は{person}です')
```

### 関数

* 組込関数とユーザー定義関数
* 外部ファイル化と読込
* 標準モジュール(random,datetime,csv)

### エラー例外制御/考査
* エラーと例外処理
* 課題考査(文法の基礎試験)
