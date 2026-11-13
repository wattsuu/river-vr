河川VR教材 完成版テンプレート

【入っているもの】
・index.html
  多摩川のイラスト上から地点1〜6を選ぶページです。

・viewer.html
  選んだ地点の360°動画を再生する共通ページです。
  6地点すべて同じ viewer.html を使います。

【準備】
1. images フォルダに、多摩川のイラストを
   tamagawa-map.png
   という名前で入れてください。

2. videos フォルダに360°動画を次の名前で入れてください。
   point1.mp4
   point2.mp4
   point3.mp4
   point4.mp4
   point5.mp4
   point6.mp4

3. VS Code の Live Server などで index.html を開いてください。
   HTMLファイルを直接ダブルクリックするより、Live Serverで確認することをおすすめします。

【地点マーカーの位置変更】
index.html の次の部分を変更します。

.p1 { top: 26%; left: 14%; }
.p2 { top: 35%; left: 29%; }
...

left を大きくすると右へ、
left を小さくすると左へ、
top を大きくすると下へ、
top を小さくすると上へ動きます。

【地点名・説明・動画名の変更】
viewer.html の「const pointData = { ... }」を書き換えます。

例：
1: {
  title: "奥多摩",
  description: "川幅や河原の石に注目して観察しよう。",
  video: "videos/point1.mp4"
}

【注意】
360°動画の表示には A-Frame をインターネットから読み込みます。
学校で利用するときは、サイトをインターネット上に公開した状態で使う想定です。
