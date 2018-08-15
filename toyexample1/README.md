<p align="center">
  <img width="400" src="https://media.giphy.com/media/l0MYCVtjdO2g7KbT2/giphy.gif" /><br />
   <sup><a href="https://giphy.com/gifs/lion-movie-lion-movie-sunny-pawar-l0MYCVtjdO2g7KbT2">source</a></sup>
</p>

<h1 align='center'> Toy example 1) "Cabin boy"</h1>

A consumer is the one that wants something from the Ocean. Toy example 1) "Cabin boy" just wants to get some data from Ocean by using one or two lines of code in Python. Make Cabin boy life simple.

First, we have to obtain an ID of an asset on the Ocean. 
If you already know the ID, you can skip the following section. 
#### Registering the data
If you don't know how, let's do it for you for a simple data asset. First, run [provider backend](https://github.com/oceanprotocol/provider-backend). Let's assume local install.
```python
import wget
from ocean_web3.consumer import register1,consume
ID=register1()
```
If you use _register1()_ function, ID will be of Boston housing data set (https://www.cs.toronto.edu/~delve/data/boston/bostonDetail.html).

#### Downloading the data
Consuming this resource means getting a temporary URL where you will be able to download data. How to download it using Python and just one line of code?
```python
wget.download(consume(ID))
```
_ocean_web3_ is the library you need to interact with Ocean in this simple way. 
Caveat: the _consume()_ function will use test network where you will get some free Ocean tokens.  

Thats it! Try to download other data sets, even publish your own e.g. using [Pleuston](https://github.com/oceanprotocol/pleuston). 


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


