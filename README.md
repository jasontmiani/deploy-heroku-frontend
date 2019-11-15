
# Deploy Heroku (Frontend)

## Steps to deploy ...

### 1) Did you deploy ** _ backend _ **?

Follow the steps to deploy ** _ backend _ ** [here] (https://github.com/cod3rcursos/deploy-heroku-backend).

### 2) Clone project repository ** _ frontend _ **

`` `bash
$ git clone https://github.com/cod3rcursos/deploy-heroku-frontend
`` `

### 3) Enter project folder ** _ frontend _ **

`` `bash
$ cd deploy-heroku-frontend
`` `

### 4) Install project dependencies ** _ frontend _ **

`` `bash
$ npm i
`` `

### 5) Change the file ** _ src / consts.js _ **

`` `javascript
export default {
    API_URL: 'https: // <yourbackend> .herokuapp.com/api',
    OAPI_URL: 'https: // <yourbackend> .herokuapp.com/oapi',
}
`` `

### 6) Run script to generate production build

`` `bash
$ npm run production
`` `

### 7) Add and Commit Locally the ** _ src / consts.js _ ** File

`` `bash
$ git add.
$ git commit -am 'Setting Backend URLs'
`` `

### 8) Create a project in Heroku via _Heroku CLI_

`` `bash
heroku create cod3r-my-money-app-frontend
`` `

> ** IMPORTANT **
>
> As an example, we'll call the Heroku app ** cod3r-my-money-app-frontend **, but you need to choose another unique name.

### 9) Select buildpack for NodeJS

`` `bash
$ heroku buildpacks: set heroku / nodejs
`` `

### 10) Set up the remote repository

`` `bash
$ heroku git: remote -a cod3r-my-money-app-frontend
`` `

> ** IMPORTANT **
>
> Use the ** name ** of your project.

### 11) Deploying the application via ** push ** into the repository.

`` `bash
$ git push heroku master
`` `

### 12) Set the Minimum Escalation Type (Free) - Step ** Optional **

`` `bash
$ heroku ps: scale web = 1
`` `

### 13) Open Application

`` `bash
$ heroku open
`` `

### 14) Check the log and check if everything went well - Step ** Optional **

`` `bash
$ heroku logs --tail
`` `
