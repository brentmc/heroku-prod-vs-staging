# Heroku Prod vs Staging Test
----
## Purpose
I wanted to confirm that I could run two Heroku apps; staging and production from the one git repo.

I have done so by following [these steps](https://devcenter.heroku.com/articles/multiple-environments)

----
## Dev Live Reload
From develop branch

    npm run start:dev
[Dev App can be found here](https://localhost:8080)

----
## Staging Deployment
From develop branch

    npm run build
    git commit (new public/build.js) 
    git push origin develop
    git push staging develop:master

[Staging App can be found here](https://bm-env-test-staging.herokuapp.com/)

----
## Production Deployment
From master branch

    npm run build
    git commit (new public/build.js) 
    git push origin master
    git push prod master

[Production App can be found here](https://bm-env-test-prod.herokuapp.com/)
