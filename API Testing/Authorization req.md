 API Test: Authorization 

## Request

- **URL**: `{{baseUrl}}/posts/`
- **Method**: POST

## Variables

| Variable Name | Value                       |
|---------------|-----------------------------|
| `baseUrl`     | `https://simple-books-api.glitch.me`|

## Body
```json
{
    "clientName": "{{name}}",
    "clientEmail": "{{email}}"
}
```
## Pre-request scripts
```javascript
let name = pm.variables.replaceIn('{{$randomFirstName}}')
let email = pm.variables.replaceIn('{{$randomEmail}}')
pm.collectionVariables.set("name", name)
pm.collectionVariables.set("email", email)
```
## Tests

```javascript
const token = pm.response.json();
pm.test("Expect the response to be an object", function () {
    pm.expect(pm.response.json()).to.be.an('object');
    pm.collectionVariables.set('authToken', token.accessToken);
    console.log(pm.collectionVariables.get('authToken'));
});
