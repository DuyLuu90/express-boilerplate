# Setup:
   
- `git clone <CLONE-URL> <name> && cd $_ && -rf .git && git init`
- `npm i knex pg postgrator-cli uuid uuidv4 valid-url winston xss`
- `D dependencies: mocha, chai,suptertest,nodemon`
- ./package.json-- "script":
    
    -`"migrate": "postgrator --config postgrator-config.js"`
    -`"migrate:test": "env NODE_ENV=test npm run migrate",`
    
- ./postgrator-config.js:
- ./Procfile: ` web: node src/server.js`
- ./.env: `DB_URL, TEST_DB_URL, JWT_SECRET`
- Node modules: `morgan`, `express`, `cors`, `helmet`

# DEPLOYMENT:
- hide secret
- respect env PORT
- use minimal logging
- remove console logs
- hide sensitive server err message
- change API token
- make a Proclife: the file that Heroku look for to determine how to start the server Then in package.json, add "engines": {"node": "12.16.1"}
- audit our packages

**Heroku**:
-heroku login-> git push heroku master -> heroku ps:scale web=1 -> heroku open
    1. read the files->find the <package.json>->setup env variables
    2. see Node version->install dependencies, ignore devDependencies
    3. read the <Procfile>
- Setup env variables: ` heroku config:set <key>=<value>`

# Syntax: 
- Create content: `echo <content> > <fileName>`-> `export <key> = <value>` -> `echo $<key>`
- App obj: to SET: `app.set(key,val)`, to READ: `app.get(key)`, to CREATE route: `app.[method](path,handler)`
- Run Node: `node`-> excecute JS (console.log..), to close `ctrl-c` twice or`.exit`
- Execute a file: `node fileName`

# Notes:
- **Node** (JS run inside the machine):
    - API server can access ports on your machine
    - Generate dynamic content by connecting to a db
    
- **Express framework**: `express()`, app, request, response, router(mini app)
- **Best practices**:  Using CONTINUOUS INTEGRATION(CI) SERVICES, having multiple hosted env


    
