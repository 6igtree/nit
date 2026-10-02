# nit 💬

**Your agent, now an English-speaking teammate.**

You already talk to your coding agent for hours every day. nit makes those hours English practice, without slowing down the work.

It is built for engineers whose first language is not English: you read docs fine, but writing a review comment, pushing back politely, or giving a quick status update still takes effort. Textbooks do not teach that. Teammates do.

## What it looks like

You write:

> this function is wrong, you should rewrite it

Your teammate answers the actual question, then adds one line:

```
nit: "you should rewrite it" → "could we rewrite this part?" (softer; "should" can sound like an order in reviews)
```

Write in your own language and it still does the work, then shows you how to say it to your team:

```
in English: "I'm not sure this handles empty input. Can you take a look?"
```

## How it works

- **Talks like a teammate.** Plain workplace English, real expressions like LGTM, blocker, and flaky, with a short gloss the first time.
- **One nit, at most.** Never a list of mistakes. It picks the one thing that matters at work: meaning first, then tone, then naturalness.
- **Tone over grammar.** A missing article is fine. A review comment that sounds rude is not.
- **Your own phrasebook.** Useful phrases go to `~/.nit/phrasebook.md`, built from your real work. Say `review my phrasebook` for a 3-question quiz. Your agent may ask permission the first time it writes outside your project.
- **Never slower.** The work comes first. Code, logs, and error messages are never touched.

## Install

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

## Usage

Say `nit` (or `/nit` in Claude Code) to start. Say `stop nit` to stop.

Move from your own language to full English one step at a time:

| Level | Replies | Extra |
| --- | --- | --- |
| `nit 1` lite | Your own language | One line of how to say it in English. Default. |
| `nit 2` bilingual | Plain English | A one-line summary in your language for longer replies. |
| `nit 3` full | English only | One nit per message. |
| `nit 4` immersion | English only | You draft PR descriptions, commit messages, and status updates in English first, then polish them together. |

nit remembers your level in `~/.nit/level`. When your messages need fewer nits, it suggests moving up. When things get hard, it suggests stepping back. It never switches on its own.

## See also

[senpai](https://github.com/6igtree/senpai): your agent writes the code, and you still learn the engineering.

## License

MIT
