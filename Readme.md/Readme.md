<h1>RedStore Ecmmerce</h1>
<h1>Deploy</h1>
<h2>Features</h2>
<h3>Products Features</h3>

| Feature          | Coded |           Description                  |
|------------------|-------|----------------------------------------|
| Add a Product    |       | Ability to Add a Product on the System |
| List Products    |       | Ability to List Products               |
| Edit a Product   |       | Ability to Edit a Product              |
| Delete a Product |       | Ability to Delete a Product            |
| Stock            |       | Ability to Update the Stock            |
| Stock History    |       | Ability to see the Stock History       |

<h3>Purchase Features</h3>

| Feature          | Coded? |  Description                            |
|------------------|--------|-----------------------------------------|
| Create a Cart    |        | Ability to Create a new Cart            |
| See Cart         |        | Ability to see the Cart and it items    |
| Remove a Cart    |        | Ability to Remove a Cart                |
| Add Item         |        | Ability to add a new Item on the Cart   |
| Remove an Item   |        | Ability to Remove an Item from the Cart |
| Checkout         |        | Ability to Checkout                     |
 
 <h2>eCommerce</h2>
 eCommerce is an open source (test scenario) software made to create an easy and simple "Shop" API, where you have two micro services, one the Products API that stores and handles everything Related to Stock and Products. And the Purchase API where you can create orders (cart's) and checkout items.

The purpose of this repository is for education and test. But the code is being coded in a proper way.

<h2>Documentation</h2>
eCommerce has a full API documentation made with Swagger, you can check it by accessing this link.

If you have any Issue or bug you can submit a new Issue by accessing this link.

If you want to Contribute you can submit a Pull Request, remember to READ the Contributing Guide

<h2>Installation</h2>
Commerce is splitted into two standalone RESTful API's, so you can run it on whatever port you want. Installing eCommerce it's easy, the tutorial above will explain to you. eCommerce uses Groovy 2.4 and Grails 3.2.11.

You can run eCommerce in different ways. You can go to the Releases Page and download the source code of the latest release, or a bundled .war or a standalone java application (.jar).

<h2>Development</h2>
You can attach the .war in WebServers like Nginx using the Management Interface.

If you want run the standalone .jar just download it, and open your CMD/Terminal and write:
<h2>If you want RUN the Products API</h2>

```java -jar ecommerce-products-api-XXX.jar 
```
OR

```./products-api/grailsw run-app
```
You also can build from the sources by running the Grails Console, go to one of the API's folder

```purchase-api 
```
OR
```purchase-api 
```
OR
```products-api
```
and write on your CMD/Terminal the following:
```grailsw assemble
```
If you want to run it in development scenario, you can also do it by building the sources. You have two manner to do it. You can Gradle or directly Grails. Both products-api and purchase-api comes with Groovy, Grails and Gradle standalone packages. So you can run it without installing them.

<h2>Option #1 - Run by Gradle</h2>

```grailsw run-app
```
<h2>Production</h2>
roduction Environments are focused in being ready. That means, you just need execute the Jar File.
In the Production Environment all eCommerce API's are configured to work with MySQL in two databases; productsAPI and purchaseAPI and to work with a default username and password combination:

<h2>Note</h2>
.: Remember importing each SQL files using MySQL for Production. You can find them inside

```products-api/src/main/sql/
```
and

```purchase-api/src/main/sql/
```
<strong>.</strong>Username: commerce</strong>
<strong>.</strong>Password: commerceapi
<strong>.</strong>Database: productsapi & purchaseapi
<strong>.</strong>Port: 3306
You can change those credentials in the application.yaml file. In production environments you need import the database schema before running the software. Both products-api and purchase-api DDL files are available on this folder.

<strong>Notes</strong>

.: By default products-api runs on port 8080 and purchase-api on port 8090.
Note

.: In all Development and Test Scenarios, eCommerce uses H2 in-memory Database.


.: You can change your database credentials both for development/test and production scenarios in the app-config.yml available on each API sources root. Those configuration files can be used also externally, after building the .jar


.: You also can clean the sources and rebuild the sources by running
```grailsw clean
```
<strong>Running Test Cases</strong>
You can easily run the Test Cases using the standalone Grails package built-in with both the API's. Go to the home folder of one of them (products-api or purchase-api). And write on your CMD/Terminal:

```grailsw test-app
```
<strong>Credits</strong>
This development/educational scenario was coded and created under the GNU GPL v3 License. The objective of this repository is for practical test of RESTful API's with Java + Groovy.
