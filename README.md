# Simple Utils

Simple form validation build with pure Javascript

### Phone Number Validation

```javascript
const amount = '087739999776'
if (/^\d+$/.test(amount) || amount === '') { return amount }
```

### Email Validation

```javascript
const isValidEmail = (string) => {
  let regex = /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,})+$/
  return regex.test(string)
}

String.prototype.isValidEmail = function () {
  let regex = /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,})+$/
  return regex.test(this)
}
```

### Password Validation
```javascript
const isStrongPassword = (string) => {
  let regex = ^.*(?=.{8,})(?=.*[a-zA-Z])(?=.*\d)(?=.*[!#$%&? "]).*$
  return regex.test(string)
}
```

- ^.*              : Start
- (?=.{8,})        : Length
- (?=.*[a-zA-Z])   : Letters
- (?=.*\d)         : Digits
- (?=.*[!#$%&? "]) : Special characters
- .*$              : End

### Covert bytes to KB, MB, GB

```javascript
const getReadableFileSizeString = (fileSizeInBytes) => {
  let i = -1
  const byteUnits = [' KB', ' MB', ' GB', ' TB', 'PB', 'EB', 'ZB', 'YB']
  do {
    fileSizeInBytes = fileSizeInBytes / 1024
    i++
  } while (fileSizeInBytes > 1024)

  return Math.max(fileSizeInBytes, 0.1).toFixed(1) + byteUnits[i]
}
```

### Remove duplicates object from two array

```javascript
const arr1 = [{ id: "001", name: "kang" }, { id: "002", name: "abbad" }, { id: "003", name: "naufal" }]
const arr2 = [{ id: "001", name: "kang" }, { id: "002", name: "abbad" }]

const filtered = arr1.filter((base) => {
  return !arr2.find((target) => {
    return target.id === base.id
  })
})
```
