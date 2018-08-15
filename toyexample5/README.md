<h1 align='center'> Toy example 5) "Argosy"</h1>

<p align="center">
  <img width="400" src="https://media.giphy.com/media/Npt0Te9MTd2fe/giphy.gif" /><br />
   <sup><a href="http://www.orcandenizcilik.com/hidrografi-ctd-olcumleri.php">source</a></sup>
</p>

A provider is the one with data, computing power or both that wants to offer it on Ocean. 
Toy example 5) "Argosy" (_large trading vessels commonly built in the Ragusea regions of Dalmatia and Venice during the late 17th century_)) - hmm, life is too easy on Ocean so let's complicate stuff! Put computing instance plus some data and don't reveal (all of the) data to the consumer! Wow, now we are talking...

The first part of the tutorial will prepare a simple Flask app that will have data and offer computing power. 

## Flask app as a compute+data instance

We decided to take a little Flask app from [here](https://medium.com/@dvelsner/deploying-a-simple-machine-learning-model-in-a-modern-web-application-flask-angular-docker-a657db075280) and add it to our Ocean!

### Clone/Fork repository

First fork or clone the Flask repo e.g. `https://github.com/oceanprotocol/nautilina.git`
 
After cloning the repository go into the project folder:
`cd toyexample5`

Run `docker-compose up` which will start a Flask web application for the backend API (default port `8081`) and an Angular frontend served through a webpack development web server (default port `4200`).

In your browser navigate to: `http://localhost:4200` (or whatever port you defined for the frontend in `docker-compose.yml`).

### Backend development

Navigate inside the backend directory: `cd backend`
Install pip dependencies: `pip install -r requirements.txt`
Run `python app.py` in backend root (will watch files and restart server on port `8081` on change).

### Frontend development

Navigate inside the frontend directory: `cd frontend`
Assure you have [Nodejs](https://nodejs.org/en/), [Yarn](https://yarnpkg.com/en/docs/install) and the [angular-cli](https://cli.angular.io/) installed.
Install npm dependencies: `yarn install --pure-lockfile` 
Run `yarn start` in frontend root (will watch files and restart dev-server on port `4200` on change).
All calls made to `/api` will be proxied to the backend server (default port for backend `8081`), this can be changed in `proxy.conf.json`.

## Publish Flask app on Ocean

Try using [Pleuston](https://github.com/oceanprotocol/pleuston) and publish your Flask app! Don't forget that you do have to host your app and that Ocean serves as a marketplace:
<p align="center">
  <img width="500" src="https://github.com/oceanprotocol/nautilina/blob/master/imgs/publish_compute.png" />
</p>
And that is it! :)

### Contributing

We use GitHub as a means for maintaining and tracking issues and source code development.

If you would like to contribute, please fork this repository, do work in a feature branch, and finally open a pull request for maintainers to review your changes.

Ocean Protocol uses [C4 Standard process](https://github.com/unprotocols/rfc/blob/master/1/README.md) to manage changes in the source code.  Find here more details about [Ocean C4 OEP](https://github.com/oceanprotocol/OEPs/tree/master/1).

### License

```
Copyright 2018 Ocean Protocol Foundation

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```



