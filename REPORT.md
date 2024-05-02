```sh
> export GITHUB_USERNAME=ArinaUrnysheva

> export GITHUB_TOKEN=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

> cd ${GITHUB_USERNAME}/workspace

> pushd .
~/ArinaUrnysheva/workspace ~

> source scripts/activate

> git clone git@github.com:ArinaUrnysheva/lab03.git projects/lab04
Клонирование в «projects/lab04»...
remote: Enumerating objects: 36, done.
remote: Counting objects: 100% (36/36), done.
remote: Compressing objects: 100% (22/22), done.
remote: Total 36 (delta 7), reused 36 (delta 7), pack-reused 0
Получение объектов: 100% (36/36), 7.23 КиБ | 1.81 МиБ/с, готово.
Определение изменений: 100% (7/7), готово.

> cd projects/lab04

> git remote remove origin

> git remote add origin git@github.com:ArinaUrnysheva/lab04.git

> cat > .travis.yml <<EOF
language: cpp
EOF

> cat >> .travis.yml <<EOF

script:
- cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
- cmake --build _build
- cmake --build _build --target install
EOF

> cat >> .travis.yml <<EOF

addons:
  apt:
    sources:
      - george-edison55-precise-backports
    packages:
      - cmake
      - cmake-data
EOF


> ex -sc '1i|<фрагмент_вставки_значка>' -cx README.md

> git add README.md

> git commit -m"added CI"
[main 0231068] added CI
 1 file changed, 1 insertion(+)

> git push origin main
Перечисление объектов: 39, готово.
Подсчет объектов: 100% (39/39), готово.
При сжатии изменений используется до 4 потоков
Сжатие объектов: 100% (25/25), готово.
Запись объектов: 100% (39/39), 7.48 КиБ | 7.48 МиБ/с, готово.
Всего 39 (изменений 9), повторно использовано 34 (изменений 7), повторно использовано пакетов 0
remote: Resolving deltas: 100% (9/9), done.
To github.com:ArinaUrnysheva/lab04.git
 * [new branch]      main -> main

> popd
~

> export LAB_NUMBER=04

> git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}

> mkdir reports/lab${LAB_NUMBER}

> cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md

> cd reports/lab${LAB_NUMBER}

> edit REPORT.md

> gist REPORT.md
```
