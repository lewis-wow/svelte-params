# svelte-params
Route params manipulator


```js
import { locale, manipulate } from 'svelte-params'

// lang must be first param
$locale = $page.params.lang

// map items order must be the same as params order 
$manipulate = {
  'en': new Map([
     ['slug', 'king']
  ]),
  'cs': new Map([
     ['slug', 'kral']
  ])
}

$locale = 'cs' // trigger the change
```

## Skip slug

```js
$manipulate = {
  'en': new Map([
     ['slug', 'king'],
     ['slug2', 'name']
  ]),
  'cs': new Map([
     ['slug', null]
.    ['slug2', 'jmeno']
  ])
}
```

## Remove slug

```js
$manipulate = {
  'en': new Map([
     ['slug', 'king'],
     ['slug2', 'name']
  ]),
  'cs': new Map([
     ['slug', 'kral']
  ])
}
```
