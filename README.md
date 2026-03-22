# pub-app
The pub App of our group. Sports Event Finder

```markdown
# Sports Event Finder - Watch Party Locator

> An intelligent bridge connecting sports fans and bars — never watch a game alone again

## 📱 Overview

Sports Event Finder is a social app designed for sports viewing scenarios, solving the two-sided pain point: fans struggling to find bars showing specific games, and bars having difficulty reaching their target audience.

**Core Value**:
- For fans: real-time, accurate bar event information, with features for group viewing and fan community building
- For bars: efficient event promotion channels, improved operational efficiency, and increased foot traffic

## 🎯 Project Status

- **Phase**: MVP Development
- **Target Platforms**: iOS + Android (Cross-platform)
- **MVP Release**: TBD

## 🛠 Tech Stack

| Layer | Technology | Description |
|-------|------------|-------------|
| Frontend | Flutter | Single codebase for both iOS and Android |
| Backend | Firebase / Tencent CloudBase | Authentication, database, cloud storage (TBD) |
| Instant Messaging | Tencent Cloud IM | Private messaging and group chat |
| Map Services | Google Maps / Amap | Bar location, route navigation |
| Content Moderation | Cloud Content Safety API | Text and image auto-moderation |

## 📂 Project Structure

```
sports-event-finder/
├── app/                    # Flutter application root
│   ├── lib/                # Source code
│   │   ├── main.dart       # App entry point
│   │   ├── models/         # Data models
│   │   ├── screens/        # UI pages
│   │   ├── widgets/        # Reusable components
│   │   ├── services/       # Backend service calls
│   │   └── utils/          # Helper functions
│   ├── assets/             # Images, fonts, etc.
│   └── pubspec.yaml        # Flutter dependencies
├── backend/                # Backend code (cloud functions or self-hosted)
├── docs/                   # Project documentation
│   ├── MVP-features.md     # MVP feature list
│   ├── database-schema.md  # Database design
│   └── wireframes/         # UI prototype files
├── .gitignore              # Git ignore configuration
└── README.md               # Project documentation (this file)
```

## ✅ MVP Core Features

### User Side
- [ ] Phone number one-tap login
- [ ] Home feed (bars showing events, sorted by time/distance)
- [ ] Event filter (Football, Basketball, Other)
- [ ] Bar detail page (address, playing events, atmosphere tags)
- [ ] Favorite / follow bars
- [ ] Report function

### Bar Side
- [ ] Bar account login/registration (requires approval)
- [ ] Publish / edit event information (event name, time, notes)
- [ ] Venue information management (address, phone, business hours)

### Common
- [ ] Content moderation (third-party API integration)
- [ ] User feedback channel

## 🚀 Quick Start

### Prerequisites
- Flutter SDK >= 3.0
- Android Studio / Xcode (depending on target platform)
- Git

### Clone Repository
```bash
git clone https://github.com/[your-username]/sports-event-finder.git
cd sports-event-finder
```

### Install Dependencies
```bash
cd app
flutter pub get
```

### Environment Configuration
1. Copy `lib/config/config.example.dart` to `lib/config/config.dart`
2. Fill in your API keys (Firebase / Tencent Cloud, etc.)

### Run the App
```bash
# Run in debug mode
flutter run

# Build Android APK
flutter build apk --release

# Build iOS (requires macOS)
flutter build ios --release
```

## 📊 Database Schema (MVP)

### Users Collection
| Field | Type | Description |
|-------|------|-------------|
| userId | String | Primary key, unique identifier |
| phone | String | Phone number |
| nickname | String | Display name |
| avatar | String | Avatar URL |
| userType | String | Type: user / bar |
| createdAt | Timestamp | Registration time |

### Bars Collection
| Field | Type | Description |
|-------|------|-------------|
| barId | String | Primary key, references users.userId |
| name | String | Bar name |
| address | String | Street address |
| latitude | Double | Geographic latitude |
| longitude | Double | Geographic longitude |
| phone | String | Contact number |
| atmosphereTags | Array | Tags (quiet/lively/fan zone, etc.) |
| businessHours | String | Operating hours |

### Events Collection
| Field | Type | Description |
|-------|------|-------------|
| eventId | String | Primary key |
| barId | String | Publishing bar ID |
| sportType | String | football / basketball / other |
| matchName | String | Event name (e.g., "Manchester United vs Liverpool") |
| startTime | Timestamp | Match start time |
| notes | String | Additional info (e.g., "Happy hour specials available") |
| status | String | upcoming / ongoing / ended |

### Favorites Collection
| Field | Type | Description |
|-------|------|-------------|
| userId | String | User ID |
| barId | String | Bar ID |
| createdAt | Timestamp | Time favorited |

## 🤝 Contributing

This project is currently in MVP development. If you're interested in contributing or becoming a technical partner, please reach out.

### Contact
- **Project Lead**: [Your Name]
- **Email**: [Your Email]
- **GitHub Issues**: Please submit issues in this repository

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

*Last updated: March 2026*
```

---

## Instructions

This README is ready to use. Please update the following placeholders:

1. **GitHub repository URL**: Replace `[your-username]` in `https://github.com/[your-username]/sports-event-finder.git` with your actual GitHub username

2. **Contact information**: Update `[Your Name]` and `[Your Email]` at the bottom

3. **Tech stack**: If you end up choosing different technologies (e.g., LeanCloud instead of Firebase), update the Tech Stack table accordingly

4. **License**: If you don't have a LICENSE file yet, either create one (MIT is recommended) or remove the License section

---

## Next Steps

After adding this README to your repository, you'll also want to:

1. **Create `.gitignore`** — use Flutter's official template if this is a Flutter project
2. **Create `docs/MVP-features.md`** — document your MVP feature list in detail
3. **Create `docs/database-schema.md`** — expand on the database design

Would you like me to write the **MVP-features.md** or **database-schema.md** files as well? Or are you ready to create the repository and start adding these files?
