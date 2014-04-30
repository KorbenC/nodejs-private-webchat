# _Realtime Chat with Node.js_

_Realtime chat system with Node.js and the socket.io library_

## Requirements
All dependencies are declared in the package.json file. They are not included in the zip and you will have to run npm install to get them.

### Dependencies
- express.js
- gravatar
- socket.io
- ejs

### Buzz Words
- [Node.js](http://nodejs.org/)
- [Heroku](https://www.heroku.com/)
- [Git](http://git-scm.com/)
- [JQuery](http://jquery.com/)
- [Twitter Bootstrap](http://getbootstrap.com/)
- [Glyphicons](http://glyphicons.com/)


### What's included

Within the download you'll find the following directories and files, You'll see something like this:

```
nodejs-private-webchat/
├── public/
│   ├── css/
│   │   ├── bootstrap.icon-large.min.css
│   │   └── stylesheet.css
│   ├── img/
│   │   ├── glyphicons.png
│   │   ├── nodejslogo.png
│   │   └── unnamed.jpg
│   └── js/
│   │   ├── chat.js
│   │   └── moment.min.js
├── views/
│   ├── chat.html
│   └── home.html
├── app.js
├── config.js
├── routes.js
└── package.json
```

## Testing
To begin running locally make sure you have [Node.js](http://nodejs.org/) installed and fork/clone this repo.

Navigate to directory

```
cd nodejs-private-webchat
```
Install dependencies

```
npm install
```
Start app on local server

```
node app.js
```

## Deploying

### _Setup_


1. [Create an account](https://id.heroku.com/signup), if you don’t have one already.
2. Install the [Heroku toolbelt](https://toolbelt.heroku.com/) for your operating system. It will give you access to the heroku command from a terminal window.
3. Initialize an empty git repository (explained below)
4. Push your code to Heroku. This will deploy it and give you a URL which you can share with your friends.

### _How to deploy_

Creating a git repo

```git
git init
```

Create a new empty text file named **.gitignore** with the following content:

```
node_modules/
```
Create a new empty text file named **Procfile** with the following content:

```
web: node app.js
```

Then commit the changes with these commands:

```
git add Procfile
git commit -m 'Added a procfile'
```

### _Pushing to Heroku_

First you need to login to heroku from the command line tool:

```
heroku login
```

Add your ssh key if one is not auto generated.

```
heroku keys:add
```

Create a new heroku application from the code in this folder:

```
heroku create
```

finally, push code.

```
git push heroku master
```

Your application code was sent to heroku, where their servers will process your package.json file and install all libraries that your app needs. Do this every time you need to upload a new version of the code (you must have made a commit beforehand). All that is left, is to enable websockets so that our real-time chat can work

```
heroku labs:enable websockets
```

Open it in a tab in your default browser.

```
heroku open
```

## License

The MIT License

Copyright (c) 2014 Korben Carreno

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
