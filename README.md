# Error-handling-and-control-

const expected = true;
function compare(actual, success, failure) {
 if (actual === expected) {
 success();
 } else {
 failure();
 }
}
function onSuccess() {
 console.log('Value was expected');
}
function onFailure() {
 console.log('Value was unexpected/exceptional');
}
compare(true, onSuccess, onFailure);
compare(false, onSuccess, onFailure);
// Outputs:
// "Value was expected"
// "Value was unexpected/exceptional"
