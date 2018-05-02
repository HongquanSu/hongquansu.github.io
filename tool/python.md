---                                                                                                                                                                                                                                                             
layout: default
title: "My Python Notes"
tagline: "python"
---

Python remove whitespace in a string :

If you want to remove leading and ending spaces, use str.strip():
```
sentence = ' hello  apple'
sentence.strip()
```
- Output : 
```
'hello  apple'
```

If you want to remove all spaces, use str.replace():
```
sentence = ' hello  apple'
sentence.replace(" ", "")
```
- Output : 
```
'helloapple'
```

If you want to remove duplicated spaces, use str.split() :
```
sentence = ' hello  apple'
" ".join(sentence.split())
```

- Output : 
```
'hello apple'
```
