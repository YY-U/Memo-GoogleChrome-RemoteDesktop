# memo
## Chrome-RemoteDesktop
## 構築環境
windows10(接続元) → ubunut18.04(接続先)

## 手順
### 1．chromeRemoteDesktopの修正
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

`echo $DISPLAY`
