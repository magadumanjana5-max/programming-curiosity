# HTTP

## Curiosity questions

46. What is HTTP?
   **Answer:** HTTP is an application protocol for exchanging requests and responses between clients and servers. It defines methods, headers, status codes, and message conventions; HTTPS is HTTP protected by TLS.
48. What happens when you click a button on a website?
   **Answer:** The browser runs event-handling code; depending on the button, it may update the page locally or send a request to a server. The server may read or change data and return a response that the browser uses to update the interface.
49. How does your request travel thousands of kilometres?
   **Answer:** Network protocols divide data into packets, and routers forward them hop by hop across connected networks using destination addresses. Physical links carry signals as radio waves, light, or electrical changes; routes and latency vary.
50. How does the server know where to send the response?
   **Answer:** The connection carries addressing and transport state so the server can send data back to the client endpoint. For HTTP, request headers also identify details such as the target host and requested resource; NAT and proxies may translate or relay the route.
