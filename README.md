crystalCloud-test
=================

Some documentation on randomly merging github targets

merging two repositories on disk (that are branches)
====

# get branch 1
git clone -b b1 git@github.com:rtholmes/crystalCloud-test.git b1

# get branch 2
git clone -b b2 git@github.com:rtholmes/crystalCloud-test.git b2

# try to merge the two
cd b2; git remote add -f b1 ../b1/

# see if b1 and b2 can be merged cleanly
git merge b1/b1

# if merge is clean, do build and test stuff here

# reset repo
git reset origin/b2 --hard

merging a fork with a branch
===

git clone git://github.com/brunyuriy/crystalCloud-test.git brun

# see if b1 merges ok
cd brun; git remote add -f b1 ../b1/; git merge b1/b1

