
#REST API 해보기
* Reference site
  * https://redux-advanced.vlpt.us/3/01.html
  * https://poiemaweb.com/js-rest-api

### REST API?
* ...

### Implements
* Necessary
  * json-server
  * json (or xml)
  * Postman (https://www.getpostman.com/apps)


### Step by Step
1. Install __json-server__
~~~
$ cd Desktop
$ mkdir json-server-exam && cd json-server-exam
$ npm i -g json-server
~~~

2. Create db file (db.json)
~~~
{
  "books": [
    { "id": 1, "title": "html", "author": "Lee" },
    { "id": 2, "title": "css", "author": "Kim" },
    { "id": 3, "title": "javascript", "author": "Park" }
  ]
}
~~~

3. Edit __package.json__ file
~~~
{
  "name": "rest-api-exam",
  "version": "1.0.0",
  "description": "",
  "scripts": {
    "serve": "json-server --watch db.json --port 5000"
  },
  "dependencies": {
    "json-server": "^0.12.0"
  }
}
~~~

4. Connect with db file & set port number & Run
~~~
$ json-server --watch db.json --port 5000
~~~

5. Postman에서 잘 작동하는지 확인할 수 있다
