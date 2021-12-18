# Reactive Combat System (仮称)

## 概要

Reactive Combat System: RCS は、超越者同士の高速戦闘を表現するための戦闘システムです。戦闘はネクロニカなどに類似した、行動値をリソースとするCTB方式で行われます。最大の特徴は、行動のほとんどが能動的な選択行動：Action ではなく、事前に設定した受動的な反応行動：Reaction によって行われる点にあります。なぜでしょうか？　超越者同士の刹那の攻防、そこに一瞬の隙をついて差し込まれる援護や妨害、これら須臾の間に行われる全てを最も華麗な形で表現するためです。

## 戦闘シーンの基本フロー

- 戦闘シーンは次の3つのフェイズで構成されます。

  - 1.開始フェイズ
  - 2.メインフェイズ
  - 3.終了フェイズ

  以下では、上に示した3つのフェイズについて詳説します。

### 開始フェイズ

戦闘の前準備を行い、特殊なルールが存在する場合は、その内容をGMとPLで共有します。典型的には、次のような内容を開始フェイスで共有します。

- **戦闘に参加するキャラクターと、その所属陣営** 具体的には、PLサイドとして参加するキャラクターと、エネミーサイドとして参加するキャラクターを明確にします。第三、第四の陣営に所属するキャラクターが戦闘に参加する場合、そのキャラクターと所属陣営についても同様です。
  - ただし、GMが戦場の霧の発生を認める場合、これらの情報を一部未公開にしても構いません。この場合、未開示の情報が存在する可能性を示唆するべきです。
  - 以下のような状況では戦場の霧が発生する可能性があります。
    - 不意遭遇戦。文字通りに霧が生じているなど、視界不明瞭な状態で戦闘を行う場合。市街地や建物内で戦闘なども、不意遭遇戦となる場合になる可能性があるでしょう。
    - エネミーサイドの伏兵。この場合、GMは事前にその可能性を何らかの形で示唆し、PLに伏兵を看破する機会を与えるべきです。
- **勝利 / 敗北条件** 典型的にはエネミーサイドのキャラクターを全滅させることが勝利条件となり、PLサイドのキャラクターが全滅することが敗北条件となります。これ以外の勝利 / 敗北条件が設定されている場合、GMは開始フェイズで通知しなければなりません。

### メインフェイズ

戦闘シーンの中心となるフェイズで、実際に戦闘に係る処理を行います。メインフェーズは、更に次のサブフェイズに分けられます。

- 2-a.セットアップサブフェイズ
- 2-b.バトルサブフェイズ

以下では、上に示した2つのサブフェイズについて詳説します。

#### セットアップサブフェイズ

戦闘開始直前の準備行動を行うサブフェイズです。このサブフェイズでは、以下の処理を記述通りの順番で行います。

1. 各キャラクターの[行動値を初期化](#行動値の初期化)します。
2. [行動値の高い順](#実行権の処理順)で各キャラクターに Reaction の[実行権](#実行権)が与えられます。このタイミングで起動できるReactionは起動タイミングがセットアップサブフェイズであるものに限定されることに注意してください。

#### バトルサブフェイズ

本格的な戦闘行動を行うサブフェイズです。このサブフェイズでは、以下の処理を記述通りの順番で行います。

1. 最も行動値が高いキャラクターに Action の実行権が与えられます。最も行動値の高いキャラクターが複数いた場合の処理は[実行権の処理順](#実行権の処理順)を参照してください。
2. 勝利 / 敗北条件が満たされていた場合、戦闘を終了します。
3. 全てのキャラクターの行動値が0以下だった場合、全てのキャラクターの行動値にキャラクターそれぞれの[行動値を初期化](#行動値の初期化)します。
4. 1.に戻ります。

デッドロックが生じたなど、GMが必要と認めた場合は上記の手続きを中断し、終了フェイズに移行しても構いません。その場合、戦闘の結果や報酬についてはPLに配慮 / 相談して決定してください。

### 終了フェイズ

戦闘の結果と、PLが入手する報酬を明確にします。ただし、GMが戦闘が連続すると認める場合、終了フェイズを行わず、次の戦闘の開始フェイズに移行しても構いません。この場合、GMは連続する全ての戦闘が終了した後、全ての戦闘の報酬を忘れずに伝えなければなりません。終了フェイズでPLが入手する報酬はアイテム類です。経験点はセッション終了時に清算されます。

### 戦闘シーンの細則

#### 行動値の初期化

行動値の初期化は、以下の計算式で行います。

(初期化された行動値) = (初期化前の行動値) + (基準行動値) + 1d3

- セットアップサブフェイズでは、初期化前の行動値は 0 として扱います。

#### 実行権の処理順

実行権の処理は行動値の高いキャラクターから順番に行います。行動値が同じキャラクターが複数存在した場合、PLサイドのキャラクターが優先されます。PLサイドのキャラクター同士で行動値が同じキャラクターが複数存在した場合、PL間で相談して処理順を決定してください。PLサイドではない陣営のキャラクターで行動値が同じキャラクターが複数存在した場合、陣営に関係なくGMが処理順を決定します。

#### 実行権

実行権の概念はRCSの中核をなすものです。戦闘ルールは 1. どのタイプの実行権が 2. いつ与えられるか、という構成で記述されます。その他のルールは、全て実行権の行使に関するルールとして与えられます。

- 実行権は以下の2つです。
  - Action の実行権。 Action は能動的な選択行動です。[バトルサブフェイズ](#バトルサブフェイズ)時に与えられます。
  - Reaction の実行権。 Reaction は受動的な反応行動です。[セットアップサブフェイズ](#セットアップサブフェイズ)時に与えられます。
