[![masizime](http://masizime.com/common/images/logo.png)](http://masizime.com)
masizime Mixins
===
masizime Sass Mixinsです。

[Burbon](http://bourbon.io/), [Pure](http://purecss.io/), [Bootstrap](http://getbootstrap.com/)を参考にしています。


Requirements
====
- [Sass](https://github.com/sass/sass) 3.4+


Bower Installation
====

```bash
bower install masizime.sass.mixins --save-dev
```

Sass Import
====

```scss
@import "masizime.mixins/masizime";
```

Document
====
<div class="unit">
  <h4 class="heading-b">grid</h4>
  <div class="clearfix">
    <h5><strong>グリッドレイアウト</strong></h5>
    <p>グリッドの幅を指定</p>
    <ul>
      <li><code>$grid</code>:総グリッド数</li>
      <li><code>$columnsWidth</code>:最大幅</li>
      <li><code>$gutter</code>:ガター幅</li>
      <li><code>$direction</code>:ガターのマージンの向き [left or auto]</li>
      <li><code>$thisGrid</code>:求めたいグリッド数</li>
    </ul>

    <pre><code>@include col-width($grid:12,$columnsWidth:980,$gutter:10,$direction:left,$thisGrid:1);</code></pre>
    <p>グリッドのマージンを指定</p>
    <ul>
      <li><code>$grid</code>:総グリッド数</li>
      <li><code>$columnsWidth</code>:最大幅</li>
      <li><code>$gutter</code>:ガター幅</li>
      <li><code>$direction</code>:ガターのマージンの向き [left or auto]</li>
      <li><code>$align</code>:text-align [値 or false]</li>
      <li><code>$mb</code>:margin-bottom [値 or false]</li>
    </ul>
    <pre><code>@include col-margin($grid:12,$columnsWidth:980,$gutter:10,$direction:left, $align:false, $mb:false);</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/grid/_col.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>外枠</strong></h5>
    <p>グリッドの外枠を指定</p>
    <pre><code>@include row();</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/grid/_row.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>折り返し</strong></h5>
    <p>カラムの折り返し時のマージンを0にする</p>
    <pre><code>@include by-return($col: 3, $direction: left);</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/grid/_by-return.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>幅、隙間</strong></h5>
    <p>最大幅を指定</p>
    <pre><code>@include l-wrapper($screen-width:960, $screen-fsize:13,$target:ie10);</code></pre>
    <p>左右の隙間を指定</p>
    <pre><code>@include l-gap($gap:10px);</code></pre>
    <p>1カラムに落とす</p>
    <pre><code>@include l-one($direction:left)</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/grid/_layout.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>個別に作るグリッド</strong></h5>
    <p>グリッドの外枠を指定</p>
    <pre><code>@include grid-row();</code></pre>
    <p>グリッドのカラムベースを指定</p>
    <pre><code>@include grid-col-base();</code></pre>
    <p>グリッドのカラムを指定</p>
    <ul>
      <li><code>$col</code>:段組数</li>
      <li><code>$w</code>:最大幅</li>
      <li><code>$g</code>:ガター幅</li>
      <li><code>$align</code>:text-align [値 or false]</li>
      <li><code>$mb</code>:margin-bottom [値 or false]</li>
      <li><code>$direction</code>:ガターのマージンの向き [left or right or auto]//autoは左右</li>
      <li><code>$target</code>:ie8をサポートするか？ [ie8 or ie10]</li>
      <li><code>$from</code>ie8ターゲットの場合に連番クラスを指定する最小値</li>
      <li><code>$to</code>:ie8ターゲットの場合に連番クラスを指定する最大値</li>
    </ul>
    <pre><code>@include grid-col($col: 6, $w: 940, $g: 20, $align:false, $mb:false, $direction:left,$target:ie10,$from:1,$to:20);</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/grid/_grid-col.scss">ソースを見る</a></p>
  </div>
  <hr>
  <h4 class="heading-b">rwd</h4>
  <div class="clearfix">
    <h5><strong>フォントサイズ</strong></h5>
    <p>Smallサイズ, Middleサイズ, Largeサイズをまとめて指定</p>
    <pre><code>@include fsize($size: 14px, $size-md: false, $size-sm: false);</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/rwd/_fontsize.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>高さ</strong></h5>
    <p>Smallサイズ, Middleサイズ, Largeサイズをまとめて指定</p>
    <pre><code>@include h($size: 20px, $size-md: false, $size-sm: false);</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/rwd/_height.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>幅</strong></h5>
    <p>Smallサイズ, Middleサイズ, Largeサイズをまとめて指定</p>
    <pre><code>@include w($size: 20px, $size-md: false, $size-sm: false);</code></pre>
    <pre><code>@include w-percentage($size: 20, $parentW:0, $size-md: false, $parentW-md:0 , $size-sm: false, $parentW-sm:0 );</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/rwd/_width.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>ラインハイト</strong></h5>
    <p>Smallサイズ, Middleサイズ, Largeサイズをまとめて指定</p>
    <pre><code>@include lh($size: 1, $size-md: false, $size-sm: false);</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/rwd/_line-height.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>ポジション</strong></h5>
    <p>Smallサイズ, Middleサイズ, Largeサイズをまとめて指定</p>
    <pre><code>@include t($size: 0, $size-md: false, $size-sm: false);</code></pre>
    <pre><code>@include r($size: 0, $size-md: false, $size-sm: false);</code></pre>
    <pre><code>@include b($size: 0, $size-md: false, $size-sm: false);</code></pre>
    <pre><code>@include l($size: 0, $size-md: false, $size-sm: false);</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/rwd/_position.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>マージン</strong></h5>
    <p>Smallサイズ, Middleサイズ, Largeサイズをまとめて指定</p>
    <pre><code>@include m($t:10px,$r:true,$b:true,$l:true); //一括指定</code></pre>
    <pre><code>@include mt($size: 20px, $size-md: false, $size-sm: false);</code></pre>
    <pre><code>@include mr($size: 20px, $size-md: false, $size-sm: false);</code></pre>
    <pre><code>@include mb($size: 20px, $size-md: false, $size-sm: false);</code></pre>
    <pre><code>@include ml($size: 20px, $size-md: false, $size-sm: false);</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/rwd/_margin.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>パディング</strong></h5>
    <p>Smallサイズ, Middleサイズ, Largeサイズをまとめて指定</p>
    <pre><code>@include p($t:10px,$r:true,$b:true,$l:true); //一括指定</code></pre>
    <pre><code>@include pt($size: 20px, $size-md: false, $size-sm: false);</code></pre>
    <pre><code>@include pr($size: 20px, $size-md: false, $size-sm: false);</code></pre>
    <pre><code>@include pb($size: 20px, $size-md: false, $size-sm: false);</code></pre>
    <pre><code>@include pl($size: 20px, $size-md: false, $size-sm: false);</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/rwd/_padding.scss">ソースを見る</a></p>
  </div>
  <hr>
  <h4 class="heading-b">text</h4>
  <div class="clearfix">
    <h5><strong>マウスエフェクト</strong></h5>
    <p>マウス操作時にエフェクトを追加  </p>
    <ul>
      <li><code>$r</code>:カラーRed</li>
      <li><code>$g</code>:カラーGreen</li>
      <li><code>$b</code>:カラーBlue</li>
      <li><code>$num1</code>:グラデーション下の透明度</li>
      <li><code>$num2</code>:グラデーション上の透明度</li>
    </ul>

    <pre><code>@include mouse-effect-hover($r:0,$g:0,$b:0,$num1:0.1,$num2:0.2);</code></pre>
    <pre><code>@include mouse-effect-on($r:0,$g:0,$b:0,$num1:0.1,$num2:0.2);</code></pre>
    <pre><code>@include mouse-effect-active();</code></pre>
    <pre><code>@include mouse-effect-disabled();</code></pre>
    <pre><code>@include mouse-effect($r:255,$g:255,$b:255,$num2:0.1,$num3:0.2);</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/text/_mous-effect.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>テキストインデント</strong></h5>
    <pre><code>@include text-indent();</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/text/_text-indent.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>テキストオーバーフロー</strong></h5>
    <pre><code>@include text-overflow();</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/text/_text-overflow.scss">ソースを見る</a></p>
  </div>
  <hr>
  <h4 class="heading-b">addons</h4>
  <div class="clearfix">
    <h5><strong>クリアフィックス</strong></h5>
    <pre><code>@include clearfix();</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/addons/_clearifx.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>メディアクエリ</strong></h5>
    <pre><code>@include min-media( $min-w );</code></pre>
    <pre><code>@include max-media( $max-w );</code></pre>
    <pre><code>@include min-max-media( $min-w, $max-w );</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/addons/_media.scss">ソースを見る</a></p>
  </div>
  <hr>
  <div class="clearfix">
    <h5><strong>メディアクエリ入り - プロパティ</strong></h5>
    <p>Smallサイズ, Middleサイズ, Largeサイズをまとめて指定</p>
    <pre><code>@include media-property( $propertyName:top, $size: 0, $size-md: false, $size-sm: false );</code></pre>
    <p class="pull-right">
      <a href="https://github.com/tamshow/masizime.sass.mixins/blob/master/addons/_media-property.scss">ソースを見る</a></p>
  </div>
</div>