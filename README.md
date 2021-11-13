## submodule direction

### submodule の導入

```
git submodule add https://github.com/tetsukamen/submodule_test_A.git repoA
git commit -m "Add module"
cd repoA
git config core.sparsecheckout true
cat ../.gitsparse > ../.git/modules/repoA/info/sparse-checkout
git read-tree -mu HEAD
```

### クローン後にやること

```
cd repoA
git config core.sparsecheckout true
cat ../.gitsparse > ../git/modules/repoA/info/sparse-checkout
git read-tree -mu HEAD
```

### submodule の update

```
cd repoA
git pull
```

### 親リポジトリが submodule を update した場合

```
cd repoA
git submodule update
```
