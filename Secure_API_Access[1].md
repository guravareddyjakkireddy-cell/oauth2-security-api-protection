# Secure API Access

## API Protection Strategy
The application protects APIs using role-based access control.

## Public Endpoints
| Endpoint | Access |
|---|---|
| `/auth/login` | Public |
| `/public/**` | Public |

## Secured Endpoints
| Endpoint | Required Role |
|---|---|
| `/api/user/**` | USER or ADMIN |
| `/api/admin/**` | ADMIN |

## Security Controls
- JWT bearer token required for secured APIs
- Role-based authorization
- Stateless session management
- Restricted CORS origins
- Security headers enabled
- CSRF disabled only for stateless API usage

## Example Secured Request
```http
GET /api/user/profile
Authorization: Bearer <access_token>
```
