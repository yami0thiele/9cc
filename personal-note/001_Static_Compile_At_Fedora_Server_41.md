# Fedora Server 41 での静的コンパイル

下記のコンパイルが通らなかった

```sh
cc -std=c11 -g -static 9cc.c -o 9cc
```

一方で以下は通る。

```sh
cc -std=c11 -g 9cc.c -o 9cc
```

[glibc-static](https://packages.fedoraproject.org/pkgs/glibc/glibc-static/) が入っていなかったためだった。
入れたら通るようになった。
