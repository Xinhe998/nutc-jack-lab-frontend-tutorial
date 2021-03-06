# Git首次設定與初始化

## Git首次設定

請在安裝完Git後打開Cmd。

```bash
$ git --version
```

![](../.gitbook/assets/1.png)

若有成功顯示安裝Git的版本資訊，則代表已成功安裝。

一開始要告訴Git使用者資訊

```bash
$ git config --global user.name "Xinhe"
$ git config --global user.email "xinhe998@gmail.com"
```

p.s. **--global**代表全域設定

當送出新版本\(push\)時，就是依照上述兩個設定紀錄於Git的日誌檔中

接著可用以下指令查看剛剛設定是否成功。

```bash
$ git config --list
```

## Git專案初始化

完成上述步驟後，現在我們就可以為一個專案加入Git版本控制～

這裡我們先以新建一個test專案做示範

```bash
建立test資料夾
$ mkdir test

路徑移動至test資料夾下
$ cd test

Git初始化
$ git init
```

![](../.gitbook/assets/3.png)

成功後資料夾內就會多出.git這個隱藏資料夾，這個資料夾若遭刪除，即會取消此專案的Git版本控制。

