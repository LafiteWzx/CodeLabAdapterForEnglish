# readme.md
[CodeLab Adapter](https://adapter.codelab.club)'s Projects docs，over [mkdocs](https://www.mkdocs.org/)。

Welcome Everyone to mend docs!（new_v2 branch）


# Usage

```
git clone https://github.com/CodeLabClub/codelab-adapter-docs
cd codelab-adapter-docs
pip3 install mkdocs pymdown-extensions mkdocs-material markdown_include

# debug
mkdocs serve

# build
mkdocs build

# publish
make push
```

# How to Edit docs
[mkdocs docs](https://www.mkdocs.org/#getting-started)

# Images and media
[Linking to images and media](https://www.mkdocs.org/user-guide/writing-your-docs/#linking-to-images-and-media)


# push to github
```bash
git checkout gh-pages
ghp-import -r github -p site
```

