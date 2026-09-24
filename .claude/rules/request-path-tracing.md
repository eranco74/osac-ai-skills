# Request path tracing

When designing or implementing a feature driven by an external API or CLI
request, trace its input from the user-facing entry point to the handler.

For OSAC, read the canonical `fulfillment-service/docs/REQUEST_PATH_TRACING.md`
in the `osac` mono-repo before editing. From `osac-workspace`, the same file is
at `osac/fulfillment-service/docs/REQUEST_PATH_TRACING.md`. It documents the
current REST gateway header matcher and the boundary checks needed when input
passes through routing, filtering, or transformation layers.

The REST gateway's default header matcher does not forward arbitrary custom
HTTP headers. Check the mux's custom matcher for each new header, and test that
the value reaches the gRPC server through the REST path.
