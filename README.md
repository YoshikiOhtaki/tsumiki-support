# つみき サポート・お問い合わせ

つみき（Tsumiki）の全アプリ共通のサポート / お問い合わせページです。
GitHub Pages で公開し、各アプリの App Store「サポートURL」に設定して使います。

## 公開手順（GitHub Pages）

1. このリポジトリを GitHub 上に作成し、`index.html` / `.nojekyll` / `README.md` をアップロード（または push）する
2. リポジトリの **Settings → Pages** を開く
3. **Build and deployment → Source** を「Deploy from a branch」に設定
4. **Branch** を `main` / `/ (root)` にして **Save**
5. 数十秒〜数分で公開 URL が発行される

> 無料アカウントで GitHub Pages を使う場合、リポジトリは **Public** にしてください。

公開 URL の形式：
`https://<ユーザー名>.github.io/<リポジトリ名>/`
例：`https://yoshikiohtaki.github.io/tsumiki-support/`

## App Store Connect での使い方（アプリが増えても作り直し不要）

このリポジトリは **一度作れば全アプリで使い回せます**。アプリが増えても、
新しいリポジトリを作る必要も、このページを編集する必要もありません。

各アプリの **サポートURL** に、アプリ名を付けたURLを設定するだけです：

```
https://<ユーザー名>.github.io/<リポジトリ名>/?app=オシカド
https://<ユーザー名>.github.io/<リポジトリ名>/?app=逆算学習プランナー
https://<ユーザー名>.github.io/<リポジトリ名>/?app=固定費カット
```

`?app=` を付けると、件名が自動で `[アプリ名] お問い合わせ` になり、
ヘッダーにアプリ名が表示され、アプリ選択リストは自動で非表示になります。
**新アプリは `?app=新アプリ名` を設定するだけ**で対応完了です。

`?app=` を付けない素のURL（`.../<リポジトリ名>/`）は、全アプリ共通の
お問い合わせハブとして表示されます（直接アクセス用）。

## メールアドレス

問い合わせ先は `tsumikiapps@gmail.com`。
変更する場合は `index.html` 内の `tsumikiapps@gmail.com`（複数箇所）を置換してください。

## 任意：ハブのアプリ一覧を更新したいとき

素のURLで表示される「アプリを選んで問い合わせ」の一覧を最新に保ちたい場合のみ、
`index.html` のボタン（`<a class="btn btn-app" ...>`）を複製して
`data-subject` のアプリ名と表示ラベルを変更します。
※ `?app=` 運用だけなら、この編集は不要です。

## ファイル

- `index.html` … サポートページ本体（単一ファイル・外部依存なし）
- `.nojekyll` … GitHub Pages の Jekyll 処理を無効化（そのまま配置）
