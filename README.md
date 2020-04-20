# sample
sample

ブランチテストをします


■事前準備 (1回だけdevelop brachを作成する)

1) master brachからdevelop brachを作成
```
$ git checkout master
Switched to branch 'master'

$ git checkout -b develop
Switched to a new branch 'develop'

$ git push origin develop
Total 0 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/SusumuKanazawa/sample/pull/new/develop
remote: 
To https://github.com/SusumuKanazawa/sample.git
 * [new branch]      develop -> develop
```
2) default branchの変更
github上で、code => branchesから、default branchをmasterからdevelopに変更する。

■開発
1) develop brachからcheckoutをする
```
$ git fetch && git checkout origin/develop
Note: switching to 'origin/develop'.

$ git checkout -b hogehoge
```

2) pull request先はdevelop branch
```
$ git push origin develop hogehoge
```

3) OKの場合はgithub上でmerge
develop branchにmergeされます

■リリース
1) developからmaster
github上でnew pull requestを作成し、master ← developとなるようにする

2) merge
プルリクしてmerge
