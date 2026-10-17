# Security Policy

Foldworks is currently in pre-development and does not yet have a production
application or supported release.

## Reporting vulnerabilities

Please do not disclose suspected security vulnerabilities through public
GitHub issues.

A private reporting mechanism will be established before Foldworks publishes
software intended for real-world deployment.

Until then, security concerns relating to project design or architecture may
be raised privately with the project maintainer.

## Security philosophy

Security is considered throughout development rather than being deferred until
the end of the project.

Areas expected to receive particular attention include:

- malicious or malformed uploaded files;
- PDF, PDO, image, and archive parsing;
- archive bombs;
- path traversal;
- resource exhaustion;
- authentication and authorization;
- tenant isolation;
- session security;
- CSRF and XSS;
- SQL injection;
- dependency security;
- backup and restore integrity;
- parser fuzzing.

A formal security hardening and threat-modeling phase will occur before a
public production-ready release.

This document will evolve as Foldworks becomes operational.