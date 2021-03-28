# 大阪思い出のこしマップ
* 大阪市立図書館の「思い出のこしプロジェクト」で公開しているデータを地図で閲覧するツールです。
  * https://www.oml.city.osaka.lg.jp/index.php?page_id=1301
* 地図上から図書館アイコンをクリックすると、その図書館に寄せられた思い出が表示されます。
* 個々の思い出へのリンクURLを用意しています。誰かに思い出を伝えたい時にご利用ください。
* 左上の下向けの矢印をクリックするとリスト表示され、カテゴリーやキーワードで検索が出来ます。

# Community MapMakerを利用しています
* 開発中ですが、ある程度動作するのでデモンストレーション的に思い出のこしマップを作りました。
  * https://github.com/K-Sakanoshita/community_mapmaker
* 技術者向けに簡単に説明すると、SPA(Single Page Application)で開発しています。
  * バックエンドはOpenStreetMapのOverpass API。また、Googleスプレッドシートのスクリプトで簡単なAPIを作っています。
* 「思い出のこし」のデータはGoogleスプレッドシートから読み込んでいるのでデータ更新は簡単です。
* 図書館の座標はOpenStreetMapから取得しており、その座標の上に思い出をリスト表示する挙動です。
* OpenStreetMapのデータをOverpass APIで取得する機能は搭載済みですが、今回は図書館だけなので無効にしてAPIの返答をファイル化して読み込んでいます（APIサーバー側の負担削減と高速化）
* データの投稿機能やOpenStreetMapのタグによって挙動を変化する機能などを開発後、Community MapMakerは初期バージョンとして公開予定です。
