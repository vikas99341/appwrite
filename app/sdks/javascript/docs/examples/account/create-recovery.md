let sdk = new Appwrite();

sdk
;

let promise = sdk.account.createRecovery('email@example.com', 'https://example.com');

promise.then(function (response) {
    console.log(response);
}, function (error) {
    console.log(error);
});