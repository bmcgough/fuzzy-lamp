## Welcome to doc test site!

### Languages
#### bash
```bash
#!/bin/bash

. /app/lmod/lmod/init/bash
module use /app/modules/all
ml R/3.4.3-foss-2016b-fh2

for s in ~/*.R
do
  Rscript $s
done
```
#### R
```R
library('rhdf5')
```
#### python
```Python
import sys

if bob:
  print("bob")
```
### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/bmcgough/fuzzy-lamp/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
