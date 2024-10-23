---
layout: project
type: project
image: images/vuelogo.svg
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

<img class="ui image" src="{{ site.baseurl }}/images/vue01.png">

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

<img class="ui image" src="{{ site.baseurl }}/images/vue02.png">

- Navigation bar button for adding, editing, and deleting series.

<img class="ui image" src="{{ site.baseurl }}/images/vue03.png">

- Page for optimal price calculation:
  - Books are selected in the book page and stored temporarily.
  - On the cart page, clicking the button to calculate the optimal price loads data from temporary storage and displays the optimal price.

<img class="ui image" src="{{ site.baseurl }}/images/vue04.png">

  
- Testing:

  - JUnit: Unit testing framework for Java.
  -  Mockito: Mocking framework for unit tests.


Sample Code Integration

Java Backend – Simple REST Resource

````java
@Path("/books")
public class BookResource {


    @Inject
    BookRepository bookRepository;

    @GET
    @Produces(MediaType.APPLICATION_JSON)
    public List<Book> getAllBooks() {
        return bookRepository.listAll();
    }
    // ...
}
````


Vue Frontend – Simple Component

````typescript
<template>
  <v-container>
    <v-row>
      <v-col cols="12" sm="6" md="4" v-for="book in books" :key="book.id">
        <v-card>
          <v-card-title>{{ book.title }}</v-card-title>
          <v-card-subtitle>{{ book.author }}</v-card-subtitle>
        </v-card>
      </v-col>
    </v-row>
    <v-btn @click="calculateOptimalPrice">Calculate Optimal Price</v-btn>
  </v-container>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { useBooksStore } from '@/stores/booksStore';

export default defineComponent({
  setup() {
    const booksStore = useBooksStore();
    booksStore.fetchBooks();
    return {
      books: booksStore.books,
      calculateOptimalPrice,
    };
  },
});
</script>
````


JUnit Test Example

````typescript
@SpringBootTest
public class BookResourceTest {

    @Inject
    BookResource bookResource;

    @Test
    public void testGetAllBooks() {
        List<Book> books = bookResource.getAllBooks();
        assertNotNull(books);
        assertFalse(books.isEmpty());
    }
}
````


Mockito Test Example

````typescript
    @Test
    void testCalculateOptimalPrice_nonEmptyBasket() {
        Book book1 = new Book();
        book1.setId(1L);
        book1.setTitle("Book 1");

        Series series = new Series();
        series.setBooks(Arrays.asList(book1));

        when(seriesRepository.listAll()).thenReturn(Collections.singletonList(series));

        Response response = shoppingCartResource.calculateOptimalPrice(Arrays.asList(book1));
        assertEquals(Response.Status.OK.getStatusCode(), response.getStatus());
    }
````


Source: <a href="https://github.com/knanw/shop/"><i class="large github icon"></i>Webshop App</a> 

