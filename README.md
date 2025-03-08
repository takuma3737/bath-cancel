bashで以下のコマンドを叩き，dockerのビルドコマンドのエイリアスを登録する．

```
touch ~/.zshrc
echo "alias dcup='docker-compose up --build'" >> ~/.zshrc
source ~/.zshrc
```

これ以降，"dcup"でビルドする．

