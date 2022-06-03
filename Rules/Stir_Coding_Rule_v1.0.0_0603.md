# Stir Coding Rule

Created at: June 1, 2022 10:40 PM

Language: English, Japanese

Reference1: https://realpython.com/python-pep8/

Reference2: https://qiita.com/naomi7325/items/4eb1d2a40277361e898b

# English

## Why do we need this?

Consistency of naming and commenting style will make readable code and ensure maintainability.

We will use PEP8 for python standard and also use part of SET coding standard in Stir.

SET coding standard is from Conestoga College which resides in Ontario, Canada.

## Source Code Commenting

Source code commenting is done through Header Comments and Inline Comments.

This is one of the important things that developer can do while they code along.

Header comments comes with three different forms: **File**, **Class**, and **Function** header comments.

In Stir, the **header comments** should be written by **English** and inline/block comments can be written in either Japanese or English.

### File Header

File header comments are important in conveying information about your thought process to the reader. File header comments are **found at the start of each source file** you create.(Before imports)

File header comment includes following information:

- File Name
- Description - Describe functionalities of source file includes.

    ```python
    """
    FILE        : example.py
    DESCRIPTION : This file contains XXXXX functionality of ..... part of this project.
    """
    ```


### Class Header

Class header comments are to tell the reader all about the class such as:

- What does the class model? What does it represent?
- What are the features and capabilities of the class?
- What other classes does this class relate to and how?

The class header comments are found in the source file before the class is declared.

```python
"""
NAME    : ExampleClass
PURPOSE : The Example class has been created to <<What it do>>
"""
```

### Function Header

Function header comments are found at the start of each and every function that you write in your source files.

Function header comments includes following information:

- Function - Function name.
- Description - Describe functionalities of the function does.
- Parameters - List of parameters the function takes.
    - The types of the parameters are optional.
- Returns - If function has any returns, write it here.
    - If there is no returning value, write “None”

    ```python
    """
    FUNCTION    : my_example_function
    DESCRIPTION : This function <<write what it does>>
    PARAMETERS  : int instance_count   : instance count
    							string instance_name : name of the instance
    RETURNS     : boolean result : result of the instance check
    """
    ```


### Other Comments

These comments are used to inform the reader about major code blocks, difficult to understand or obscure code, about workarounds that were implemented for unexpected problems, etc. Generally inline comments are used to document the flow of logic within your source code.

There are two types of comments: **inline comments** and **block comments.**

Key points to remember when adding comments to the code in common are:

- Limit the line length of comments to 72 characters. (if planning to use docstring, this is important)
- Use complete sentences, starting with a capital letter.
- Make sure to update comments if you change your code.

**Inline Comments**

Inline comments explain a single statement in a piece of code. They are useful to remind you, or explain to others, why a certain line of code is necessary.

Inline comments tips:

- Use inline comments sparingly.
- Write inline comments on the same line as the statement they refer to.
- Separate inline comments by two or more spaces from the statement.
- Start inline comments with a `#` and a single space, like block comments.
- Don’t use them to explain the obvious.

```python
x = 5  # This is an inline comment
```

**Block Comments**

Use block comments to document a small section of code. They are useful when you have to write several lines of code to perform a single action, such as importing data from a file or updating a database entry. They are important as they help others understand the purpose and functionality of a given code block.

Block comments tips:

- Indent block comments to the same level as the code they describe.
- Start each line with a `#` followed by a single space.
- Separate paragraphs by a line containing a single `#`.

```python
for i in range(0, 10):
    # Loop over i ten times and print out the value of i, followed by a
    # new line character
    print(i, '\n')
```

## Naming Conventions

Whenever possible, use the same words to form identifiers in your programs that you use in analysis and design.

- There should only be one variable declaration per line of code.
- Spell words out. Do not use arbitrary abbreviations.
- Use constants/variables instead of literals (magic numbers) within your code.
    - There are exceptions to this rule depending on the context.
- Avoid global variables whenever possible.

The table below outlines some of the common naming styles in Python code and when you should use them:

| Type | Naming Conventions | Examples | Case |
| --- | --- | --- | --- |
| Function | Use a lowercase word or words. Separate words by underscores to improve readability. | function, my_function | Snake |
| Variable | Use a lowercase single letter, word, or words. Separate words with underscores to improve readability. | x, var, my_variable | Snake |
| Class | Start each word with a capital letter. Do not separate words with underscores. This style is called camel case. | Model, MyClass | Pascal |
| Method | Use a lowercase word or words. Separate words with underscores to improve readability. | class_method, method | Snake |
| Constant | Use an uppercase single letter, word, or words. Separate words with underscores to improve readability. | CONSTANT, MY_CONSTANT, MY_LONG_CONSTANT | Upper |
| Module | Use a short, lowercase word or words. Separate words with underscores to improve readability. | module.py, my_module.py | Snake |
| Package | Use a short, lowercase word or words. Do not separate words with underscores. | package, mypackage | Lower |

**Note**: Never use `l`, `O`, or `I` single letter names as these can be mistaken for `1` and `0`, depending on typeface.

```python
O = 2  # This may look like you're trying to reassign 2 to zero
```

# 日本語

## なぜ必要か

命名規則やコメントのルール決めをしておくことによって可読性や保守性を確保するため。

StirではPythonはPEP8基準に加え、SETのコーディングルールを一部適用しています。

## ソースコードのコメント

