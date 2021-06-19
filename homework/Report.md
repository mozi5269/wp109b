# 猜數字 
## 來源 
參考:https://developer.mozilla.org/zh-TW/docs/Learn/JavaScript/First_steps/A_first_splash#%E6%A2%9D%E4%BB%B6  

本程式修改自 mozilla 的官方範例，網址如下：

-- https://github.com/mdn/learning-area/blob/master/javascript/introduction-to-js-1/first-splash/number-guessing-game.html

## 功能
1. 輸入數字
2. 跑馬燈
3. 提示

## 技術手段
### 輸入數字

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

## 修改目標
1. 按鈕
2. 修復bug
3. 重新開始
4. 美化
