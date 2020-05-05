touch app.js - create file
open app.js - open file

npm i -g typescript
tsc --init (create ts config file)
npm i express


dev deps:

npm i -D typescript ts-node nodemon @types/node @types/express


npm scripts:

"start": "node dist/app.js" (start the compiled server)
"dev": "nodemon src/app.ts" (allows to use pure TS during dev without compiling)
"build": "tsc -p ." (build the ts to js for PROD)
