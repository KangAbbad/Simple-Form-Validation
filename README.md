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
