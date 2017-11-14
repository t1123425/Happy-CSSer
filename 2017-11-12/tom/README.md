2017-11-12 happy csser Two Square loading

範例效果:https://dribbble.com/shots/3807497-Two-squares-four-triangles

codepen:https://codepen.io/Tommax/pen/xPdVmb

實作步驟:

1. 先設外框.boxWrap將內部四個三角形包起來，其中裡面四個三角形為了呈現混合圖層的效果
   四個三角形要使用css3的mix-blend-mode屬性，其中用的設定為difference，當div有重疊
   的時候就會出現反色的效果，而裡面的三角形是用 css border所刻出 顏色都為白色

2. 再來是定位設定，依範例先是有一個白色方塊包住黑色方塊，這邊我是將其中兩個三角形
   寬則設.boxWrap寬的一半 讓這兩層在其中的另外兩個黑框設70px，因為mix-blend-mode屬性
   會讓四個寬在重疊時出現反色效果，而做出有一個白色方塊包住黑色方塊(白色的反色為黑)的狀態

3.動態方面我則是控制.boxWrap進行方塊旋轉跟縮放，兩個大的白色方塊在旋轉後因為會對稱
  被包住的兩個小三角形，所以在動態上我有設定borderWidth會跟著縮小。
  (當然也可設scale但比例我懶得算XD)
  動態上在實作遇到比較大的問題是時間要對到個動態的時間也就是各三角形展開後會剛好回到最初狀態

  PS:另外mix-blend-mode目前支援上好像chorme跟firefox呈現比較沒問題(chorme會有重疊線，火狐則無)
     微軟ie跟edge是全數陣亡

   

