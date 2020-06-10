[![Build Status](https://travis-ci.com/callmemiya/lab09.svg?branch=master)](https://travis-ci.com/callmemiya/lab09)
## Laboratory work IX

<a href="https://yandex.ru/efir/?stream_id=vYrKRcFKi46o"><img src="https://raw.githubusercontent.com/tp-labs/lab09/master/preview.png" width="640"/></a>

Данная лабораторная работа посвещена изучению процесса создания артефактов на примере **Github Release**

```sh
$ open https://help.github.com/articles/creating-releases/
```

## Tasks

- [x] 1. Создать публичный репозиторий с названием **lab09** на сервисе **GitHub**
- [x] 2. Ознакомиться со ссылками учебного материала
- [x] 3. Получить токен для доступа к репозиториям сервиса **GitHub**
- [x] 4. Выполнить инструкцию учебного материала
- [x] 5. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```sh
$ export GITHUB_TOKEN=****************************************
$ export GITHUB_USERNAME=callmemiya
$ export PACKAGE_MANAGER=brew
$ export GPG_PACKAGE_NAME=gpg
```

```sh
# for *-nix system
$ $PACKAGE_MANAGER install xclip
$ alias gsed=sed
$ alias pbcopy='xclip -selection clipboard'
$ alias pbpaste='xclip -selection clipboard -o'
```

```sh
$ cd ${GITHUB_USERNAME}/workspace
$ pushd .
$ source scripts/activate
$ go get github.com/aktau/github-release
```

```sh
$ git clone https://github.com/${GITHUB_USERNAME}/lab08 projects/lab09
Клонирование в «projects/lab09/l»…
remote: Enumerating objects: 35, done.
remote: Counting objects: 100% (35/35), done.
remote: Compressing objects: 100% (23/23), done.
remote: Total 35 (delta 4), reused 32 (delta 3), pack-reused 0
Получение объектов: 100% (35/35), 12.45 KiB | 4.15 MiB/s, готово.
Определение изменений: 100% (4/4), готово.
$ cd projects/lab09
$ git remote remove origin
$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab09
```

```sh
$ gsed -i 's/lab08/lab09/g' README.md
```

```sh
$ $PACKAGE_MANAGER install ${GPG_PACKAGE_NAME}
==> Downloading https://homebrew.bintray.com/bottles/adns-1.5.1.mojave.bottle.ta
==> Downloading from https://akamai.bintray.com/1a/1a067d7acebfc1733c3b035ca51c7
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/libtasn1-4.16.0.mojave.bott
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/nettle-3.6.mojave.bottle.ta
==> Downloading from https://akamai.bintray.com/d3/d378b026725d8d449ca6497ce2158
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/libffi-3.3.mojave.bottle.ta
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/p11-kit-0.23.20_1.mojave.bo
==> Downloading from https://akamai.bintray.com/72/72d092bf908d2623a9be13c716fd8
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/libevent-2.1.11_1.mojave.bo
==> Downloading from https://akamai.bintray.com/1e/1e14fc34baae0b65cac6d7c75bc5e
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/unbound-1.10.1.mojave.bottl
==> Downloading from https://akamai.bintray.com/04/04dfb0c9becb94b0e76ad11ba6b0b
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/gnutls-3.6.14.mojave.bottle
==> Downloading from https://akamai.bintray.com/d5/d57c7537ca0565e8c8fdf13beb4b0
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/libgpg-error-1.38.mojave.bo
==> Downloading from https://akamai.bintray.com/60/60867a965e4ea8dc1e119adfecaa2
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/libassuan-2.5.3.mojave.bott
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/libgcrypt-1.8.5.mojave.bott
==> Downloading from https://akamai.bintray.com/d9/d983dca1f56d0177d4ecd6ea27524
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/libksba-1.4.0.mojave.bottle
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/libusb-1.0.23.mojave.bottle
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/npth-1.6.mojave.bottle.tar.
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/pinentry-1.1.0_1.mojave.bot
######################################################################## 100.0%
==> Downloading https://homebrew.bintray.com/bottles/gnupg-2.2.20.mojave.bottle.
==> Downloading from https://akamai.bintray.com/e8/e826cf4b1764da749eba007097be8
######################################################################## 100.0%
==> Installing dependencies for gnupg: adns, libtasn1, nettle, libffi, p11-kit, libevent, unbound, gnutls, libgpg-error, libassuan, libgcrypt, libksba, libusb, npth and pinentry
==> Installing gnupg dependency: adns
==> Pouring adns-1.5.1.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/adns/1.5.1: 14 files, 597.5KB
==> Installing gnupg dependency: libtasn1
==> Pouring libtasn1-4.16.0.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/libtasn1/4.16.0: 60 files, 388.3KB
==> Installing gnupg dependency: nettle
==> Pouring nettle-3.6.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/nettle/3.6: 87 files, 2.3MB
==> Installing gnupg dependency: libffi
==> Pouring libffi-3.3.mojave.bottle.tar.gz
==> Caveats
libffi is keg-only, which means it was not symlinked into /usr/local,
because macOS already provides this software and installing another version in
parallel can cause all kinds of trouble.

For compilers to find libffi you may need to set:
  export LDFLAGS="-L/usr/local/opt/libffi/lib"
  export CPPFLAGS="-I/usr/local/opt/libffi/include"

For pkg-config to find libffi you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/libffi/lib/pkgconfig"

==> Summary
🍺  /usr/local/Cellar/libffi/3.3: 16 files, 484.8KB
==> Installing gnupg dependency: p11-kit
==> Pouring p11-kit-0.23.20_1.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/p11-kit/0.23.20_1: 63 files, 2.9MB
==> Installing gnupg dependency: libevent
==> Pouring libevent-2.1.11_1.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/libevent/2.1.11_1: 1,063 files, 5MB
==> Installing gnupg dependency: unbound
==> Pouring unbound-1.10.1.mojave.bottle.tar.gz
==> Caveats
To have launchd start unbound now and restart at startup:
  sudo brew services start unbound
==> Summary
🍺  /usr/local/Cellar/unbound/1.10.1: 57 files, 5MB
==> Installing gnupg dependency: gnutls
==> Pouring gnutls-3.6.14.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/gnutls/3.6.14: 1,244 files, 10.2MB
==> Installing gnupg dependency: libgpg-error
==> Pouring libgpg-error-1.38.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/libgpg-error/1.38: 26 files, 908.8KB
==> Installing gnupg dependency: libassuan
==> Pouring libassuan-2.5.3.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/libassuan/2.5.3: 16 files, 444.2KB
==> Installing gnupg dependency: libgcrypt
==> Pouring libgcrypt-1.8.5.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/libgcrypt/1.8.5: 22 files, 2.6MB
==> Installing gnupg dependency: libksba
==> Pouring libksba-1.4.0.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/libksba/1.4.0: 15 files, 387.6KB
==> Installing gnupg dependency: libusb
==> Pouring libusb-1.0.23.mojave.bottle.1.tar.gz
🍺  /usr/local/Cellar/libusb/1.0.23: 26 files, 467.2KB
==> Installing gnupg dependency: npth
==> Pouring npth-1.6.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/npth/1.6: 11 files, 71.7KB
==> Installing gnupg dependency: pinentry
==> Pouring pinentry-1.1.0_1.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/pinentry/1.1.0_1: 12 files, 263.9KB
==> Installing gnupg
==> Pouring gnupg-2.2.20.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/gnupg/2.2.20: 134 files, 11MB
==> Caveats
==> libffi
libffi is keg-only, which means it was not symlinked into /usr/local,
because macOS already provides this software and installing another version in
parallel can cause all kinds of trouble.

For compilers to find libffi you may need to set:
  export LDFLAGS="-L/usr/local/opt/libffi/lib"
  export CPPFLAGS="-I/usr/local/opt/libffi/include"

For pkg-config to find libffi you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/libffi/lib/pkgconfig"

==> unbound
To have launchd start unbound now and restart at startup:
  sudo brew services start unbound
$ gpg --list-secret-keys --keyid-format LONG
gpg: создан каталог '/Users/mariazabrodina/.gnupg'
gpg: создан щит с ключами '/Users/mariazabrodina/.gnupg/pubring.kbx'
gpg: /Users/mariazabrodina/.gnupg/trustdb.gpg: создана таблица доверия
$ gpg --full-generate-key
gpg (GnuPG) 2.2.20; Copyright (C) 2020 Free Software Foundation, Inc.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Выберите тип ключа:
   (1) RSA и RSA (по умолчанию)
   (2) DSA и Elgamal
   (3) DSA (только для подписи)
   (4) RSA (только для подписи)
  (14) Existing key from card
Ваш выбор? 1
длина ключей RSA может быть от 1024 до 4096.
Какой размер ключа Вам необходим? (2048) 2048
Запрошенный размер ключа - 2048 бит                                      
Выберите срок действия ключа.
         0 = не ограничен
      <n>  = срок действия ключа - n дней
      <n>w = срок действия ключа - n недель
      <n>m = срок действия ключа - n месяцев
      <n>y = срок действия ключа - n лет
Срок действия ключа? (0) 0
Срок действия ключа не ограничен           
Все верно? (y/N) y
                          
GnuPG должен составить идентификатор пользователя для идентификации ключа.

Ваше полное имя: callmemiya
Адрес электронной почты:                
Примечание:                                   
Вы выбрали следующий идентификатор пользователя:
    "callmemiya"

Сменить (N)Имя, (C)Примечание, (E)Адрес; (O)Принять/(Q)Выход? O
$ gpg --list-secret-keys --keyid-format LONG
pub   rsa2048 2020-06-08 [SC]
      2B237A17679DB6CE82FDB923952130D5788F3B92
uid                      callmemiya
sub   rsa2048 2020-06-08 [E]
$ gpg -K ${GITHUB_USERNAME}
gpg: проверка таблицы доверия
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: глубина: 0  достоверных:   2  подписанных:   0  доверие: 0-, 0q, 0n, 0m, 0f, 2u
sec   rsa2048 2020-06-08 [SC]
      2B237A17679DB6CE82FDB923952130D5788F3B92
uid         [  абсолютно ] callmemiya
ssb   rsa2048 2020-06-08 [E]
$ GPG_KEY_ID=$(gpg --list-secret-keys --keyid-format LONG | grep ssb | tail -1 | awk '{print $2}' | awk -F'/' '{print $2}')
$ GPG_SEC_KEY_ID=$(gpg --list-secret-keys --keyid-format LONG | grep sec | tail -1 | awk '{print $2}' | awk -F'/' '{print $2}')
$ gpg --armor --export ${GPG_KEY_ID} | pbcopy
$ pbpaste
$ open https://github.com/settings/keys
$ git config user.signingkey ${GPG_SEC_KEY_ID}
$ git config gpg.program gpg
```

```sh
$ test -r ~/.bash_profile && echo 'export GPG_TTY=$(tty)' >> ~/.bash_profile
$ echo 'export GPG_TTY=$(tty)' >> ~/.profile
```

```sh
$ cmake -H. -B_build -DCPACK_GENERATOR="TGZ"
-- The C compiler identification is AppleClang 11.0.0.11000033
-- The CXX compiler identification is AppleClang 11.0.0.11000033
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc
-- Check for working C compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/cc - works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++
-- Check for working CXX compiler: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/c++ - works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- [hunter] Calculating Toolchain-SHA1
-- [hunter] Calculating Config-SHA1
-- [hunter] HUNTER_ROOT: /Users/mariazabrodina/.hunter
-- [hunter] [ Hunter-ID: 5659b15 | Toolchain-ID: a47179b | Config-ID: 65a58ee ]
-- [hunter] GTEST_ROOT: /Users/mariazabrodina/.hunter/_Base/5659b15/a47179b/65a58ee/Install (ver.: 1.10.0)
-- Looking for pthread.h
-- Looking for pthread.h - found
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE  
-- Configuring done
-- Generating done
-- Build files have been written to: /Users/mariazabrodina/callmemiya/workspace/projects/lab09/_build
$ cmake --build _build --target package
Scanning dependencies of target print
[ 25%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[ 50%] Linking CXX static library libprint.a
[ 50%] Built target print
Scanning dependencies of target demo
[ 75%] Building CXX object CMakeFiles/demo.dir/demo/main.cpp.o
[100%] Linking CXX executable demo
[100%] Built target demo
Run CPack packaging tool...
CPack: Create package using TGZ
CPack: Install projects
CPack: - Run preinstall target for: print
CPack: - Install project: print []
CPack: Create package
CPack: - package: /Users/mariazabrodina/callmemiya/workspace/projects/lab09/_build/print-0.1.0.0-Darwin.tar.gz generated.
```

```sh
$ travis login --auto
Successfully logged in as callmemiya!
$ travis enable
Detected repository as callmemiya/lab09, is this correct? |yes| yes
callmemiya/lab09: enabled :)
```

```sh
$ git tag -s v0.1.0.0
$ git tag -v v0.1.0.0
object 946ada083e37234455536370a8d18e2d5239fb82
type commit
tag v0.1.0.0
tagger callmemiya <mari.zabrodina.01@mail.ru> 1591636110 +0300

release
$ git show v0.1.0.0
tag v0.1.0.0
Tagger: callmemiya <mari.zabrodina.01@mail.ru>
Date:   Mon Jun 8 20:08:30 2020 +0300

release

commit 946ada083e37234455536370a8d18e2d5239fb82 (HEAD -> master, tag: v0.1.0.0, origin/master)
Author: callmemiya <mari.zabrodina.01@mail.ru>
Date:   Mon Jun 8 20:01:52 2020 +0300

    added

diff --git a/.gitmodules b/.gitmodules
new file mode 100644
index 0000000..53f40d0
--- /dev/null
+++ b/.gitmodules
@@ -0,0 +1,3 @@
+[submodule "tools/polly"]
+       path = tools/polly
+       url = https://github.com/ruslo/polly.git
diff --git a/.travis.yml b/.travis.yml
$ git push origin master --tags
Перечисление объектов: 1, готово.
Подсчет объектов: 100% (1/1), готово.
Запись объектов: 100% (1/1), 163 bytes | 163.00 KiB/s, готово.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/callmemiya/lab09
 * [new tag]         v0.1.0.0 -> v0.1.0.0
```

```sh
$ github-release --version
github-release v0.8.1
$ github-release info -u ${GITHUB_USERNAME} -r lab09
$ github-release release \
    --user ${GITHUB_USERNAME} \
    --repo lab09 \
    --tag v0.1.0.0 \
    --name "libprint" \
    --description "my first release"
```

```sh
$ export PACKAGE_OS=`uname -s` PACKAGE_ARCH=`uname -m` 
$ export PACKAGE_FILENAME=print-${PACKAGE_OS}-${PACKAGE_ARCH}.tar.gz
$ github-release upload \
    --user ${GITHUB_USERNAME} \
    --repo lab09 \
    --tag v0.1.0.0 \
    --name "${PACKAGE_FILENAME}" \
    --file _build/*.tar.gz
```

```sh
$ github-release info -u ${GITHUB_USERNAME} -r lab09
$ wget https://github.com/${GITHUB_USERNAME}/lab09/releases/download/v0.1.0.0/${PACKAGE_FILENAME}
$ tar -ztf ${PACKAGE_FILENAME}
print-0.1.0.0-Darwin/cmake/
print-0.1.0.0-Darwin/cmake/print-config-noconfig.cmake
print-0.1.0.0-Darwin/cmake/print-config.cmake
print-0.1.0.0-Darwin/bin/
print-0.1.0.0-Darwin/bin/demo
print-0.1.0.0-Darwin/include/
print-0.1.0.0-Darwin/include/print.hpp
print-0.1.0.0-Darwin/lib/
print-0.1.0.0-Darwin/lib/libprint.a
```

## Report

```sh
$ popd
$ export LAB_NUMBER=09
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gistup -m "lab${LAB_NUMBER}"
```

## Links

- [Create Release](https://help.github.com/articles/creating-releases/)
- [Get GitHub Token](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/)
- [Signing Commits](https://help.github.com/articles/signing-commits-with-gpg/)
- [Go Setup](http://www.golangbootcamp.com/book/get_setup)
- [github-release](https://github.com/aktau/github-release)

```
Copyright (c) 2015-2020 The ISC Authors
```
