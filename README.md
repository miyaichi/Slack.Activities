# Slack Activities

Slack Web API（ https://api.slack.com/web#methods )のうち、最低限必要なものだけ実装しています。

## chat

### chat.postMessage


| Argument | Required | Description |
| -------- | -------- | ----------- |
| token | Required | 必要なスコープを持つ認証トークン。 |
| channel | Required | メッセージを送信するチャネル、プライベートグループ、またはIMチャネル。エンコードされたIDまたは名前になります。 |
| text | Required | 送信するメッセージのテキスト。 |
| as_user | Optional | ボットとしてではなく、正式なユーザーとしてメッセージを投稿するにはtrueを渡します。 |
| attachments | Optional | 構造化された添付ファイルのJSONベースの配列。URLエンコードされた文字列として表示されます。 |
| icon_emoji | Optional | 絵文字をこのメッセージのアイコンとして使用します。icon_urlをオーバーライドします。as_userset と組み合わせて使用​​する必要がありますfalse。それ以外の場合は無視されます。 |
| icon_url | Optional | このメッセージのアイコンとして使用するイメージへのURL。as_userfalse と設定して使用する必要があります。 |
| link_names | Optional | チャンネル名とユーザー名を検索してリンクします。 |
| mrkdwn | Optional, default=true | スラックマークアップ解析を無効にするには、に設定しfalseます。デフォルトでは有効です。 |
| parse | Optional | メッセージの扱い方を変更する。デフォルトはnone。 |
| reply_broadcast | Optional | thread_tsと一緒に使用し、チャネルまたは会話の全員に返信を表示するかどうかを示します。デフォルトはfalse。|
| thread_ts | Optional | このメッセージを返信する別のメッセージの値を指定します。返信のts値を使用しないでください。代わりにその親を使用してください。 |
| unfurl_links | Optional | テキストベースのコンテンツを展開できるようにするにはtrueを渡します。 |
| unfurl_media | Optional | メディアコンテンツの展開を無効にするには、falseを渡します。 |
| username | Optional | ボットのユーザー名を設定します。as_userをfalseと設定して使用する必要があります。それ以外の場合は無視します。 |

## conversations

### conversations.members

| Argument | Required | Description |
| -------- | -------- | ----------- |
| token | Required | 必要なスコープを持つ認証トークン。 |
| channel | Required | メンバーを取得するチャンネルID。 |

## files

### fies.upload

| Argument | Required | Description |
| -------- | -------- | ----------- |
| token | Required | 必要なスコープを持つ認証トークン。 |
| channels | Optional	|  ファイルを共有するチャネル名またはIDのコンマ区切りのリスト。|
| content	| Optional	| ファイルのコンテンツ。このパラメーターを省略する場合は、fileを指定する必要があります。 |
| file | Optional	| ファイル内容をmultipart/form-dataで送信します。このパラメータを省略する場合は、contentを指定する必要があります。 |
| filename | Optional | ファイル名。|
| filetype | Optional	| ファイルタイプ識別子。 |
| initial_comment	| Optional | ファイルの内容を説明するメッセージテキスト。 |
| thread_ts	| Optional | このファイルを返信するための別のメッセージのts値を指定します。返信のts値を使用せず、親を使用してください。 |
| title |	Optional | ファイルのタイトル。|

## users

## users.info

| Argument | Required | Description |
| -------- | -------- | ----------- |
| token | Required | 必要なスコープを持つ認証トークン。 |
| user | Required | 情報を取得するユーザー名。 |
