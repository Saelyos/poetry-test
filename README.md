## With poetry 1.1.0b2

```
  Obtaining file:///home/user/poetry-test/package-a
    Installing build dependencies: started  
    Installing build dependencies: finished with status 'done'  
    Getting requirements to build wheel: started
    Getting requirements to build wheel: finished with status 'done'
      Preparing wheel metadata: started
      Preparing wheel metadata: finished with status 'done'
  Installing collected packages: package-a
    Running setup.py develop for package-a
      ERROR: Command errored out with exit status 1:
       command: /home/user/.cache/pypoetry/virtualenvs/poetry-test-dz16zTr5-py3.7/bin/python -c 'import sys, setuptools
, tokenize; sys.argv[0] = '"'"'/home/user/poetry-test/package-a/setup.py'"'"'; __file__
='"'"'/home/user/poetry-test/package-a/setup.py'"'"';f=getattr(tokenize, '"'"'open'"'"', open
)(__file__);code=f.read().replace('"'"'\r\n'"'"', '"'"'\n'"'"');f.close();exec(compile(code, __file__, '"'"'exec'"'"'))' develop --no-deps
           cwd: /home/user/poetry-test/package-a/
      Complete output (3 lines):
      Traceback (most recent call last):
        File "<string>", line 1, in <module>
      ModuleNotFoundError: No module named 'setuptools'
      ----------------------------------------
  ERROR: Command errored out with exit status 1: /home/user/.cache/pypoetry/virtualenvs/poetry-test-dz16zTr5-py3.7/bin
/python -c 'import sys, setuptools, tokenize; sys.argv[0] = '"'"'/home/user/poetry-test/package-a
/setup.py'"'"'; __file__='"'"'/home/user/poetry-test/package-a/setup.py'"'"';f=getattr(tokenize, '"'"'open'"'"', open
)(__file__);code=f.read().replace('"'"'\r\n'"'"', '"'"'\n'"'"');f.close();exec(compile(code, __file__, '"'"'exec'"'"'))' develop --no-deps Check the logs for full command output.
  WARNING: You are using pip version 20.1.1; however, version 20.2 is available.
  You should consider upgrading via the '/home/user/.cache/pypoetry/virtualenvs/poetry-test-dz16zTr5-py3.7/bin/python -m
 pip install --upgrade pip' command.
  

  at ~/.poetry/lib/poetry/utils/env.py:915 in _run
       911│                 output = subprocess.check_output(
       912│                     cmd, stderr=subprocess.STDOUT, **kwargs
       913│                 )
       914│         except CalledProcessError as e:
    →  915│             raise EnvCommandError(e, input=input_)
       916│ 
       917│         return decode(output)
       918│ 
       919│     def execute(self, bin, *args, **kwargs):
```