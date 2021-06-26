# 猜數字 
## 來源 
參考:https://developer.mozilla.org/zh-TW/docs/Learn/JavaScript/First_steps/A_first_splash#%E6%A2%9D%E4%BB%B6  

### 本程式修改自 mozilla 的官方範例，網址如下：

-- https://github.com/mdn/learning-area/blob/master/javascript/introduction-to-js-1/first-splash/number-guessing-game.html

## 功能
1. 背景圖片
2. 跑馬燈
3. 提示
4. 重新開始
5. 除錯

## 技術手段
### 背景圖片
自己拍攝的照片
```html
<style>
body 
{
      background-image: url('風景1.jpg');
      background-repeat: no-repeat;
      background-size: cover;
}
</style>
```
### 跑馬燈
```html
<marquee behavior="alternate" scrollamount="10" bgcolor=aqua>
    <font size="5">
      <h1>猜數字</h1>
    </font>
</marquee>
```
### 提示
```js
if (userGuess < randomNumber)
{
          min = userGuess;
          lowOrHi.textContent = '太低!';
} 
else if (userGuess > randomNumber) 
{
          max = userGuess;
          lowOrHi.textContent = '太高!';
}
```
### 重新開始
```js
function resetGame() {
      guessCount = 1;
      max = 100;
      min = 0;
      const resetParas = document.querySelectorAll('.resultParas p');
      for (let i = 0; i < resetParas.length; i++) {
        resetParas[i].textContent = '';
      }
```
### 除錯
```js
      if (userGuess > max || userGuess < min)
        lastResult.textContent = '😑請猜範圍內數字!😑';
```
## 修改目標
1. 按鈕功能
2. 修復bug
3. 美化
