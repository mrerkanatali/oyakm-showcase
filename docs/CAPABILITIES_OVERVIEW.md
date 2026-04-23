# Platform Capabilities Overview (Sanitized)

This file presents platform capabilities without exposing proprietary implementation.

## Flutter (iOS + Android)

- Unified mobile experience for members.
- Structured content consumption flows (news, announcements, blog-like feeds).
- Notification-driven deep-link behavior by content type.
- Locale-aware UX patterns and Turkish-first content presentation.
- Calculation tool family at category level (details kept proprietary).

## API Layer (PHP REST-style)

- Serves content and app configuration to mobile clients.
- Handles device registration and push-target eligibility.
- Supports controlled content distribution across client surfaces.
- Provides operational boundaries for admin-originated actions.
- Uses server-side integration patterns to avoid exposing sensitive keys on clients.

## Backend and Operations

- MySQL-backed content and operational records.
- Background processing model for notification dispatch jobs.
- Role-separated components: API, admin interface, worker process.
- Deployment-ready separation for public site, admin area, and service endpoints.

## Admin Capabilities

- Content management workflows for publishing and updates.
- Operational controls for notification campaigns.
- Audience scoping patterns (for example, test-only vs broader targets).
- Editorial lifecycle support from draft-like preparation to publish actions.

## Static Public Web

- Visitor-facing static site delivery.
- Optional server-side bridge model for controlled data access.
- Branding and content can be tailored per white-label deployment.

## Security and IP posture

- Showcase repo contains no source code and no secret material.
- Implementation logic, formulas, and internals remain private.
- Demo credentials are never committed and are only shared privately on request.
