webui-aria2
===========

こちらは、https://github.com/playbuger/Aria2WebUI.git をフォークし、RasPi3~4へ適用させたものになります。x86_64で利用される方は、フォーク元を利用しましょう。

This is a forked version of https://github.com/playbuger/Aria2WebUI.git and applied to RasPi3~4. If you use x86_64, please use the forked version.

Build
===========

```
docker build -f rpi-Dockerfile -t local/webui-aria2 .
```

RUN
===========

```
docker run --restart=always -d -v /home/$USER/data/aria2:/data -p 6800:6800 -p 8080:8080 --name="webui-aria2" local/webui-aria2:latest
```

ダウンロード先:/home/$USER/data/aria2
※書き込めないなどのエラーが出る場合は、パーミッションの変更をしましょう

USEAGE
===========

ブラウザにて、http://ホストIP:8080/にてUIが展開されます

License
===========

LICENSEファイル(MITライセンス)を参照してください。

Refer to the LICENSE file (MIT License). 
