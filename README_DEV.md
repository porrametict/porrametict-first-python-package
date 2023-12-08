# HOW to push to Pypi

1. generate token
   https://pypi.org/manage/account/token/

2. install twine

```
pip install twine

```

3. Update ~/.pypirc Configuration File:

for linux/mac

```
[pypi]
username = __token__
password = <your-api-token>
```

for window (powershell)

```
$ENV:TWINE_USERNAME="__token__"
$ENV:TWINE_PASSWORD="<your-api-token>"
```

4. build package
   \*\* ensure update version in setup.py first

```
python setup.py sdist bdist_wheel
twine upload dist/*
```