開発者がコードを書きながらできる重要なこととの一つとして**ソースコードのコメント**があります。

ソースコードのコメントは、ヘッダーコメントとインラインコメントを使用します。

ヘッダーコメントには**ファイル**、**クラス**、**ファンクション（関数）**の3種類の形式があります。

シングルクオートとダブルクオートはどちらもでも大丈夫です。

Stirでは**ヘッダーコメント**は**英語**でインライン・ブロックコメントはどちらの言語でも良いとします。

### ファイルヘッダー

ファイルヘッダーコメントは、開発者の思考過程を伝えるための重要な情報の一つです。

ファイルヘッダーコメントは**各ソースファイルの先頭**に書きます。(import等の前)

ファイルヘッダーコメントには以下の情報が含まれます。

- ファイル名
- 説明 - ソースファイル内での処理の説明などを記載します。

```python
"""
FILE        : example.py
DESCRIPTION : This file contains XXXXX functionality of ..... part of this project.
"""
```

### クラスヘッダー

クラスヘッダーコメントは、読み手にクラスについて以下の情報を伝えるために書きます。

- クラスのモデルやなにを示しているのか。
- クラスの特徴や機能。
- 他クラスとの関係。

クラスヘッダーコメントはソースファイル内のクラス宣言の前に書きます。

```python
"""
NAME    : ExampleClass
PURPOSE : The Example class has been created to <<What it do>>
"""
```

### 関数ヘッダー

関数ヘッダーコメントはソースファイル内の各関数宣言の前に書きます。

関数ヘッダーコメントは以下の情報を含みます。

- 関数 - 関数名。
- 説明 - 関数内での処理の説明などを記載します。
- パラメータ - 関数が取るパラメータのリスト。
    - パラメータの型はあればいいが、必須ではない。
- 戻り値 - 関数に戻り値がある場合、記載します。
    - 戻り値がない場合はNoneなど書きます。

```python
"""
FUNCTION    : my_example_function
DESCRIPTION : This function <<write what it does>>
PARAMETERS  : int instance_count   : instance count
							string instance_name : name of the instance
RETURNS     : boolean result : result of the instance check
"""
```

### その他のコメント

このコメントは、主なコードブロック、理解しにくいコード、不明なコード、予期せぬ問題に対して実装された回避策などについて、読者に知らせるために使用されます。一般的にインラインコメントは、ソースコード内のロジックの流れを記録するために使用されます。

コメントには**インラインコメント**と**ブロックコメント**の2種類の形式があります。

コード内でコメントを書く際の共通注意ポイントは以下の通りです。

- コメントの長さを**72文字**に制限する。
- 大文字から始まる文章を作成する。
- コードに変更があっら場合は、必ずコメントを更新してください。

**インラインコメント**

インラインコメントはコード内の1つステートメントを説明するものです。

また、とある行がなぜ必要なのか、自分自身や他の人に説明するのに便利なものです。

インラインコメントチップス:

- インラインコメントは控えめに使用する。
- 参照するステートメントと同じ行に記載する。
- インラインコメントは、ステートメントと2つ以上のスペースで区切ります。
- インラインコメントは、ブロックコメントと同様に `#` と空白1つで始めます
- 明らかなことを説明するためには説明しないようにしてください。

```python
x = 5  # This is an inline comment
```

**ブロックコメント**

ブロックコメントは、コードの一部分を文書化するために使用します。
ブロックコメントは、ファイルからデータのインポートやDBエントリの更新など、1つのアクションを実行するために数行のコードを記述する際にあると便利です。

故に、目的と機能を他の人が理解するのに役に立ちます。

ブロックコメントのチップス:

- ブロックコメントは記述するコードと同じインデントレベルに収めます。
- 各行の先頭は`#` で始め、その後スペースを1つ入れます。
- 段落の区切りには`#`1行入れる。

```python
for i in range(0, 10):
    # Loop over i ten times and print out the value of i, followed by a
    # new line character
    print(i, '\n')ｙ
```

## 命名規則

できる限り、プログラムの識別子には分析や設計に使用する名称と同じ単語を使用してください。

- 変数の宣言は1行につき1つだけにしてください。
- 単語はなるべく正確に書き、任意の略語は使用しないでください。
- コード内ではマジックナンバーではなく、定数や変数を使用してください。
    - ただし、文脈によっては例外あり。
- グローバル変数はできるだけ使用しないでください。

以下の表は、PEP8で定められている命名方法の概要:

| 種類 | 命名規則 | 例 | Case |
| --- | --- | --- | --- |
| 関数 | 全小文字 + アンダースコア区切り | function, my_function | Snake |
| 変数 | 全小文字 + アンダースコア区切り | x, var, my_variable | Snake |
| クラス | 最初大文字 + 大文字区切り | Model, MyClass | Pascal |
| メソッド | 全小文字 + アンダースコア区切り | class_method, method | Snake |
| 定数 | 全大文字 + アンダースコア区切り | CONSTANT, MY_CONSTANT, MY_LONG_CONSTANT | Upper |
| モジュール | 全小文字 なるべく短くアンダースコア可 | module.py, my_module.py | Snake |
| パッケージ | 全小文字 なるべく短くアンダースコア非推奨 | package, mypackage | Lower |

**メモ**: `l`, `O`, や `I` の一文字は書体によって `1`や`0`に間違われることがあるので、変数名として使用しないでください。

```python
O = 2  # ゼロに2を代入しているように見える
```
