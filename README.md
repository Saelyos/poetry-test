# With Poetry 1.0.5

```
$ python ~/get-poetry.py
$ poetry install
Installing dependencies from lock file


Package operations: 1 install, 0 updates, 0 removals

  - Installing package-a (0.1.0 package-a)

[EnvCommandError]
Command ['/Users/alisue/Library/Caches/pypoetry/virtualenvs/poetry-test-MDzUKMz
t-py3.7/bin/pip', 'install', '--no-deps', '-U', '-e', '/Users/alisue/.ghq/githu
b.com/lambdalisue/poetry-test/package-a'] errored with the following return cod
e 1, and output:
Obtaining file:///Users/alisue/.ghq/github.com/lambdalisue/poetry-test/package-
a
  Installing build dependencies: started
  Installing build dependencies: finished with status 'done'
  Getting requirements to build wheel: started
  Getting requirements to build wheel: finished with status 'done'
    Preparing wheel metadata: started
    Preparing wheel metadata: finished with status 'done'
Installing collected packages: package-a
  Running setup.py develop for package-a
    ERROR: Command errored out with exit status 1:
     command: /Users/alisue/Library/Caches/pypoetry/virtualenvs/poetry-test-MDz
UKMzt-py3.7/bin/python -c 'import sys, setuptools, tokenize; sys.argv[0] = '"'"
'/Users/alisue/.ghq/github.com/lambdalisue/poetry-test/package-a/setup.py'"'"';
 __file__='"'"'/Users/alisue/.ghq/github.com/lambdalisue/poetry-test/package-a/
setup.py'"'"';f=getattr(tokenize, '"'"'open'"'"', open)(__file__);code=f.read()
.replace('"'"'\r\n'"'"', '"'"'\n'"'"');f.close();exec(compile(code, __file__, '
"'"'exec'"'"'))' develop --no-deps
         cwd: /Users/alisue/.ghq/github.com/lambdalisue/poetry-test/package-a/
    Complete output (3 lines):
    Traceback (most recent call last):
      File "<string>", line 1, in <module>
    ModuleNotFoundError: No module named 'setuptools'
    ----------------------------------------
ERROR: Command errored out with exit status 1: /Users/alisue/Library/Caches/pyp
oetry/virtualenvs/poetry-test-MDzUKMzt-py3.7/bin/python -c 'import sys, setupto
ols, tokenize; sys.argv[0] = '"'"'/Users/alisue/.ghq/github.com/lambdalisue/poe
try-test/package-a/setup.py'"'"'; __file__='"'"'/Users/alisue/.ghq/github.com/l
ambdalisue/poetry-test/package-a/setup.py'"'"';f=getattr(tokenize, '"'"'open'"'
"', open)(__file__);code=f.read().replace('"'"'\r\n'"'"', '"'"'\n'"'"');f.close
();exec(compile(code, __file__, '"'"'exec'"'"'))' develop --no-deps Check the l
ogs for full command output.
WARNING: You are using pip version 19.2.3, however version 20.0.2 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.

```

# With Poetry 1.1.0a1

```
$ POETRY_PREVIEW=1 python ~/get.poetry.py
$ poetry install
Installing dependencies from lock file


Package operations: 1 install, 0 updates, 0 removals

  - Installing package-a (0.1.0 package-a)

  TypeError

  __init__() takes from 2 to 3 positional arguments but 4 were given

  at ~/.poetry/lib/poetry/installation/pip_installer.py:214 in install_director
y
      210|             # file since pip, as of this comment, does not support
      211|             # build-system for editable packages
      212|             # We also need it for non-PEP-517 packages
      213|             builder = SdistBuilder(
    > 214|                 Factory().create_poetry(pyproject.parent), NullEnv()
, NullIO()
      215|             )
      216|
      217|             with open(setup, "w", encoding="utf-8") as f:
      218|                 f.write(decode(builder.build_setup()))
```
