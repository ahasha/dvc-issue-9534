# dvc-issue-9534
Minimal example to reproduce the bug in iterative/dvc#9534

Steps to reproduce:

1. git clone git@github.com:ahasha/dvc-issue-9534.git
2. dvc repro
3. git checkout file_out
4. dvc repro
5. git checkout dir_out
6. dvc checkout

You should see:
```
ERROR: unexpected error - [Errno 17] File exists: '/Users/alexhasha/repos/dvc-issue-9534/data/foo.txt'     
```
