# ADR-0001: License Foldworks under GNU AGPLv3

- **Status:** Accepted
- **Date:** 2026-10-17

## Context

Foldworks is intended to be genuinely open-source software that can be
self-hosted without artificial feature restrictions.

Foldworks may also be offered as a hosted service. The project's commercial
model is based on charging for operating the software reliably rather than
withholding application functionality from self-hosted users.

The project therefore needs a license that permits use, modification,
redistribution, self-hosting, and commercial hosting while preserving the
open nature of modified versions of Foldworks, including versions operated
as network services.

## Decision

Foldworks will be licensed under the GNU Affero General Public License,
version 3.0 (AGPL-3.0).

The repository's LICENSE file contains the complete license text.

## Consequences

Users may use, study, modify, and redistribute Foldworks subject to the
terms of the AGPL-3.0.

Commercial use and commercial hosting are permitted.

Modified covered versions operated for users over a network are subject to
the AGPL-3.0 network-source provisions.

Foldworks Cloud does not receive a proprietary or feature-enhanced edition
of the application merely because it is commercially hosted.

The project may separately evaluate the licensing of clearly separable
components, libraries, APIs, SDKs, or other works if such components are
created in the future.

## Rationale

AGPL-3.0 aligns with the Foldworks Product Constitution:

- self-hosted Foldworks is the complete application;
- Foldworks Cloud sells operations rather than artificial software scarcity;
- users retain control over their collections and data;
- commercial competition is permitted;
- improvements to the covered application cannot avoid copyleft obligations
  merely by being offered exclusively as a network service.