# Dummy-Products

Project to do call outs to external api service and get products to persist in bbdd. It allows insertions of one/multiple products. It also requires authentification to do before actions.

## Usage
* Deploy apex classes in your org.
* From SF setup > Remote Site Settings you must create a new remote site (URL = https//dummyjson.com)
* Instantiate DummyProductsCallOuts class with two parameters (name and username). For testing use username: emilys and password: emilyspass.
* Execute method getSessionCredentials (if you don´t do that not allow get products). 
* Execute getOneProducts (for persist one object) or getAllProducts (for persist all products). If execute both action in same transaction only work the first one.
* One/Multiple objets are stored in bbdd (Note that duplicates product are not persisted).
  
## EXAMPLE TO EXECUTE FROM ANONIMOUS WINDOW 

DummyProductsCallOuts dPC = new DummyProductsCallOuts('emilys' , 'emilyspass');

dPC.getSessionCredentials();

// Exetue following methods in differents transactions:

//dPC.getOneProducts();

//dPC.getAllProducts();




