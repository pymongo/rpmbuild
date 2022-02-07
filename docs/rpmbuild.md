## pre require

### package

|distribution|package|
|---|---|
|fedora/centos|rpm-build|
|ubuntu|rpm|
|archlinux|rpm-tool|

binary: rpmbuild

optional package rpmdevtools provide scaffold many tool to build rpm

### rpmbuild tips

building rpm not recommend to use root user

what is `~/.rpmmacros` ?

---

### init rpmbuild folders

rpmbuild **must under home directory**

`rpmdev-setuptree` or `mkdir -p rpmbuild/{BUILD,RPMS,SOURCES,SPECS,SRPMS}`

```
[w@ww ~]$ rpmdev-setuptree
[w@ww ~]$ tree rpmbuild/
rpmbuild/
├── BUILD
├── RPMS
├── SOURCES
├── SPECS
└── SRPMS
```



### script

```bash
#!/bin/bash
set -exu

cd ~
rm -rf rpmbuild
rpmdev-setuptree
```

---

## reference
- <https://wiki.centos.org/HowTos/SetupRpmBuildEnvironment>
- <https://www.linuxidc.com/Linux/2016-12/138080.htm>

