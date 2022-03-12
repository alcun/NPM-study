# Intro 

We have used JS to add interactivity to the front end of a page, build and SPA and do algos.
It can be used on the backed(server) also to build entire web apps.
Microservices - small modular apps that work together to form something bigger.
We will learn to write back end apps with node js and npm.
We will build apps with Express framework and a people finder microservice with MongoDB and Mongoose Library.

---

# NPM

Npm is a command lin etool used to install, create and share packages of JS code writted for nodjs.
These can cut out a lot of build time so we are not ‘reinventing the wheel’ every time.
We will look at the basics of npm and working with package.json to manage installed dependencies. 


package.json is the center of any node.js project or npm package.
It stores info about our project as a <head> section of html describes the page content.
key value pairs - name + version
we can have an author field in a simple string
eg “author”: “Slarti Bartfast”

for larger projects we can use an object with contact or other details.

note: in JSON all field names use “ double quotes” and are separated with a comma , 

# FCC

We cloned repo in command line 
e.g. $ git clone https://github.com/libgit2/libgit2

we then made a heroku account
used heroku local web to test
used heroku create
in package.json added our npm version in ‘engines’
make sure our start script is server.s (for this project)
added our git ignore with `
/node_modules
npm-debug.log
.DS_Store
/*.env
`


then 
git add .
git commit -m""
git push heroku HEAD:master 

it the gave us the ad of the server where it is hosted and we are able to access that in the browser 

as we have added our author key to the package.json it passes the challenge when linked to FCC 

# package.json description 
summarise a project here and what it does 
"description": "A project that does something awesome",

we can add some keywords too
    "keywords": [ "alcun", "academic", "learning", "freecodecamp" ],


# Adding a license

License field will let user know what they can do with the project 
open source licences include MIT and BSD 

"license": "MIT",

# Add a version
we do this to let users know what the current ver is 

    "version": "1.2.0",


# Adding packages

We can use package.json to make sure we get thte right dependencies when setting up on a new computer - npm instakk
in the dependency section of our package.json we can let npm know which packages we need eg

"dependencies": {
  "package-name": "version",
  "express": "4.14.0"
}

for FCC we will add ver 2.14.0 of moment package - useful for time and dates 

#Semantic Versioning

SemVer is industry standard for versioning software 

this can help us understand changes in projects when updated 

"package": "MAJOR.MINOR.PATCH"##


major will increment when we make incompatible api changes

minor increments we we add functionality in a backwards compatible manner 

patch increments when you make backwards-compatible bug fixes

patch - bug fix
minor - adds new features but wont break what worked before
major - changes that wont work with earlier versions 

for FCC we will change the ver of moment to natch major ver 2, minor v10 and patchv2

# Using tilde to always use the latest patch of a dependency 

adding specific versions with npm can freeze dependencies and maintain compatability but this can make you miss bugs and fixes 

to keep a dependency at the lates patch you can use a tilde eg 

"package": "~1.3.8"

this will keep it at any 1.3.x version

for FCC we will add a tilde to prefix our version of moment 

# Using caret char to update to latest minor ver of the dependency

we saw tilde kept us updated to latest patch, claret will do the same for minor 

"package": "^1.3.8"

this would give us any 1.x.x version of the package 

for FCC we willreplace our tilde with caret


# Removing a package from dependencies

this can be done by removing the key value pair from the json

for FCC we will remove moment (note we will have to remove preceeding comma too)