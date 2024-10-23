---
layout: project
type: project
image: images/jee-duke-icon.png
title: Microprofile App
permalink: projects/jee
# All dates must be YYYY-MM-DD format!
date: 2021-09-26
labels:
  - JEE
  - Microservices
  - Microprofile
  - Payara
  - CRUD
  - REST
  - Hibernate
  - MVC
  - Primefaces

summary: I developed an microservice with a primefaces frontend running on a payara application server to create, update, delete, read and organize cars.
---

Teaser:
I developed an microservice with a primefaces frontend running on a payara application server to create, update, delete, read and organize cars.

<img class="ui image" src="{{ site.baseurl }}/images/jee-overview.png">
<img class="ui image" src="{{ site.baseurl }}/images/jee-create.png">
<img class="ui image" src="{{ site.baseurl }}/images/jee-read.png">
<img class="ui image" src="{{ site.baseurl }}/images/jee-update.png">
<img class="ui image" src="{{ site.baseurl }}/images/jee-delete.png">
<img class="ui image" src="{{ site.baseurl }}/images/jee-tableview.png">
<img class="ui image" src="{{ site.baseurl }}/images/jee-payara.png">


```xml
<?xml version="1.0" encoding="UTF-8"?>
<persistence version="2.1" xmlns="http://xmlns.jcp.org/xml/ns/persistence" 
             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
             xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/persistence http://xmlns.jcp.org/xml/ns/persistence/persistence_2_1.xsd">
    <persistence-unit name="PersistenceUnitName" transaction-type="JTA">
        <provider>org.eclipse.persistence.jpa.PersistenceProvider</provider>
        <jta-data-source>jdbc/carsdb</jta-data-source>
        <properties>
            <property name="eclipselink.create-ddl-jdbc-file-name" value="createDDL_ddlGeneration.jdbc"/>
            <property name="eclipselink.drop-ddl-jdbc-file-name" value="dropDDL_ddlGeneration.jdbc"/>
            <property name="eclipselink.ddl-generation.output-mode" value="both"/>
            <property name="eclipselink.logging.level" value="FINE"/>
            <property name="eclipselink.logging.level.sql" value="FINE"/>
            <property name="javax.persistence.schema-generation.database.action" value="drop-and-create"/>
        </properties>
    </persistence-unit>
</persistence>
```

Source: <a href="https://github.com/knanw/"><i class="large github icon"></i>app</a> 

