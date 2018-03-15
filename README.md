# Regex-Editors
Some regular expressions to use in find and replacer on editors

## JavaScript
### Object attribution to define property.
  - Regex: (\w+)\.(\w+)\s?=\s?(.+)?;
  - Replace: $2: $3,
  - Ex.: foo.bar = 35;  -->  bar: 35,

### Function definition to var object attribution.
  - Regex: function\s(\w+)\(\)\s+?{}
  - Replace: var $1 = {};
  - Ex.: function Foo() {}  -->  var Foo = {};

### Const function attribution to function definition.
  - Regex: const\s(\w+)\s?=\s?(\(.+\))\s?=>\s?{
  - Replace: function $1$2 {
  - Ex.: function Foo() {}  -->  var Foo = {};

### String template to Concatanation.
  - Regex: \${(.+?)}
  - Replace: " + $1 + "
  - Ex.: ${CCToolkit.getServiceUrl()}getimagedatastring?session=${CCToolkit.getSessionId()}&imageID=3  -->  " + CCToolkit.getServiceUrl() + "getimagedatastring?session=" + CCToolkit.getSessionId() + "&imageID=3"
  
### Enclosing string template to Normal enclosing string.
  - Regex: \`(.+?)\`
  - Replace: "$1"
  - Ex.: \`tttatsdgsdgdsg\`  -->  "tttatsdgsdgdsg"

#### String Template to String
  - myStr.replace(/\${(.+?)}/gi, '" + $1 + "').replace(/\`(.+?)\`/gi, "$1")
