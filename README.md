# Post Scheduler — Backend API

RESTful API for scheduling and automatically publishing social media posts across multiple platforms.

## Resources

| Resource | Description |
|---|---|
| `workspaces` | Team workspaces (multi-tenant) |
| `accounts` | Connected social media accounts (OAuth 2.0) |
| `posts` | Post drafts and scheduled posts |
| `publishes` | Publish history (immutable log) |
| `calendar` | Calendar view of scheduled posts |
| `media` | Media asset uploads |
| `schedules` | Recurring post schedule templates |

## API Spec

OpenAPI 3.1 spec is at [`openapi.json`](./openapi.json). Open it in [Swagger Editor](https://editor.swagger.io) by dragging the file in.

## Supported Platforms

`instagram` · `facebook` · `twitter` · `linkedin` · `tiktok` · `pinterest`

## Authentication

JWT Bearer token obtained via `POST /auth/token` (password or refresh grant).

## URL Structure

All resources are scoped to a workspace:

```
/v1/workspaces/{workspace_id}/posts
/v1/workspaces/{workspace_id}/accounts
/v1/workspaces/{workspace_id}/calendar?from=2026-05-01&to=2026-05-31
```
