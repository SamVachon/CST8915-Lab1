# CST8915 Lab 1 - Algonquin Pet Store

**Student Name:** Samuel Vachon  
**Student ID:** 041101891  
**Course:** CST8915 Full-stack Cloud-native Development  
**Semester:** Fall 2026

## Demo Video

[Watch the demo video here](https://www.youtube.com/watch?v=d_IoEEbgk6o)

## Order Service

The Order Service is built using Node.js. Its job is to receive order requests from the store front and send the order information to RabbitMQ. When a user places an order on the website, the request is sent to the Order Service through port 3000.

This service acts as the connection between the user-facing application and the messaging system. Instead of processing everything directly, it sends the order to RabbitMQ so the order can be handled separately.

## Product Service

The Product Service is built using Rust. Its job is to provide the list of products that are shown on the store front. The service runs on port 3030 and returns product information such as the product name and price.

The store front sends a request to the Product Service when the page loads. The Product Service then sends back the product data, which allows the user to see and select items such as Dog Food, Cat Food, and Bird Seeds.

## Store Front

The Store Front is built using Vue.js. It is the part of the application that the user interacts with in the browser. It displays the available products, allows the user to select a quantity, calculates the total cost, and lets the user place an order.

The Store Front communicates with both backend services. It gets product information from the Product Service and sends completed orders to the Order Service. In this lab, the Store Front runs on port 8080.
