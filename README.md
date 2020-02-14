# Simple Form Validation

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
