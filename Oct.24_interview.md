# Interview
1. how to consume the xml data?
```
	 jQuery.parseXML()
```
```
var request = new XMLHttpRequest();
request.open("GET", "/path/demo.xml", false);
request.send();
var xml = request.responseXML;
var users = xml.getElementsByTagName("user");
for(var i = 0; i < users.length; i++) {
    var user = users[i];
    var names = user.getElementsByTagName("name");
    for(var j = 0; j < names.length; j++) {
        alert(names[j].childNodes[0].nodeValue);
    }
}
http://stackoverflow.com/a/10684344
```
2. Default object of jQuery?

  jQuery Object contains `length`, `context`, `selector` properties.
  http://stackoverflow.com/a/6445357/6157406

3. $http and $resource in AngularJS

4. $ajax call

  1. jQuery:
      ```
      $("button").click(function(){
        $("#div1").load("demo_test.txt", function(responseTxt, statusTxt, xhr){
            if(statusTxt == "success")
                alert("External content loaded successfully!");
            if(statusTxt == "error")
                alert("Error: " + xhr.status + ": " + xhr.statusText);
        });
    });
      ```
  2. JavaScript:
    ```
    /**
    * AJAX helper *
    * @param method ­ GET|POST|PUT|DELETE
    * @param url ­ API end point
    * @param callback ­ This the successful callback
    * @param errorHandler ­ This is the failed callback */
    function ajax(method, url, data, callback, errorHandler) {
      var xhr = new XMLHttpRequest();
      xhr.open(method, url, true);
      xhr.onload = function () {
        if (xhr.status == 200) {
          callback(xhr.responseText); }
        };
      xhr.onerror = function () {
      console.error("The request couldn't be completed.");
      errorHandler();
      };
    if (data === null) { xhr.send();
    } else {
    xhr.setRequestHeader("Content­Type", "application/json;charset=utf­8"); xhr.send(data);
    } }
    ```

5. Why use MongoDB
