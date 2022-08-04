---
title: MDN の慣習と定義
slug: MDN/Writing_guidelines/Experimental_deprecated_obsolete
tags:
  - ドキュメント
  - ガイド
  - ガイドライン
  - MDN
  - MDN メタ
translation_of: MDN/Guidelines/Conventions_definitions
original_slug: MDN/Guidelines/Conventions_definitions
---
{{MDNSidebar}}

この記事では MDN で使用されている慣習や定義、特に文書化する際に人によっては忘れがちなものを紹介します。

## 定義

### 非推奨と廃止

**非推奨**や**廃止**は技術や仕様書によく使われている言葉ですが、どのような意味でしょうか？

- 非推奨 (Deprecated)
  - : MDN において**非推奨**の用語は、もう推奨されないものの、まだ実装されており動作する可能性がある API や技術を示すために使用されます。
    最近では、 [browser-compat-data プロジェクト](https://github.com/mdn/browser-compat-data/blob/main/schemas/compat-data-schema.md)の中で使用される定義を、「その機能はもう推奨されません。将来は削除されるか、互換性のためだけに温存されている可能性があります。この機能を使用することは避けてください。」と更新しました。
- 廃止 (Obsolete)
  - : MDN において**廃止**の用語は、もう推奨されないだけでなく、ブラウザーでももう実装されていない API や技術を示すために使用されます。しかし、これは混乱しやすもののです。 — **非推奨**と似ており、区別することがさほど役立たない（こちらも本番サイトでは使用するべきではない）ものです。従って、私たちはこれを使用するのをやめ、使用されている記述を削除するか、**非推奨**に置き換えるかしてください。

### 実験的

**実験的** (Experimental) は、聞いた場所や読んだ場所の文脈によって意味が異なる可能性があります。
MDN においてある技術が実験的と記述されている場合、その技術は生まれたばかりで未熟であり、現在ウェブプラットフォームへの追加手続の途中の（または追加が検討されている）段階であることを意味します。

次の一方または両方が成り立つ場合です。

- 主要なブラウザーの中で、実装し、既定で有効になっているものが 2 つ未満である。
- 定義している仕様が、後方互換性のない方法で大幅に変更される可能性がある（つまり、その機能に依存する既存のコードを破壊する可能性がある）。

これらの定義のうちの一方または両方が成り立つ場合、その技術を様々な種類の製品プロジェクト（つまり、単なるデモまたは実験ではない場合）に使用する前に慎重に考えなければなりません。
実験的の定義については、 [browser-compat-data プロジェクト](https://github.com/mdn/browser-compat-data/blob/main/schemas/compat-data-schema.md#status-information)も参照してください。

逆に、以下のような場合は実験的とは言いません。

- 2 つ以上の主要なブラウザーで実装されている。または、
- 定義している仕様が、ウェブを壊すような形で変化することはないとみられる。

ここでは**または**が重要です。 — 通常、ある技術に複数の主要なブラウザーが対応した場合、仕様は安定するでしょうが、これは常に言えるわけではありません。また、技術によっては安定した仕様書がありよく使用されてはいるものの、ブラウザーでのネイティブな対応がない場合もあります（[IMSC](/ja/docs/Related/IMSC) などがその例）。

### アーカイブページ

アーカイブページは、 MDN の[廃止されたコンテンツのアーカイブ](/ja/docs/Archive)に保存されているページです。これらのページには古くなった情報が含まれているため、他の人にとっては直接役に立ちません。

最も一般的なのは、これらは廃止されてもはや信頼されるべきではない Mozilla プロジェクトに関係します。しかし、それらは有用な歴史的記録を形成するのでそれらを単純に削除するのではなく、その中に含まれるパターンやアイデアのいくつかは将来の作業に役立つかもしれません。 良い例は [B2G (Firefox OS) プロジェクト](/ja/docs/Archive/B2G_OS)です。

#### どのような時にページをアーカイブするか？

ページをアーカイブするべきである場合は、ページが上記の説明に合う場合です。ページをアーカイブするには、[ページ移動]機能 ([詳細] - [この記事を移動]) を使用して、ページを[アーカイブ]ページツリー (/ja/docs/Archive) に移動します。この機能を使用する権限がない可能性があります。ページのアーカイブを開始する前に、まず MDN コミュニティと話し合う必要があります - [ディスカッションフォーラム](https://discourse.mozilla.org/c/mdn/236)で私たちに相談してください。

### 削除されたページ

削除されたページは、 MDN から明示的に削除されたページです — 例えば [`SharedKeyframeList`](/ja/docs/Web/API/SharedKeyframeList) インターフェイスと [`SharedKeyframeList()`](/ja/docs/Web/API/SharedKeyframeList/SharedKeyframeList) コンストラクターを見てください。 これらのページには、もはや有用ではない情報が含まれています。また、利用可能にしておくと混乱したり、知っていたりすることが不適切な場合もあります。

次のようなものが該当する可能性があります。

- ブラウザーに実装される前に仕様から削除された API 機能のリファレンスページ。
- 後に悪い手法であることが示され、より良い技術に置き換えられた手法をカバーする記事。
- 後に他の、より質の高い記事で置き換えられた情報を含む記事。
- MDN にふさわしくない内容を含む記事。
- 古く、時代遅れで、修正が難しい翻訳記事で、すなわち英語版が推奨されて翻訳し直した方が簡単である場合。

#### どのような時にページを削除するか

上記の説明に合う場合はページを削除する必要があります。ページを削除するには、[このページを削除] 機能 ([詳細設定] > [このページを削除]) を使用してページを削除します。あなたはおそらくこの機能を使う権限を持っていないでしょう、そしてページを削除することを考えるときあなたは最初にそれを MDN コミュニティと議論するべきです - [ディスカッションフォーラム](https://discourse.mozilla.org/c/mdn)で私たちに相談してください。

### 新しい技術を記述するとき

MDN では、新しいウェブ標準技術を適切に文書化することを常に検討しています。
私達は、開発者が必要なときにすぐに新機能について学ぶことができるように文書を十分に早く公開することと、定期的に更新したり迅速に削除したりする必要がないように技術が成熟し安定したものになるように十分に遅く公開することのバランスをとるようにしています。

一般的に、新しい技術を文書化することを検討する最も早い定義は、次のとおりです。

_「この機能が標準化過程にあり、どこかで実装されている場合」_

新しい技術を文書化することを絶対的に考えるべきであるのは以下のような場合です。

- 信頼できる標準化団体 (W3C、WHATWG、Khronos、IETFなど) の下で公開された仕様書で指定されており、妥当なレベルの安定性に達している (例えば、 W3C のワーキングドラフトや候補者の勧告、あるいはそれに対して提起された問題の流れから判断すると、仕様はかなり安定しているように見えます)
- 他のブラウザー開発者が興味を引く兆しを見せており、少なくとも1つのブラウザーで一貫して実装されている場合 (有効なチケットや「実装」プロセスなど)

次のような場合は、新しい技術を文書化することにもっと慎重になるべきです（ただし、意味がある場合はそれを考慮する必要があります）。

- 仕様書がない、あるいは、変更するべきであるような大まかなメモでしかない場合
- 現在それを実装しているブラウザーがないか 1 種類であり、対応していないブラウザーが実装する様子を見せていない場合（それらのブラウザーの開発をしているエンジニアに尋ねたり、ブラウザーのバグトラッカーやメーリングリストなどを調べたりすることで評価することができます)。

次のような場合は、その新しい技術を文書化しようと考えないでください。

- ウェブに公開された技術ではない場合や、完全に私有の技術である場合
- すでに非推奨になっている、または同様の機能によって置き換えられる見込みがある

## 慣習

### 何かが仕様書から削除されたとき

新しい仕様の開発中や、 HTML のようなリビングスタンダードの進化の過程で、新しい要素、メソッド、プロパティなどが仕様書に追加され、しばらく存在してから削除されることが時々あります。これはとても速い周期で行われることもあれば、新しい項目が仕様書に数か月から数年の間、削除されずに残っていることもあります。これによって、仕様書から項目が削除されたと判断することが難しくなっています。どうするべきかを決める参考となるガイドラインをいくつか紹介します。

> **Note:** ここでは「項目」という単語を、仕様書の一部になりうるものすべてを示す意味で使用しています。要素や要素の属性、インターフェイスや個々のメソッド、プロパティ、またはインターフェイスの他のメンバーなどがこれに該当します。

- その項目が*どの*ブラウザーのリリース版でも*全く*実装されていない場合 — 設定やフラグで隠されている場合を含めて — 単純にその項目のリファレンスを文書から削除してください。

  - その項目に、その項目のみを説明するドキュメントページがある場合（例えば {{domxref("RTCPeerConnection.close()")}}）、そのページを削除してください。
    削除された項目がインターフェイスであった場合、そのインターフェイスのプロパティやメソッドを記述しているサブページもすべて削除することを意味します。
  - プロパティ、属性、メソッドなどの一覧から、その項目を削除してください。
    インターフェイスのメソッドの場合、例えば、そのインターフェイスの概要ページの「メソッド」セクションから削除することを意味します。
  - そのインターフェイスや要素などの概要ページのテキストを検索し、削除された項目への参照を探します。
    テキストの文法がおかしくなるなどの問題を残さないように注意しながら、それらの参照を削除してください。
    これは単に単語を削除するだけでなく、文章や段落をより意味のあるものに書き換えることを意味する場合もあります。
    また、項目の使用方法の説明が長い場合は、コンテンツのセクション全体を削除することもあります。
  - 同様に、関連する API や技術に関するガイドやチュートリアルの中に、その項目についての記述がないか探してください。
    それらの参照を削除し、テキストの文法がおかしくなるなどの問題を残さないように注意してください。
    これは、単に単語を削除するだけでなく、文章や段落をより意味のあるものに書き換えることを意味する場合もあります。
    また、その項目の使用に関する記述が長い場合は、コンテンツのセクション全体を削除することを意味することもあります。
  - MDN を検索して、削除された項目への参照を探し、他の場所で議論されている場合に備えてください。
    実装されていないのであれば、広く議論されることはないでしょうから、そのようなことはないでしょう。
    それらの言及も削除してください。
  - [Browser Compatibility Data リポジトリー](https://github.com/mdn/browser-compat-data) の JSON ファイルに削除された項目のデータがある場合、 JSON コードからそれらのオブジェクトを削除し、その変更を PR として提出し、コミットメッセージと PR 説明文に理由を記述してください。
    このとき、 JSON の構文を崩さないように注意してください。

- もし、その項目が 1 つ以上のブラウザーのリリースバージョンで実装されたことがあり、環境設定やフラグで隠されていたものであった場合は、その項目をドキュメントからすぐに削除しないでください。
  その代わりに、以下のように非推奨とマークしてください。

  - もしその項目が、その項目だけを説明するドキュメントページ（例えば {{domxref("RTCPeerConnection.close()")}}）であるなら、ページの先頭に [`deprecated_header`](https://github.com/mdn/yari/blob/main/kumascript/macros/Deprecated_Header.ejs) マクロを追加して、そのページのタグリストに `Deprecated` タグを追加してください。
  - 要素、インターフェイス、 API の概要ページで、仕様から削除された項目を含む項目のリストを見つけ、そのリスト内の項目名の後に [`deprecated_inline`](https://github.com/mdn/yari/blob/main/kumascript/macros/Deprecated_Inline.ejs) マクロを追加してください。
  - そのインターフェイス、要素などの概要ページの情報テキストを検索して、削除された項目への参照を探してください。
    適当な場所に警告ボックスを追加し、「●●は仕様から削除され、近日中にブラウザーから削除されます」という内容のテキストを追加してください。
    新しい方法については、\[ページへのリンク]を参照してください。
  - 同様に、関連する API や技術に関するガイドやチュートリアルに、その項目についての記述がないか探してみてください。同様の警告を追加してください。
  - 他の場所で議論されている場合に備えて、削除された項目への参照を MDN で検索してください。
    そこにも同様の警告ボックスを追加してください。
  - 将来のある時点で、ドキュメントから実際にその項目を削除することが決定されるかもしれません。通常は行いませんが、その項目が特に使われていなかったり、興味がない場合は、そうすることが決定されるかもしれません。
  - [ブラウザー互換性データリポジトリー](https://github.com/mdn/browser-compat-data)の関連する項目を更新し、影響を受ける項目が陳腐化したことを反映させてください。

- もし、その項目がブラウザーの 1 つ以上のリリースビルドで実装されたことがあり、環境設定やフラグの変更を必要としなかった場合、次のようにその項目を非推奨としてマークしてください。

  - その項目に、その項目だけを説明するドキュメントページがある場合 ({{domxref("RTCPeerConnection.close()")}} など)、 [`deprecated_header`](https://github.com/mdn/yari/blob/main/kumascript/macros/Deprecated_Header.ejs) マクロをそのページのトップに追加し、`Deprecated` タグをそのページのタグリストに追加してください。
  - 要素、インターフェース、 API の概要ページで、仕様から削除された項目を含む項目のリストを見つけ、そのリスト内の項目名の後に [`deprecated_inline`](https://github.com/mdn/yari/blob/main/kumascript/macros/Deprecated_Inline.ejs) マクロを追加してください。
  - そのインターフェース、要素などの概要ページの情報テキストを検索して、削除された項目への参照を探してください。
    適切な場所に警告ボックスを追加し、「●●は仕様から削除され、非推奨となりました。
    今後、ブラウザーから削除される可能性がありますので、使用しないでください。
    新しい方法については、\[ページへのリンク]を参照してください」のようなテキストを記入してください。
  - 同様に、関連する API や技術に関するガイドやチュートリアルに、その項目についての記述がないか探してください。同様の警告を追加してください。
  - 他の場所で議論されている場合に備えて、削除された項目への参照を MDN で検索してください。
    そこにも同様の警告ボックスを追加してください。
  - これらの項目がすぐにドキュメントから削除されることは、たとえあったとしても、まずないでしょう。
    しかし、一部またはすべての資料がサイトの [Archive](/en-US/docs/Archive) セクションに移動される可能性があります。
  - [ブラウザー互換性データリポジトリー](https://github.com/mdn/browser-compat-data)の関連する項目を更新して、影響を受ける項目の非推奨を反映させてください。

上記のガイドラインで提案されている警告メッセージの文言やその他の文章の変更については、常識的な範囲でお願いします。
項目によって、必要な言葉遣いや対処が異なります。
迷ったときは、 [Matrix](https://wiki.mozilla.org/Matrix) の [MDN Web Docs chat room](https://chat.mozilla.org/#/room/#mdn:mozilla.org) や [MDN Web Docs discussion forum](https://discourse.mozilla.org/c/mdn/236) で遠慮なく相談してください。

### MDN 内でのコンテンツのコピー

ときどき、複数のページで同じテキストを再利用する必要が生じる場合 (または、あるページを別のページのテンプレートとして利用したい場合) があります。その場合、3つの選択肢があります。

- ページ全体をコピーしたい場合。

  1. コピーしたいページを閲覧中に、**詳細**（歯車）メニュー内にある、 **[この記事を複製](/ja/docs/MDN/Contribute/Howto/Create_and_edit_pages#clone_of_an_existing_page)**を選んで下さい。
    新しいページのエディターのユーザーインターフェイスが、複製されたページの内容がすでに入った状態で開かれます。
  2. 新しい**タイトル**と**スラッグ**を、複製したページに入力します。
  3. 必要に従ってページを編集し、通常と同じように保存します。

- ページの一部分だけをコピーしたい場合は、**ページの単純なコピーアンドペーストはやめて下さい。
  **余計な HTML の断片を作成中のページに埋め込むことになり、誰かが片付けをすることになります。あなたかもしれないし、他の編集者かもしれませんが、誰もそんなことやりたくありません。
  MDN のページの一部をコピーする場合、

  1. ソースページで、**編集**ボタンをクリックします。
  2. **エディターの UI の中で再利用したい部分をコピーします。**
  3. **変更を破棄**をクリックして、エディターの UI を終了します。
  4. 貼り付けしたいページのエディターの UI を開きます。
  5. 内容をクリップボードから貼り付けします。

  > **Note:** Chrome では一般的に、エディターで文書をコピーして貼り付けた際に、コンテンツに適用されるクラスが含まれません。
  > これを行った後にコンテンツを確認し、失われたスタイルを再適用する必要があります。
  > 特に表、構文ボックス、構文の強調表示、コンテンツの非表示部分をチェックしてください。

- 文字通り、同じコンテンツを多くのページに利用したい場合もあるかもしれません。そんな時は、そのコンテンツを一つのページにまとめてしまうのがいいかもしれません。そして [`page`](https://github.com/mdn/yari/blob/main/kumascript/macros/page.ejs) マクロを利用して、一つのページから他のページへ素材を転写しましょう。こうすると、参照元のページが更新されると、参照先のページの内容も同様に更新されます（これは強制的に更新したり、参照先のページが定期的に再構築されたりした際に起こります）。

#### 他の場所からの内容のコピー

多くの場合、MDN 以外にもウェブ上のどこかにトピックに関する有用なコンテンツがあります。しかし、そのようなコンテンツをコピーすることは、法的にも技術的にも困難を伴うことがあります。

技術的なレベルでは、検索エンジンは通常他の場所で利用可能なコンテンツを再生するために彼らのランキングでサイトにペナルティを課します。したがって、MDN のコンテンツの検索エンジンのランキングを向上させるために、MDN にオリジナルのコンテンツを含めることが好ましいです。MDN から既存のコンテンツにリンクできます。

法的なレベルでは、あなたはコンテンツを寄付する権限を与えられなければならず、そしてそれは [MDN のライセンス](/ja/docs/MDN/About#copyrights_and_licenses)と互換性のある方法でライセンスされそして帰属しなければなりません。

- **既存のコンテンツを作成し** (あなた自身の目的のためであり、仕事用としてではなく)、それを MDN のライセンスの下で MDN に寄付する意思がある場合、これが最も簡単なケースであり、自由にコンテンツを寄付できます
- **コンテンツの著作権が他の人に帰属する場合**、それは MDN のライセンスと互換性があるようにライセンスされている必要があります。弁護士ではない人にとって、互換性のあるライセンスを判断するのは容易ではありません。安全のため、必要に応じて [MDN スタッフチーム](https://wiki.mozilla.org/MDN#Staff_Team)のメンバーに連絡してください

#### 仕様書が競合したときの調整方法

なお、時々 (まれに) 仕様書の異なるバージョン (特に W3C と WHATWG) が競合することがあり、例えば一方のバージョンがある機能を非推奨とする一方で、もう一方が非推奨にしない場合などがあります。このような場合、何が真実なのか — 例えば、ブラウザーは実際にどうしているか — を考慮し、「重要」なメモを書いて最新の状態を要約してください。例えば、 2019 年 1 月時点の [`inputmode`](/ja/docs/Web/HTML/Global_attributes/inputmode) グローバル属性には競合があり、次のように要約されています。

> **Warning:** 仕様の衝突: WHATWG 仕様では `inputmode` がリストアップされており(https://html.spec.whatwg.org/multipage/interaction.html#attr-inputmode)、最近のブラウザーはこれに対応する方向で動いています。
> しかし[W3C HTML 5.2 仕様書](https://html.spec.whatwg.org/multipage/index.html#contents)はこれをリストアップしていません（つまり廃止とマークしています）。
> コンセンサスが得られるまでは、 WHATWG の定義が正しいと考えるべきでしょう。