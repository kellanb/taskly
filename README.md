# Taskly 📋⏰

A modern React Native task management app built with Expo, featuring a shopping list and countdown timer with push notifications.

## 🚀 Features

### Shopping List
- **Add Items**: Quickly add items to your shopping list
- **Complete/Uncomplete**: Toggle items as completed with satisfying haptic feedback
- **Delete Items**: Remove items with confirmation alerts
- **Persistent Storage**: Your list persists between app sessions
- **Smart Sorting**: Completed items move to the bottom, with recent items on top

### Countdown Timer
- **Recurring Timer**: Set a 10-second countdown for recurring tasks
- **Visual Feedback**: Clear countdown display with days, hours, minutes, and seconds
- **Overdue Alerts**: Red background when tasks are overdue
- **Push Notifications**: Get notified when it's time to complete your task
- **Celebration**: Confetti animation when you complete a task
- **History Tracking**: Keep track of completion timestamps

## 🛠️ Tech Stack

- **React Native** (0.79.2) - Cross-platform mobile development
- **Expo** (SDK 53) - Development platform and tooling
- **TypeScript** - Type-safe JavaScript
- **Expo Router** - File-based routing system
- **AsyncStorage** - Local data persistence
- **Expo Notifications** - Push notification system
- **Expo Haptics** - Haptic feedback for better UX
- **date-fns** - Date manipulation utilities
- **React Native Confetti Cannon** - Celebration animations

## 📁 Project Structure

```
taskly/
├── app/                          # App screens (Expo Router)
│   ├── _layout.tsx              # Root layout
│   ├── index.tsx                # Shopping list screen
│   ├── counter/                 # Counter feature
│   │   ├── _layout.tsx          # Counter layout
│   │   ├── index.tsx            # Main counter screen
│   │   └── history.tsx          # Timer history
│   └── idea.tsx                 # Additional screen
├── components/                   # Reusable components
│   ├── ShoppingListItem.tsx     # Shopping list item component
│   └── TimeSegment.tsx          # Time display component
├── utils/                       # Utility functions
│   ├── storage.ts               # AsyncStorage helpers
│   └── registerForPushNotificationsAsync.ts  # Push notification setup
├── assets/                      # App icons and images
├── theme.ts                     # App theme configuration
└── package.json
```

## 🏃‍♂️ Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Expo CLI (`npm install -g expo-cli`)
- iOS Simulator (for iOS development)
- Android Studio (for Android development)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd taskly
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Run on your preferred platform**
   ```bash
   # iOS
   npm run ios
   
   # Android
   npm run android
   
   # Web
   npm run web
   ```

## 📱 Usage

### Shopping List
1. **Add items**: Type in the text input and press "Done" or submit
2. **Mark as complete**: Tap on any item to toggle its completion status
3. **Delete items**: Tap the red close button and confirm deletion
4. **View organization**: Completed items appear at the bottom with strikethrough text

### Countdown Timer
1. **Navigate to Counter**: Use the app navigation to access the counter screen
2. **Start timer**: Tap "I've done the thing!" to start/restart the 10-second countdown
3. **Track progress**: Watch the countdown display showing time remaining
4. **Get notified**: Receive push notifications when the timer expires
5. **View history**: Check your completion history in the history tab

## 🎨 Theme

The app uses a consistent color scheme defined in `theme.ts`:

- **Primary Blue**: #1a759f (buttons, accents)
- **White**: #fff (backgrounds)
- **Black**: #000 (text)
- **Grey**: grey (secondary text)
- **Light Grey**: #eee (completed items)
- **Red**: #ee6055 (delete buttons, overdue alerts)

## 🔧 Configuration

### Push Notifications
- The app requests notification permissions on first use
- Notifications are scheduled locally using Expo Notifications
- On physical devices, you'll need to enable notifications in device settings

### Storage
- Uses AsyncStorage for local data persistence
- Shopping list items are stored with completion timestamps
- Counter state includes notification IDs and completion history

## 🧪 Development

### Available Scripts

- `npm start` - Start Expo development server
- `npm run ios` - Run on iOS simulator
- `npm run android` - Run on Android emulator
- `npm run web` - Run in web browser
- `npm run lint` - Run ESLint code analysis

### Code Quality
- **TypeScript** for type safety
- **ESLint** with Expo and Prettier configs
- **Prettier** for code formatting
- Consistent component structure and naming

## 📋 Dependencies

### Core Dependencies
- `expo` - Expo SDK and development tools
- `expo-router` - File-based routing
- `react-native-safe-area-context` - Safe area handling
- `@react-native-async-storage/async-storage` - Local storage

### Feature Dependencies
- `expo-notifications` - Push notifications
- `expo-haptics` - Haptic feedback
- `date-fns` - Date manipulation
- `react-native-confetti-cannon` - Celebration animations
- `@expo/vector-icons` - Icon library

## 🚀 Deployment

This app is configured for deployment through Expo's build services:

1. **Build for iOS**: `expo build:ios`
2. **Build for Android**: `expo build:android`
3. **Deploy updates**: `expo publish`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is private and not licensed for public use.

## 🎯 Future Enhancements

- [ ] Custom timer intervals
- [ ] Multiple shopping lists
- [ ] Dark mode support
- [ ] Cloud synchronization
- [ ] Task categories and tags
- [ ] Advanced notification scheduling
- [ ] Data export functionality

---

Built with ❤️ using React Native and Expo 