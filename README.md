# Release management in python

## Develop --> Staging --> Master

* 0.0.1: doing this
* 0.0.2: doing this
* 0.1.0: doing this
* 0.1.1: doing this
* 1.0.0: doing this

```
git init
git add .
git commit -m "first commit"
git branch -M develop
git remote add origin https://github.com/pandalearnstocode/pythom-release-template.git
git push -u origin develop
```

```
git checkout -b staging
git add .
git commit -m "first commit"
git push origin staging
git checkout -b master
git add .
git commit -m "first commit"
git push origin master
```


```
git checkout develop
git tag 0.0.0
git push origin refs/tags/0.0.0
```



```
git checkout -b f1
touch version_001.md
git add .
git commit -m "fix: 0.0.1"
git push origin f1
```

```
git checkout -b f2
touch version_002.md
git add .
git commit -m "feat: 0.1.0"
git push origin f2
```

```
git checkout develop
git checkout -b f3
touch version_003.md
git add .
git commit -m "feat: 1.0.0"
git push origin f3
```

```
git checkout develop
git checkout -b f4
touch version_004.md
git add .
git commit -m "BREAKING CHANGE: 1.0.0"
git push origin f4
```