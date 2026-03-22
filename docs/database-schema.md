数据库设计
# Database Schema

## Users Collection

| Field | Type | Description |
|-------|------|-------------|
| userId | String | Primary key |
| phone | String | Phone number |
| nickname | String | Display name |
| avatar | String | Avatar URL |
| userType | String | `user` / `bar` |
| createdAt | Timestamp | Registration time |

## Bars Collection

| Field | Type | Description |
|-------|------|-------------|
| barId | String | Primary key, references users.userId |
| name | String | Bar name |
| address | String | Street address |
| latitude | Double | Geographic latitude |
| longitude | Double | Geographic longitude |
| phone | String | Contact number |
| atmosphereTags | Array | Tags: `quiet`, `lively`, `fan_zone` |
| businessHours | String | Operating hours |
| status | String | `pending` / `approved` / `rejected` |

## Events Collection

| Field | Type | Description |
|-------|------|-------------|
| eventId | String | Primary key |
| barId | String | Bar ID (reference) |
| sportType | String | `football` / `basketball` / `other` |
| matchName | String | Event name |
| startTime | Timestamp | Match start time |
| notes | String | Additional info |
| status | String | `upcoming` / `ongoing` / `ended` |

## Favorites Collection

| Field | Type | Description |
|-------|------|-------------|
| userId | String | User ID |
| barId | String | Bar ID |
| createdAt | Timestamp | Time favorited |

## Reports Collection

| Field | Type | Description |
|-------|------|-------------|
| reportId | String | Primary key |
| userId | String | Reporter ID |
| targetType | String | `bar` / `event` / `user` |
| targetId | String | ID of reported item |
| reason | String | Report reason |
| status | String | `pending` / `resolved` |
| createdAt | Timestamp | Report time |

## Indexes (Firestore)

| Collection | Index | Type |
|------------|-------|------|
| events | sportType + startTime | Composite |
| events | barId + startTime | Composite |
| bars | location | Geo query |