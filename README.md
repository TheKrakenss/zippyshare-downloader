# zippyshare-downloader

Download file from zippyshare directly from python

## Table of Contents

- [Key Features](#key-features)
- [Minimum Python Version](#minimum-python-version)
- [Installation](#installation)
    - [Python Packages Index (PyPI)](#python-packages-index-pypi)
    - [From the source](#from-the-source)
- [Simple Usage](#simple-usage)
    - [Command Line Interface (CLI)](#command-line-interface-cli)
    - [Embedding (API)](#embedding-api)
- [Links](#links)
- [FAQ](#faq)

## Key Features

In `zippyshare-downloader` you can:

- download file from Zippyshare (Yes of course).
- Extract filename, date uploaded, file size, and downloadable url information from given url.
- Fast Download, allows you to download in 2 connections at same time simultaneously.

## Minimum Python version

```
3.5.x
```

## Installation

### Python Packages Index (PyPI)

```bash
pip install zippyshare-downloader
```

### From the source

Clone the repository
```
git clone https://github.com/mansuf/zippyshare-downloader.git
cd zippyshare-downloader
```

And then run `setup.py`
```
python setup.py install
```

## Simple Usage

### Command Line Interface (CLI)

Read [here](https://zippyshare-downloader.readthedocs.io/en/latest/cli.html) for more informations

```bash
zippyshare-dl "insert zippyshare url here"

# or

zippyshare-downloader "insert zippyshare url here"

# Use this if `zippyshare-dl` and `zippyshare-downloader` didn't work

python -m zippyshare_downloader "insert zippyshare url here"
```

### Embedding (API)
Use `zippyshare-downloader` in your python script

Read [here](https://zippyshare-downloader.readthedocs.io/en/latest/api.html) for more informations

```python

from zippyshare_downloader import extract_info, extract_info_coro

# by default, parameter download is True
file = extract_info('insert zippyshare url here', download=True)

print(file)

# Output: <Zippyshare File name="..." size="...">

# async version
async def get_info():
    file = await extract_info_coro('insert zippyshare url here', download=True)
    print(file)

```

## Links

- [Documentation](https://zippyshare-downloader.readthedocs.io/en/latest)
- [PyPI](https://pypi.org/project/zippyshare-downloader/)


## FAQ

**Q:** I always getting `NameError: The use of "bla bla" is not allowed`, what should i do ?<br>
**A:** Zippyshare always change their code, Please update to last version, if your zippyshare-downloader is latest version, then open a issue [here](https://github.com/mansuf/zippyshare-downloader/issues)

