# Brass_HP

## 主な変更点
- レスポンシブデザイン
- スマホでも年間予定の説明が読めるようにした
- ライトモード、ダークモードに対応
- シンプルな配色にした
- 写真を2024年の活動に変更

## 問題点
- androidでダークモード対応していない
(ios,windows,Ubuntu desktopでは対応していることを確認済み)

## 更新用テンプレート
すべて1つのcssファイルで管理しているため他のhtmlファイルでもこのcss classは利用できますが、コピペしやすいようにまとめたものです。
### index.html
要素の下に青線を引き、区切りたいとき
``` html
<div class="divider">
要素の下に青線
</div>
```
例
下記コードの時写真のようになります。
``` html
   <div class="divider">
        <b><font color="red">新入団員  募集中！</font></b></br>
        お問い合わせ  <a class="link_color" href="mailto:tcu.brass.stack@gmail.com" target="_blank" rel="noopener">tcu.brass.stack@gmail.com</a>まで！
    </div>
```
---
2枚の写真をパソコンでは横並びに表示、スマホでは縦に表示したいとき
``` html
<div class="image-row">
    <div class="image-item">
        <img src="img/ファイル名">(1枚目の写真のファイル名)
    </div>
    <div class="image-item">
        <img src="img/ファイル名">(2枚目の写真のファイル名)
    </div>
</div>
```
例下記コードの時写真のようになります。
``` html
      <div class="image-row">
        <div class="image-item">
          <img src="img/2025定演表.JPG" alt="2025定演チラシ表">
        </div>
        <div class="image-item">
          <img src="img/2025定演裏.JPG" alt="2025定演チラシ裏">
        </div>
      </div>
```

### about.html
とくになし

### report.html
写真あり
``` html
    <div class="event">
      <div class="evenvt_poter">
        <img src="img/report/2025アンコン.jpg" width="200px">
      </div>
      <div class="event_description">
        <h2>タイトル</h2>
            <p>日時:20XX年X月X日(X)</br>
                XX：XX 開演</p>
            <p> 会場:</p> 
            説明、 演奏した曲目など
      </div>
    </div>
```
---
写真なし
``` html
    <div class="event">
      <div class="evenvt_poter">
        <img src="img/report/2025アンコン.jpg" width="200px">
      </div>
      <div class="event_description">
        <h2>タイトル</h2>
            <p>日時:20XX年X月X日(X)</br>
                XX：XX 開演</p>
            <p> 会場:</p> 
            説明、 演奏した曲目など
      </div>
    </div>
```

### schedule.html
イベントカード
``` html
        <div class="schedule_card overlay" >
          <input type="checkbox" id="scheduleCheck">
            <label for="scheduleCheck" class="schedule_content">
            <p class="schedule_title">タイトル</p>
            <p class="schedule_description">
              X月開催</br>
              説明</br>
            </p>
            </label>
            <a class="item" href="img/schedule/ファイル名"><!--ここで写真拡大可能に-->
              <img src="img/schedule/ファイル名" alt=""><!--ここで写真設定-->
            </a>
        </div>
```
注意点：イベントカード追加の時はimg/scheduleにファイル追加すること

### link.html
掲載団体が増えた場合
``` html
              <li><a class="link_color" href="リンク" target="_blank" rel="noopener">団体名</a></li>
```