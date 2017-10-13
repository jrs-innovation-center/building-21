<a target="\_slides" href="https://slide-img.now.sh?img=http://www.bandhgears.co.uk/7315165-set-of-gears-interconnected-forming-a-machine-concept.jpg">show slide</a>

To get started, you will need a text editor and `nodejs` installed.

* [Atom](https://atom.io/)
* [NodeJS v8.7+](https://nodejs.org)

Once you have an editor and nodejs, we need to setup your project.

Create a new folder called `twenty-one`

``` bash
mkdir twenty-one
```

Then cd into that directory and create a couple files:

``` bash
cd twenty-one
touch index.html index.css index.js
```

Lastly, we want to install a webserver to run our application:

``` bash
npm install serve -g
```

Open the folder in your text editor

``` bash
atom .
```

Lastly, run your server.

``` bash
serve -c 0 -s
```

You should now be all setup, lets go to your editor and add the following to your `index.html` page:

> You may just want to copy this, basically this just loads some polyfills and the SystemJS build system.

``` html
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Twenty One</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/fetch/2.0.3/fetch.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-polyfill/6.26.0/polyfill.min.js"></script>
    <script src="https://unpkg.com/getlibs"></script>
    <script>System.config({map:{
      'react': 'react',
      'react-dom': 'react-dom'
    }})</script>
  </head>
  <body>
    <div id="app">
      <img src="playing-cards-1.jpg" />
    </div>
    <script>System.import('./index.js')</script>
  </body>
</html>
```

Next, you want to add the following to your `index.css` file.

``` css
.card {
  width: 100px;
  height: 138px;
  padding-left: 5px;
  padding-right: 5px;
}
```

---

[Index](#)
