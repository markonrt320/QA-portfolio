# API Test: Get book that isn't on stock and put it in variable

## Request

- **URL**: `{{baseUrl}}/books?type=non-fiction&limit=2`
- **Method**: GET

## Authorization

- **Type**: Inherit from parent

## Variables

| Variable Name | Value                       |
|---------------|-----------------------------|
| `baseUrl`     | `https://jsonplaceholder.typicode.com`   |
| `id`          | `33`                       |

## Body

- **Empty**: This DELETE request does not require a request body.

## Tests

```javascript
const dataResponse = pm.response.json();

pm.test("Response time is less than 200ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(200);
});
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

const unavailableBook = dataResponse.find((book)=> {
    return book.available === false;
});
pm.test("Set variable of an unavailable book", function() {
    pm.expect(unavailableBook.available).to.be.false;
    if(unavailableBook.available === false){
        pm.collectionVariables.set("unavailableBookId", unavailableBook.id)
    }
});
