# How to contribute

## Prepare a dev environment

```powershell
git clone git@github.com:CASD-EU/build-pyenv.git

cd build-pyenv

uv sync
```
## Build the distribution files

The distribution files often have two formats:
- `.tar.gz`: Source Distribution 
- `.whl`: Built Distribution

If you used `uv` to create the dev environment, you should use `uv build` command to build the `distribution files`

```powershell
uv build

# expected output
... ...
Successfully built dist\build_pyenv-0.2.0.tar.gz
Successfully built dist\build_pyenv-0.2.0-py3-none-any.whl
```

## Upload the distribution files to PyPI

Here we suppose you already have a PyPI account and the right token.

```powershell
uv publish
```

- When prompted for a username, use `__token__`.
- When prompted for a password, paste your token `pypi-...`.

After entering the user credentials, you should see the below outputs

```text
... ...
Uploading build_pyenv-0.2.0-py3-none-any.whl (8.4KiB)
Uploading build_pyenv-0.2.0.tar.gz (9.5KiB)
```

Once the upload finishes, PyPI will give you a URL like https://pypi.org/project/build-pyenv/.
You can check the page to check the distribution files.