# 1. 作成者について
| id | 作成日 | 一言コメント |
| ---- | ---- | ---- |
| [b23a0253](https://github.com/TSWG-b23a0253) | 2026/04/12 |  |

</br></br>

# 2. こちらのディレクトリについて
こちらではC言語ソースを実行する環境を構築します。

</br></br>

# 3. 必要な環境

- [Practice-WSL](https://github.com/Tech-Share-Working-Group/Practice-WSL/tree/main/01_Install_WSL)
- [Practice-Docker](https://github.com/Tech-Share-Working-Group/Practice-Docker/tree/main/01_Install_Docker)
- [Practice-Git](https://github.com/Tech-Share-Working-Group/Practice-Git/tree/main/01_Install_Git)
- [Install-vim](https://github.com/Tech-Share-Working-Group/Practice-Editor/tree/main/04_Use_Vim)

</br></br>

# 4. C言語の実行環境構築

## 4-1. 作業ディレクトリの作成

```bash
# Ubuntu/bash

mkdir workspace_Clang && cd workspace_Clang

mkdir src
```

</br>

## 4-2. 「Dockerfile」ファイルの作成

```bash
# Ubuntu/bash

vim Dockerfile
```

<details>
<summary>「Dockerfile」のファイルの内容</summary>

```Dockerfile
FROM alpine:3.20

# gcc など必要最低限だけ入れる
RUN apk add --no-cache \
    build-base \
    git \
    zlib-dev

# libxlsxwriter をビルド
RUN git clone https://github.com/jmcnamara/libxlsxwriter.git \
    && cd libxlsxwriter \
    && make \
    && make install

WORKDIR /app

COPY . .

COPY run.sh /run.sh
RUN chmod +x /run.sh

ENTRYPOINT ["/run.sh"]
```
</details>

</br>

## 4-3. 「run.sh」ファイルの作成

```bash
# Ubuntu/bash

vim run.sh
```

<details>
<summary>「run.sh」のファイルの内容</summary>

```run.sh
#!/bin/sh
# 引数チェック(1つ目が run で、2つ目が空じゃない場合)
if [ "$1" = "run" ] && [ -n "$2" ]; then
    FILE="src/$2"

    if [ ! -f "$FILE" ]; then
        echo "ファイルが存在しません: $FILE"
        exit 1
    fi

    gcc "$FILE" -o app

    ./app
else
    echo "使い方:"
    echo "docker run cc run main.c"
fi
```
</details>

</br>

## 4-4. 「main.c」ファイルの作成

```bash
# Ubuntu/bash

vim src/main.c
```

<details>
<summary>「main.c」のファイルの内容</summary>

```main.c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n");
    return 0;
}
```
</details>

</br></br>

# 5. アプリを起動

## 5-1. ビルドして実行する。

```bash
# Ubuntu/bash

docker build -t clangenv .
docker run -it --rm -v $(pwd):/app clangenv run main.c
```

<details>
<summary>「docker build -t clangenv .」コマンド実行結果</summary>

```bash
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  4.608kB
Step 1/8 : FROM alpine:3.20
 ---> a4f4213abb84
Step 2/8 : RUN apk add --no-cache     build-base     git     zlib-dev
 ---> Running in 098a1a8f89de
fetch https://dl-cdn.alpinelinux.org/alpine/v3.20/main/x86_64/APKINDEX.tar.gz
fetch https://dl-cdn.alpinelinux.org/alpine/v3.20/community/x86_64/APKINDEX.tar.gz
(1/37) Upgrading musl (1.2.5-r1 -> 1.2.5-r3)
(2/37) Upgrading zlib (1.3.1-r1 -> 1.3.2-r0)
(3/37) Installing libgcc (13.2.1_git20240309-r1)
(4/37) Installing jansson (2.14-r4)
(5/37) Installing libstdc++ (13.2.1_git20240309-r1)
(6/37) Installing zstd-libs (1.5.6-r0)
(7/37) Installing binutils (2.42-r1)
(8/37) Installing libmagic (5.45-r1)
(9/37) Installing file (5.45-r1)
(10/37) Installing libgomp (13.2.1_git20240309-r1)
(11/37) Installing libatomic (13.2.1_git20240309-r1)
(12/37) Installing gmp (6.3.0-r1)
(13/37) Installing isl26 (0.26-r1)
(14/37) Installing mpfr4 (4.2.1-r0)
(15/37) Installing mpc1 (1.3.1-r1)
(16/37) Installing gcc (13.2.1_git20240309-r1)
(17/37) Installing libstdc++-dev (13.2.1_git20240309-r1)
(18/37) Installing musl-dev (1.2.5-r3)
(19/37) Installing g++ (13.2.1_git20240309-r1)
(20/37) Installing make (4.4.1-r2)
(21/37) Installing fortify-headers (1.1-r3)
(22/37) Installing patch (2.7.6-r10)
(23/37) Installing build-base (0.5-r3)
(24/37) Installing ca-certificates (20260413-r0)
(25/37) Installing brotli-libs (1.1.0-r2)
(26/37) Installing c-ares (1.33.1-r0)
(27/37) Installing libunistring (1.2-r0)
(28/37) Installing libidn2 (2.3.7-r0)
(29/37) Installing nghttp2-libs (1.62.1-r0)
(30/37) Installing libpsl (0.21.5-r1)
(31/37) Installing libcurl (8.14.1-r2)
(32/37) Installing libexpat (2.7.5-r0)
(33/37) Installing pcre2 (10.43-r0)
(34/37) Installing git (2.45.4-r0)
(35/37) Installing git-init-template (2.45.4-r0)
(36/37) Installing pkgconf (2.2.0-r0)
(37/37) Installing zlib-dev (1.3.2-r0)
Executing busybox-1.36.1-r31.trigger
Executing ca-certificates-20260413-r0.trigger
OK: 236 MiB in 49 packages
 ---> Removed intermediate container 098a1a8f89de
 ---> da4141c9dfe6
Step 3/8 : RUN git clone https://github.com/jmcnamara/libxlsxwriter.git     && cd libxlsxwriter     && make     && make install
 ---> Running in febc9e78ecc2
Cloning into 'libxlsxwriter'...
make[1]: Entering directory '/libxlsxwriter/third_party/minizip'
make[1]: Leaving directory '/libxlsxwriter/third_party/minizip'
make[1]: Entering directory '/libxlsxwriter/third_party/tmpfileplus'
make[1]: Leaving directory '/libxlsxwriter/third_party/tmpfileplus'
make[1]: Entering directory '/libxlsxwriter/third_party/md5'
make[1]: Leaving directory '/libxlsxwriter/third_party/md5'
make[1]: Entering directory '/libxlsxwriter/src'
make[1]: Leaving directory '/libxlsxwriter/src'
make[1]: Entering directory '/libxlsxwriter/third_party/minizip'
make[1]: Nothing to be done for 'all'.
make[1]: Leaving directory '/libxlsxwriter/third_party/minizip'
make[1]: Entering directory '/libxlsxwriter/third_party/tmpfileplus'
make[1]: Nothing to be done for 'all'.
make[1]: Leaving directory '/libxlsxwriter/third_party/tmpfileplus'
make[1]: Entering directory '/libxlsxwriter/third_party/md5'
make[1]: Nothing to be done for 'all'.
make[1]: Leaving directory '/libxlsxwriter/third_party/md5'
make[1]: Entering directory '/libxlsxwriter/src'
make[1]: Leaving directory '/libxlsxwriter/src'
 ---> Removed intermediate container febc9e78ecc2
 ---> c4497ee19c18
Step 4/8 : WORKDIR /app
 ---> Running in dff2e0288598
 ---> Removed intermediate container dff2e0288598
 ---> 2e17ab89843e
Step 5/8 : COPY . .
 ---> 1ffe78ea70f5
Step 6/8 : COPY run.sh /run.sh
 ---> cad5e26f295e
Step 7/8 : RUN chmod +x /run.sh
 ---> Running in 2b584dbc2d0b
 ---> Removed intermediate container 2b584dbc2d0b
 ---> db2a9283042e
Step 8/8 : ENTRYPOINT ["/run.sh"]
 ---> Running in 6f30e53b1222
 ---> Removed intermediate container 6f30e53b1222
 ---> 8665004bd28a
Successfully built 8665004bd28a
Successfully tagged clangenv:latest
```
</details>

</br>

<details>
<summary>「docker run --rm -v $(pwd):/app clangenv run main.c」コマンド実行結果</summary>

```bash
Hello, World!
```
</details>

</br></br>

# 6. VSCodeでワークスペースを開く

```bash
# Ubuntu/bash

# 現在のディレクトリの位置を確認
pwd

# 上記のディレクトリをVSCodeで開く
code .
```

</br>

<img width="800" alt="image" src="https://github.com/user-attachments/assets/a8d5d5b3-baf1-4eee-ae60-3ae86e128261" />

</br></nr>
