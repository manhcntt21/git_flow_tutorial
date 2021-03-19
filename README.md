normal

Bat dau hoc su dung git flow so sanh voi luong binh thuong
======================================================================

Thu nhat

1 dau tien tao branch develop va checkout sang nhanh do :

Cach1: git branch develop, sau do checkout sang nhanh do, git checkout develop

Cach2: git checkout -b develop
2 push nhanh develop len remote

Tuong duong voi lenh:

git flow init
======================================================================


Thu hai: feature branch

1 checkout sang branch develop: 
	
	git checkout develop
	
2 De tao tao feature branch tu nhanh develop (luong cua no la nhu vay)
	
	tao nhanh moi va checkout sang nhanh do: git checkout -b feature
tuong duong voi lenh

git flow start feature feature_branch
	chu y, ten nhanh se thanh the nay: feature/feature_branch

======================================================================

Thu 3: merge branch feature vao branch develop

1 neu hien tai dang khong phai o nhanh develop can checkout ve nhanh develop

	git checkout develop

2 mege nhanh feature vao nhanh develop

	git merge feature/feature

3 git branch -d feature/feature
tuong duong voi

git flow feature finish feature_branch
	
======================================================================

Thu 4: release, nhanh dung de dua ra cac ban phat hanh

Cung giong nhu feature branch, release cung duoc tao tu nhanh develop

1 can chuyen sang nhanh develop: git checkout develop

2 tao nhanh release: git checkout -b release/0.1.0

tuong duong voi

git glow release start 0.1.0
======================================================================

Thu 5: close release

1 chuyen sang nhanh master:  git checkout master

2 merge release branch vao nhanh master: git merge release/0.1.0

3 git branch -d release/0.1.0

tuong duong voi lenh sau
git flow release finish '0.1.0'

======================================================================

Thu 6: hotfix

normal:
	git checkout master
	git checkout -b hotfix_branch

git flow:
	git flow hotfix start hotfix_branch


ket thuc hot fix

tuong tu nhu ket thuc 1 release can merge vao ca develop va master(chua hieu sao tren tutorial thi phan release no khong lam ma cho nay no lai noi tuong tu)

normal:
	git checkout master
       	git merge hotfix_branch
	git checkout develop
	git merge hotfix_branch
	git branch -D hotfix_branch

git flow:
	git flow hotfix finish hotfix_branch

thuc te:
	no chi merge vao master con develop thi khong, sau khi chay theo git flow, khong giong nhu no noi
======================================================================

