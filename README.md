# PTTAutoSign
PTT 自動簽到，最近老人在用的 PTT 終於又重新開放註冊了，我也嘗試當個老人。 \
![kachow 2021-08-21 at 13 36 12@2x](https://user-images.githubusercontent.com/11913223/130311745-97ccf57e-6c67-423e-b4a6-d74908dd9df9.png)

✅ 不需要額外伺服器 \
🚀 即時發送通知到 Telegam \
👷‍♂️ 不需額外維護 

1. 首先右上角 Star 給他按下去，接著 `fork` 一份。哪天如果被我海巡到會被我單方面的 Block。
2. 接著打開 [Layerci](https://layerci.com) 用一個舒服的方式登入或註冊。
3. 點一下 `New Installation`，並點一下 `Install on GitHub` \
![1.png](https://user-images.githubusercontent.com/11913223/127747923-542a75be-89ee-4905-b87d-b4f0d88a30ef.png)
4. 點左邊的 `Secrets` 設定環境參數，不知道 `chat_id` 嗎？請參考下方 FAQ。
```
bot_token  -> telegram bot token
chat_id    -> telegram chat id
ptt_id_1   -> ptt 帳號 (username,passwd)

** 如果沒有第二個帳號要登入請一樣新增 ptt_id_2 但在輸入帳號與密碼的地方輸入 none **
ptt_id_2   -> ptt 帳號 (username,passwd)
```
5. 在左側 `Settings` 中找到 `Organization` 將 `Live API Key` 複製起來 \
  ![2.png](https://user-images.githubusercontent.com/11913223/127748093-56b0f233-ec35-4279-a847-6586e022f86a.png)
6. 新增至 GitHub Secret 中取名為 `LAYERCI`
  ![3.png](https://user-images.githubusercontent.com/11913223/127748085-187f2d4c-bc55-4d00-904b-79c15943f3e5.png)
7. 最後點自己 `Repo` 的 `Action`，找到左側 `Daily Trigger` 打開 workflow。 \
  ![image](https://user-images.githubusercontent.com/11913223/127421102-ada99cea-f20b-43ca-8899-8ba65b4b733b.png)
8. 自動同步更新原始碼，請點[這裡](https://github.com/apps/pull)，並點一下綠色的 Install，如果安裝過請點 `Configure`。 
   ![image](https://user-images.githubusercontent.com/11913223/127421412-7b146eab-4b12-4aea-b95a-656a49c73df2.png)
9. Enjoy 🎉


## FAQ
Q: 我怎麼找到我的 `bot_token` \
A: 先去找 @Botfather 申請一個，之後會拿到一個 `token` 像是 `1234567:abcdefghijklmnopqrstuwxyz` 

Q: 我要怎麼知道 `chat_id`？頻道或群組支援嗎？ \
A: 拆開講。 \
如果你要拿自己的 `chat_id` 直接私訊 @my_id_bot \
如果你要拿頻道的 `chat_id` 開好一個頻道，在頻道裡面隨便打一段字，接著將那串文字轉傳給 @my_id_bot \
如果你要拿群組的 `chat_id` 直接把 @my_id_bot 加進群組
20250724:test
