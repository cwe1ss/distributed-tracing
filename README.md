# Distributed Tracing: Trace Context

This repository is associated with the [Distributed Trace Context Community Group](https://www.w3.org/community/trace-context/).

Specification for tracing context propagation format.

## Goal

This specification defines formats to pass trace context information across systems. Our goal is 
to share this with the community so that various tracing and diagnostics products can operate 
together.

## Resources

- Trace Context [Report](https://w3c.github.io/distributed-tracing/report-trace-context.html)
- Correlation Context [Report](https://w3c.github.io/distributed-tracing/report-correlation-context.html)
- Demo [app](https://w3c.github.io/distributed-tracing/try-it.html)

## Reference Implementations

TODO: add link here

## Why are we doing this?

* If this becomes popular, frameworks and other services will automatically pass trace IDs 
through for correlated requests. This would prevent traces from hitting dead ends when a request 
reaches an un-instrumented service.
* Once aligned on a header name, we can ask for a CORS exception from the W3C. This would allow 
browsers to attach trace IDs to requests and submit tracing data to a distributed tracing service.
* Loggers can reliably parse trace / span IDs and include them in logs for correlation purposes.
* Customers can use multiple tracing solutions (Zipkin + New Relic) at the same time and not have
 to worry about propagating two sets of context headers.
* Frameworks can *bless* access to the trace context even if they prevent access to underlying 
request headers, making it available by default.

# Contributing

See [Contributing.md](CONTRIBUTING.md) for details

## Editing report

- Report is generated by [ReSpec](https://github.com/w3c/respec/wiki)
- To view report locally - start the local server like `python -m SimpleHTTPServer` to avoid cross-site file loading issue
- You can preview report from your branch or fork `http://htmlpreview.github.io/?https://github.com/<organization or form name>/distributed-tracing/blob/<branch name>/report-trace-context.html`. It is useful to review PR suggestions.

# Other

Charter document for Working Group creation: https://w3c.github.io/distributed-tracing/charter.html