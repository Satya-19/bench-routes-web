---
id: doc7
title: Basic Idea Explanation
sidebar_label: Basic Idea Explanation
---



**bench-routes** is a GUI-powered highly scalable testing tool that monitors the performance of the routes in any web/routing - application. Bench-routes would perform a series of networking algorithms and calculations involved to find the real-time state of routes in an application. It monitors the routes at regular intervals and analyzes the response and the time involved in the same. The moment, the delta in response rises above a threshold limit, an alert would be sent to the admin of the respective manager.


**Bench-routes (B)** follows a basic idea of pinging the server at a respective route.

Consider a server **S** that contains routes **R** respectively.

Let,
- **r** belongs to any route in **R**
- **t** be any time constant
- **tres** be a threshold above which the delta in response would lead to an alert to the admin
- **rmean** be the mean value of responses from **r** (where **r < tres**, since if **r** exceeds **tres**, an alert would be sent as an exceptional behavior of that particular route).
- **B** sends a request to **S** at **r** route in every **t** instant.**B** logs the response to any local storage in t intervals after each response is received.

Consider **tres** be 0.7 or 70% respectively. This means that for every consecutive response if the difference of the response length from the mean response length is >= **tres**, it would lead to alerting. **rmean** would update itself for every response < tres so that the **rmean** behaves ideally and updates itself with time, dynamic to changes.