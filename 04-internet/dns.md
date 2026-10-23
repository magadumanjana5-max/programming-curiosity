# DNS

## Curiosity questions

41. What happens when you type `google.com` into a browser?
   **Answer:** The browser checks whether it already has a usable address, then uses DNS resolution if needed. It connects to a server address, negotiates HTTPS for secure sites, sends an HTTP request, and renders the response; redirects, caches, and network intermediaries can add steps.
42. How does your computer find Google’s server?
   **Answer:** DNS supplies one or more IP addresses for the hostname, and routers forward packets toward a destination address. Large services may return different addresses based on location, load, or network conditions.
43. What is DNS?
   **Answer:** The Domain Name System is a distributed naming system that maps names such as `google.com` to records including IP addresses. A resolver asks DNS servers and may cache answers for their time-to-live period.

## Rabbit hole

- [How does your computer find another computer somewhere in the world?](../10-rabbit-holes/what-happens-when-you-open-google.md)
