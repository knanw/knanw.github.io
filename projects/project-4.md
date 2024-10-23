---
layout: project
type: project
image: images/webshop-vuelogo.svg
title: Webshop App
permalink: projects/microservice
# All dates must be YYYY-MM-DD format!
date: 2024-10-22
labels:
  - CloudNative
  - JakartaEE
  - Microservices
  - Quarkus
  - Clean
  - DDD
  - REST
  - Hibernate
  - MVVC
  - Panache
  - Lombok

summary: I developed an microservice with a primefaces frontend running on a payara application server to create, update, delete, read and organize cars.
---

<img class="ui image" src="{{ site.baseurl }}/images/webshop-vue01.png">

Teaser:

Welcome to our cutting-edge Book and Series Management Application! 
Experience the seamless integration of backend and frontend to efficiently manage your book collection while benefiting from optimal price scaling. 
My application offers an intuitive user interface and powerful features to enhance your shopping experience and make the most out of your collection.


Backend:

- Java: The core programming language of the application.
- Jakarta EE: Framework for building robust and scalable enterprise applications.
- Quarkus: Superfast and lightweight Java framework optimized for GraalVM and Kubernetes.
- Panache: Simplifies the usage of JPA/Hibernate.
- Lombok: Reduces boilerplate code through automatic code generation.
- Microsoft SQL Server: Relational database management system for data persistence.
- Docker: Containerizing the entire backend environment.


Frontend:

- Nuxt.js: Framework based on Vue.js for building universal Vue applications.
- Vue 3: Progressive JavaScript framework for building user interfaces.
- Vuetify: Material Design Component Framework for Vue.js.
- TypeScript: Static typing to improve code quality and maintainability.
- Pinia: State management library for Vue.js.


Frontend Management:

- Menu for adding, editing, and deleting books.

<img class="ui image" src="{{ site.baseurl }}/images/webshop-vue02.png">


- Navigation bar button for adding, editing, and deleting series.

<img class="ui image" src="{{ site.baseurl }}/images/webshop-vue03.png">


- Page for optimal price calculation:
  - Books are selected in the book page and stored temporarily.
  - On the cart page, clicking the button to calculate the optimal price loads data from temporary storage and displays the optimal price.

<img class="ui image" src="{{ site.baseurl }}/images/webshop-vue04.png">


- Testing:

  - JUnit: Unit testing framework for Java.
  -  Mockito: Mocking framework for unit tests.

Source: <a href="https://github.com/knanw/shop/"><i class="large github icon"></i>Webshop App</a> 

