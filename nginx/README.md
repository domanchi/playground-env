# Nginx Playground

This Dockerfile is provided for easy setup of an nginx environment, that you
can test quick ideas on.

## Development Notes

### Keeping code DRY

1. If you need to reuse location blocks, write it in a different file, then
include it when necessary.

2. Use named location blocks to send code flow.
