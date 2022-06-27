# Emero

## Table of Contents
* [Description](#description)
* [Preview](#preview)
* [Installation](#installation)
* [Models](#models)
* [Associations](#associations)
* [Contributing](#contributing)
* [Questions](#questions)

## Description

I built the back end for an e-commerce site by configuring a working Express.js API to use Sequelize to interact with a MySQL database.

## Demo

The following video shows the application's GET, POST, PUT, and DELETE routes to return all categories, all products, and all tags being tested in Insomnia:

![In Insomnia, the user tests “GET, POST, PUT, and DELETE routes”.](https://drive.google.com/file/d/18rZz6oNMgsUMHe2hRTRK31uA3Y_08qdd/view)

## Installation 
The user should clone the repository from GitHub and then install Node. Run npm i to install the other dependencies. Then run npm run seed to seed the database. Insomnia or Postman should also be installed to test API endpoints. 


### Models

My database contains the following four models, including the requirements listed for each model:

* `Category`

  * `id`

    * Integer.
  
    * Doesn't allow null values.
  
    * Set as primary key.
  
    * Uses auto increment.

  * `category_name`
  
    * String.
  
    * Doesn't allow null values.

* `Product`

  * `id`
  
    * Integer.
  
    * Doesn't allow null values.
  
    * Set as primary key.
  
    * Uses auto increment.

  * `product_name`
  
    * String.
  
    * Doesn't allow null values.

  * `price`
  
    * Decimal.
  
    * Doesn't allow null values.
  
    * Validates that the value is a decimal.

  * `stock`
  
    * Integer.
  
    * Doesn't allow null values.
  
    * Set a default value of `10`.
  
    * Validates that the value is numeric.

  * `category_id`
  
    * Integer.
  
    * References the `Category` model's `id`.

* `Tag`

  * `id`
  
    * Integer.
  
    * Doesn't allow null values.
  
    * Set as primary key.
  
    * Uses auto increment.

  * `tag_name`
  
    * String.

* `ProductTag`

  * `id`

    * Integer.

    * Doesn't allow null values.

    * Set as primary key.

    * Uses auto increment.

  * `product_id`

    * Integer.

    * References the `Product` model's `id`.

  * `tag_id`

    * Integer.

    * References the `Tag` model's `id`.

### Associations

* `Product` belongs to `Category`, and `Category` has many `Product` models, as a category can have multiple products but a product can only belong to one category.

* `Product` belongs to many `Tag` models, and `Tag` belongs to many `Product` models. Allow products to have multiple tags and tags to have many products by using the `ProductTag` through model.

## Contributing 
Contributors should reference the installation section.  

## Questions
Please contact me at carl.logerie92@gmail.com with any questions.