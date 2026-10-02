# nit 💬

[English](./README.md) | **日本語**

**あなたのエージェントが、英語で話す同僚になります。**

コーディングエージェントとは、もう毎日何時間も話しているはずです。nit は、その時間を英語の練習に変えます。作業のスピードは落としません。

対象は、英語が母国語ではないエンジニアです。ドキュメントは読めても、レビューコメントを書く、角を立てずに反対する、進捗を短く伝える、といった場面ではまだ手が止まる。こうした英語は教科書には載っていません。同僚と働くなかで身につくものです。

## 使うとこうなる

あなたがこう書いたとします。

> this function is wrong, you should rewrite it

同僚はまず質問そのものに答えてから、最後に1行だけ添えます。

```
nit: "you should rewrite it" → "could we rewrite this part?" (softer; "should" can sound like an order in reviews)
```

日本語で書いても、作業はそのまま進みます。最後に、チームに伝えるならどう言うかを見せてくれます。

```
in English: "I'm not sure this handles empty input. Can you take a look?"
```

## 特徴

- **同僚として話す**：平易な仕事の英語で返します。LGTM、blocker、flaky のような現場の言葉も使い、初めて出てきたときだけ短い説明を添えます。
- **直すのは1つだけ**：間違いを並べることはしません。仕事で一番困るものを1つだけ選びます。優先するのは意味、次に語調、最後に自然さです。
- **文法より語調**：冠詞が抜けていても気にしません。レビューコメントが失礼に聞こえるほうが問題です。
- **自分だけのフレーズ帳**：役に立つ言い回しを `~/.nit/phrasebook.md` に書きためます。教科書の例文ではなく、自分の実際の仕事から生まれた表現集です。`review my phrasebook` と言うと、3問の小テストが出ます。プロジェクトの外に書き込むので、初回はエージェントが許可を求めることがあります。
- **作業は遅くしない**：仕事が最優先です。コード、ログ、エラーメッセージには手を加えません。

## インストール

**Claude Code**

```
/plugin marketplace add 6igtree/nit
/plugin install nit@nit
```

**Codex**

```sh
git clone https://github.com/6igtree/nit.git /tmp/nit
mkdir -p ~/.agents/skills && cp -r /tmp/nit/skills/nit ~/.agents/skills/
```

## 使い方

`nit`（Claude Code では `/nit` でも可）と言うと始まり、`stop nit` で止まります。

母国語での作業から英語だけの作業へ、1段ずつ移っていけます。

| レベル | 返事 | 追加されるもの |
| --- | --- | --- |
| `nit 1` lite | 母国語 | 英語ならこう言う、の1行。初めての人はここから |
| `nit 2` bilingual | 平易な英語 | 長めの返事には、母国語の1行要約が付く |
| `nit 3` full | 英語のみ | 1メッセージにつき nit を1つ |
| `nit 4` immersion | 英語のみ | PRの説明、コミットメッセージ、進捗報告をまず自分で英語で書き、一緒に仕上げる |

レベルは `~/.nit/level` に保存され、次回も引き継がれます。nit が必要なくなってきたら、1段上がることを提案します。難しくなってきたら、1段戻ることを提案します。勝手にレベルを変えることはありません。

## 関連

[senpai](https://github.com/6igtree/senpai)：コードはエージェントが書き、エンジニアとしての学びはあなたに残します。

## ライセンス

MIT
