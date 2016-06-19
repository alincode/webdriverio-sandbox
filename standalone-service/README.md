# standalone service

## Step1 : init
```
mkdir sandbox && cd sandbox
npm init -y
npm i webdriverio -D
./node_modules/webdriverio/bin/wdio
mkdir -p ./test/specs/
mkdir -p ./errorShots/
npm install wdio-selenium-standalone-service --save-dev
```

## Step2 : edit wdio config
vi wdio.conf.js
```
browserName: 'chrome'
services: ['selenium-standalone'],
waitforTimeout: 50000,
```

## Step3 : edit npm config
vi package.json
```
"scripts": {
  "test": "wdio wdio.conf.js"
},
```

## Step4 : write sample test
```
vi test/specs/test.js
```

## Step5 : execute
```
npm test
```
