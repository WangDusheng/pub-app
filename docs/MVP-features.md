MVP功能清单
# MVP Features

## User Side

### 1. Login / Register
- Phone number + SMS verification code login
- Auto-register on first login

### 2. Home Feed
- List of bars showing live/upcoming games
- Sorted by distance (nearest first)
- Each card shows: bar name, distance, match name, match time

### 3. Event Filter
- Three filters: Football, Basketball, Other
- Tap to show only bars showing selected sport

### 4. Bar Detail Page
- Bar name, address, phone number
- List of events showing at this bar
- Atmosphere tags (quiet / lively / fan zone)
- Favorite button
- Navigate button (opens map app)

### 5. My Page
- Avatar, nickname
- My favorites list
- Logout

---

## Bar Side

### 1. Bar Login / Register
- Phone number login
- First login: fill in bar name, address, phone, business hours
- Submit for approval (pending status)

### 2. Publish Event
- Select sport type (football / basketball / other)
- Enter match name
- Select match date and time
- Add notes (optional)
- Edit and delete support

### 3. Venue Management
- Edit bar info (name, address, phone, business hours)
- Edit atmosphere tags

---

## Admin Panel

### 1. Bar Approval
- View pending bars
- Approve / reject
- Add reason if rejected

### 2. Report Management
- View user reports
- Delete inappropriate content
- Mark as resolved

---

## Out of Scope for MVP

| Feature | Reason |
|---------|--------|
| Live scoreboard | Requires paid API, complex integration |
| AI recommendations | Needs user data, low priority for MVP |
| AR features | High complexity, value unproven |
| Live stream links | Copyright issues |
| Prediction / quiz games | Nice to have, not core |
| Real-time crowd level | Hard to implement, low accuracy |
| Multi-language | Can add later |
| Advanced filters (leagues) | Can add later |

---

## User Flow