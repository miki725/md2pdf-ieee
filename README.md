# IEEE templates for md2pdf via pandoc

Works great with [`md2pdf-ieee`] :smile:

[`md2pdf-ieee`]: https://github.com/miki725/.dotfiles/blob/master/.config/fish/functions/md2pdf-ieee.fish

## Requirements

```bash
brew install pandoc pandoc-citeproc pandoc-crossref
brew cask install basictex
```

## Cheatsheet

```markdown
---
title: Very Important Paper
author:
  - name: Name
    affiliation: University
    location: New York
    email: example@domain.com
numbersections: yes
lang: en
abstract: |
    Fancy Abstract
header-includes: |
  \usepackage{booktabs}
bibliography: |
    @article{reference,
      title={title},
      author={name},
      journal={IEEE Access},
      volume={1},
      pages={1-2},
      year={2019},
      publisher={IEEE}
    }

...

---
# Section Title

[@reference]

# References

---
nocite: '@*'
---
```
