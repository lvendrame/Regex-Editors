# Regex-Editors
Some regular expressions to use in find and replacers on editors

## JavaScript
Object attribution to define property.
  - Regex: (\w+)\.(\w+)\s?=\s?(.+)?;
  - Replace: $2: $3,
  - Ex.: foo.bar = 35;  -->  bar: 35,
