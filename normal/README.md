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

tuong duong voi

git flow feature finish feature_branch

======================================================================

