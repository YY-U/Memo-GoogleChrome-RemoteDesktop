# memo
## Chrome-RemoteDesktop
## 構築環境
windows10(接続元) → ubunut18.04(接続先)

## 修正手順
### 1．前処理
#### 1-1．chromeRemoteDesktopサービスを止める

```
sudo systemctl stop chrome-remote-desktop.service
```

#### 1-2．オリジナルファイルのバックアップを作成
```
sudo cp /opt/google/chrome-remote-desktop/chrome-remote-desktop /opt/google/chrome-remote-desktop/chrome-remote-desktop.orig
```

#### 1-3．ファイルを開く
```
sudo gedit /opt/google/chrome-remote-desktop/chrome-remote-desktop
```

### 2．ファイル編集
```
echo $DISPLAY
```
↑と同じ数字を↓に書き換える

```
FIRST_X_DISPLAY_NUMBER = "数字"
```
