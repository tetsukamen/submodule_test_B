## submodule direction

### submodule の導入

submodule を追加したのち、.gitmodules をコミット

```
git submodule add https://github.com/tetsukamen/submodule_test_A.git {ディレクトリ名}
git commit -m "Add module"
```

### クローン後にやること

クローン時点では submodule への参照のみを.gitmodules で保持している状態なので、下記コマンドで submodule のファイルをクローンする

```
git submodule update -i
```

### 親リポジトリが submodule の参照する Commit ID を更新 した場合

submodule のファイルを更新する

```
git submodule update
```

### submodule の 更新を取り込む場合

submodule のディレクトリ内で pull した後、親リポジトリで参照する Commit ID の更新を Commit する

```
cd repoA
git pull
cd ../
git add -m "Update module"
```
