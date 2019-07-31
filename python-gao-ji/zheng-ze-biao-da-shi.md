# 正则表达式

##  匹配单个字符

| 代码 | 功能 |
| :--- | :--- |
| . | 匹配任意1个字符（除了\n） |
| \[ \] | 匹配\[ \]中列举的字符 |
| \d | 匹配数字，即0-9 |
| \D | 匹配非数字，即不是数字 |
| \s | 匹配空白，即 空格，tab键 |
| \S | 匹配非空白 |
| \w | 匹配非特殊字符，即a-z、A-Z、0-9、\_、汉字 |
| \W | 匹配特殊字符，即非字母、非数字、非汉字 |

## 匹配多个字符

| 代码 | 功能 |
| :--- | :--- |
| \* | 匹配前一个字符出现0次或者无限次，即可有可无 |
| + | 匹配前一个字符出现1次或者无限次，即至少有1次 |
| ? | 匹配前一个字符出现1次或者0次，即要么有1次，要么没有 |
| {m} | 匹配前一个字符出现m次 |
| {m,n} | 匹配前一个字符出现从m到n次 |

## 匹配开头和结尾

| 代码 | 功能 |
| :--- | :--- |
| ^ | 匹配字符串开头 |
| $ | 匹配字符串结尾 |

## 匹配分组相关正则表达式

| 代码 | 功能 |
| :--- | :--- |
| \| | 匹配左右任意一个表达式 |
| \(ab\) | 将括号中字符作为一个分组 |
| `\num` | 引用分组num匹配到的字符串 |
| `(?P<name>)` | 分组起别名 |
| \(?P=name\) | 引用别名为name分组匹配到的字符串 |


