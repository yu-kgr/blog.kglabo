+++
author = "@yu-kgr"
categories = ["TIL"]
tags = [""]
date = "2018-10-05"
description = "2018/09 - One week I Learned | 一週間で知った事・学んだ事の個人的な備忘録"
featured = "/img/til/til.jpg"
featuredalt = "til"
featuredpath = "https://kglabo.com"
title = "2018/09 - One week I Learned"
type = "post"
draft = "true"
+++

# 今週、知った/学んだこと

## 2018/10/01- Learned

09月01日（月）のToday I Leaned.

### Java

基本的に、下記のような形でコードを記載していく。

```java
// こんな形で記載していく
class クラス名(){
  フィールド1;
  フィールド2;
  フィールド3;
  ...

  メソッド1{
  }
  メソッド2{
  }
  メソッド3{
  }
  ...
}
```
各項目について図で記載するとこんな感じ。

| 名称 | 内容 |
|---|---|
| クラス（Class） | まんまクラス。設計図的なやつ |
| メソッド（Method） | まんまメソッド。実行処理的なもの |
| フィールド（Field） | JSでいうとオブジェクトなような変数なようなもの |

## 2018/10/02- Learned

09月02日（火）のToday I Leaned.

### Java

#### メソッドの記述方法

```java
[アクセス修飾子] [戻り値の型] メソッド名(引数1,引数2,引数3...){
	（メソッドの処理内容）
}
```

#### アクセス修飾子

- 修飾した変数・メソッドなどに対してスコープをつける事ができる

| 名称 | アクセス可能（同一クラス / 同一パッケージ / サブクラス / すべて）|
|---|---|
| public | ⭕ / ⭕ / ⭕ / ❌ | 
| protected | ⭕ / ⭕ / ⭕ / ❌ |
| 指定なし(デフォルト) | ⭕ / ⭕ / ❌ / ❌ |
| private | ⭕ / ❌ / ❌ / ❌ |

#### パッケージ

- クラスに対してパッケージというものでラベリングする事が可能

## 2018/10/03- Learned

09月03日（水）のToday I Leaned.

### Sketch

IllustratorとかPhotoshopと比較してのSketchの概念の📝

#### データ構造について

- abode系ツールと比較した場合、アートボードとかレイヤーの構成が異なっているので改めて違いを記載。

| 名称 | 説明 |
|---|---|
| ページ（Page）| 各アートボードをまとめる概念的な存在 |
| アートボード（Artboard）| イラレ/フォトショで例えると新規ファイルに該当 |
| レイヤー | 短径やらエン欠やらテキストなどのオブジェクトを含むもの |

従来のオーサリングツールではアートボード毎にファイルを分割していたが、  
ページという概念がある事により、1つのsketchファイルにまとめる形となっている。

### 昨今のデザイン周辺ツール

デザインツール周りの運用においてのワークフロー考える為にいったん、適当に一覧化してまとめる。

| 名称 | 対応（モックアップ作成 / プロトタイプ共有 / インスペクト / バージョン管理） |
|---|---|
| Sketch | ⭕ / ❌ / ❌ / ❌ |
| Zeplin | ❌ / ⭕ / ⭕ / ❌ ※inVisionに食われた感 |
| inVision | ❌ / ⭕ / ⭕ / ❌ |
| prott | ❌ / ❌ / ⭕ / ❌ |
| Abstract | ❌ / ⭕ / ❌ / ⭕ ※共同編集可能 |
| GitHub | ❌ / ❌ / ❌ / ⭕ |
| inVisionStudio | ⭕ / ⭕ / ⭕ / ⭕ |

#### デザインワークフロー案

1. Sketch + inVision + GitHub / チーム内で完結する場合
2. Sketch + inVision + Abstract / 横展開する場合
3. inVisionStudio / 詳細がわからんが思い切る場合

## 2018/10/04- Learned

09月04日（木）のToday I Leaned.

### どういうUIにしたいのか迷ったときにみるもの

| しりたい事 | URL |
|---|---|
| スマホのUIをアクション毎にみたい | <https://pttrns.com/> |
| スマホのUIの動きをみたい | <https://uimovement.com/> |
| 他の方が作成したSketchデータがみたい | <https://www.sketchappsources.com/> |
| レスポンシブデザインのサイトがみたい | <http://responsive-jp.com/> |
| ベースカラー以外の色をきめたい | <https://www.materialpalette.com/> |

## 2018/10/05- Learned

09月05日（金）のToday I Leaned.

- eee

---

## 今週の感想

- fff
