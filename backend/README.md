# Backend

## Tech Stack (TBD)

- [ ] Firebase (Firestore + Auth + Storage)
- [ ] Tencent CloudBase
- [ ] LeanCloud
- [ ] Custom Backend (Node.js / Go / Java)

## Data Models

See: `../docs/database-schema.md`

## API Endpoints (Planned)

### User Module
| Endpoint | Method | Description |
|----------|--------|-------------|
| /auth/login | POST | Phone number login |
| /auth/refresh | POST | Refresh token |
| /user/profile | GET | Get user profile |
| /user/profile | PUT | Update user profile |

### Bar Module
| Endpoint | Method | Description |
|----------|--------|-------------|
| /bars | GET | Get bar list |
| /bars/{id} | GET | Get bar details |
| /bars/{id}/events | GET | Get events at a bar |

### Event Module
| Endpoint | Method | Description |
|----------|--------|-------------|
| /events | GET | Get event list |
| /events | POST | Create event (bar side) |
| /events/{id} | PUT | Update event |
| /events/{id} | DELETE | Delete event |

### Favorite Module
| Endpoint | Method | Description |
|----------|--------|-------------|
| /favorites | GET | Get favorite list |
| /favorites/{barId} | POST | Add to favorites |
| /favorites/{barId} | DELETE | Remove from favorites |

## Environment Variables
Firebase
FIREBASE_API_KEY=
FIREBASE_AUTH_DOMAIN=
FIREBASE_PROJECT_ID=
FIREBASE_STORAGE_BUCKET=
FIREBASE_MESSAGING_SENDER_ID=
FIREBASE_APP_ID=

Or Tencent Cloud
TENCENT_SECRET_ID=
TENCENT_SECRET_KEY=
TENCENT_APP_ID=

Content Moderation API
CONTENT_MODERATION_API_KEY=

text

## Deployment

- Development: TBD
- Production: TBD