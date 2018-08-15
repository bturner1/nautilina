<h1 align='center'> Toy example 3) "Captain"</h1>

<p align="center">
  <img width="400" src="https://media.giphy.com/media/KzlCvI1DGtkre/giphy.gif" /><br />
   <sup><a href="https://www.gifbay.com/gif/pirate_bay_here_i_come-27420/">source</a></sup>
</p>

A consumer is the one that wants something from the Ocean. "Captain" wants more than just data. Always looking for more. He wants computing instance with some data in it!

Firstly, get the compute+data instance from [Pleuston](https://github.com/oceanprotocol/pleuston). If you are really hard-core data scientists that eats and sleeps Python, then please do the following commands to interface with Ocean. First, run [provider backend](https://github.com/oceanprotocol/provider-backend). Then, in Python:
```python
import wget
from ocean_web3.consumer import register2,consume
ID=register2()
```
ID is the resource identifier of a data+compute Flask instance. Where is it? Download the file and have a look :). 
```python
wget.download(consume(ID))
```

If you want to skip the above parts, you can take a look at what would you get at: 
[http://18.185.121.152:4200/home](http://18.185.121.152:4200/home)

The URL leads you straight to the frontend interface to interact with the SVM model. You are unable to see the data (intentionally) but can play with choosing the hyperparameters and getting the model parameters. 

### Model Training

Play around:
- Select a hyperparameter, train the model, get accuracy. 
- Below that, you can send your own iris flower object to the model and receive probabilities.

The current state of your model is constantly updated and stored in a model.pkl file.

![output](https://user-images.githubusercontent.com/15385040/44090861-e52322b6-9fcb-11e8-9a0b-f5d8dcdd2cf0.gif)

In this toy example, a user is not allowed to see the data being used i.e. the provider has protected their data. In other instances, the provider could allow the download of the sample data set.

### Outlook

Integrating [Fitchain](https://fitchain.io/) will enable on-premise training on sensitive data in secure enclaves. 
Also, we are working on integrating other well-known data science tools. 

## Contributing

We use GitHub as a means for maintaining and tracking issues and source code development.

If you would like to contribute, please fork this repository, do work in a feature branch, and finally open a pull request for maintainers to review your changes.

Ocean Protocol uses [C4 Standard process](https://github.com/unprotocols/rfc/blob/master/1/README.md) to manage changes in the source code.  Find here more details about [Ocean C4 OEP](https://github.com/oceanprotocol/OEPs/tree/master/1).

The Flask App by Daniel Elsner is a perfect example for open source community work. We are looking forward to stumble upon more such work or receive direct 
contribution to the Ocean network. 

## License

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
