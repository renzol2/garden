---
tags: computer-science
---

# gRPC

**gRPC** is a high performance framework for implementing [[remote-procedure-call|RPC]] [[application-programming-interface|APIs]] using [[hypertext-transfer-protocol|HTTP 2.0]] as an underlying transport protocol.

- initially created by Google
- based around the idea of defining a _service_ and specifying its methods that can then be called remotely with their parameters and return types

A client uses a gRPC API by:

- deciding which procedure to call
- calculating the parameter values to use, if any
- using a code-generated stub to make the call, passing the parameter values

## Sources

- <https://cloud.google.com/blog/products/api-management/understanding-grpc-openapi-and-rest-and-when-to-use-them>
