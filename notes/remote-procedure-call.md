---
tags: computer-science
---

# RPC: Remote Procedure Call

A **remote procedure call** (RPC) is a distributed computing process where a computer program causes a subroutine to execute in a different "address space" (another computer on a shared network), which is coded as if it were a normal, local procedure call.

- i.e. programmer writes the same code whether the subroutine is local or remote, and they can call the subroutine remotely through RPC
- form of client-server interaction, usually implemented via a request-response system
- in OOP, RPCs are represented by _remote method invocation_ (RMI)

RPCs are used as the dominant model for designing and implementing distributed [[application-programming-interface|APIs]].

- RPC fits well with the thought processes and skills of programmers on both the producer and consumer side of an API
- learning procedures of RPC is very similar to learning a new programming library
- RPC implementations are usually efficient and encoded in binary formats
- RPC encourages relatively small messages

## RPC vs REST/HTTP

RPC and [[representational-state-transfer|REST]] (usually implemented as HTTP) are both common forms of designing and implementing [[application-programming-interface|APIs]]

They are formed through opposite conceptual models:

- RCP contains procedures as addressable entities, and data is hidden behind those procedures
- REST contains data entities ("resources" in HTTP specs), and behaviors are hiden behind the data (the system behaves to create, modify, and delete resources internally)

RPC (and [[grpc|gRPC]] in particular) are generally better for:

- enabling communication between distrbiuted systems that are owned and controlled by the same entity
- optimizing processing efficiency

## Sources

- <https://en.wikipedia.org/wiki/Remote_procedure_call>
- <https://cloud.google.com/blog/products/api-management/understanding-grpc-openapi-and-rest-and-when-to-use-them>
