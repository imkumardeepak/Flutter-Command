# ==========================
# 🚀 FLUTTER COMMANDS NOTES
# ==========================

# 📁 Create a new Flutter project
flutter create my_app              # Replace 'my_app' with your desired project name
cd my_app                          # Enter the project directory

# ▶️ Run the app in debug mode (default)
flutter run                        # Runs on connected device or emulator

# 📱 List connected devices
flutter devices                    # Shows all connected physical/emulator devices

# ▶️ Run the app on a specific device
flutter run -d DEVICE_ID           # Replace DEVICE_ID with the ID from 'flutter devices'

# 🔄 Get dependencies (after adding packages in pubspec.yaml)
flutter pub get

# ⬆️ Upgrade all packages to the latest versions
flutter pub upgrade

# 🧹 Clean the project (clears old builds, fixes weird issues)
flutter clean

# 🔍 Analyze code for errors, warnings, and best practices
flutter analyze

# 🧪 Run unit/widget tests
flutter test

# 📦 Build APK files

flutter build apk --debug          # Build a debug APK (not for release or store)
flutter build apk --profile        # Profile build for performance profiling
flutter build apk --release        # Build a release APK (used for production)

# Output location for APK:
# build/app/outputs/flutter-apk/app-release.apk

# 📦 Build an Android App Bundle (.aab) for Play Store
flutter build appbundle --release

# Output location for AAB:
# build/app/outputs/bundle/release/app-release.aab

# 📲 Install APK to a connected device
flutter install                    # Installs the last built APK to device

# OR manually install using adb (Android Debug Bridge)
adb install build/app/outputs/flutter-apk/app-release.apk

# 🩺 Doctor command (checks your environment setup)
flutter doctor                    # Fixes common setup issues and shows missing tools

# 🔄 Upgrade Flutter SDK to latest version
flutter upgrade

# 🌐 (Optional) Enable or disable web support
flutter config --enable-web
flutter config --no-enable-web

# ✅ You’re all set to build and deploy your Flutter app!




ios
# ==================================
# 🍏 FLUTTER COMMANDS FOR iOS BUILD
# ==================================

# 📁 Create a new Flutter project
flutter create my_app              # Replace 'my_app' with your project name
cd my_app                          # Move into project folder

# ▶️ Run the app in debug mode on an iOS device or simulator
flutter run                        # Auto-detects iOS if available

# 📱 List all available devices (iOS Simulators and connected devices)
flutter devices

# ▶️ Run on specific iOS device
flutter run -d DEVICE_ID           # Replace with iOS simulator or physical device ID

# 🔄 Get dependencies (after adding packages)
flutter pub get

# 🧹 Clean build folder (helpful if errors appear)
flutter clean

# 🔍 Analyze code
flutter analyze

# 🧪 Run tests
flutter test

# 🍏 Build iOS app in release mode (for App Store / internal testing)
flutter build ios --release

# 📂 Output location:
# build/ios/iphoneos/Runner.app

# 🔧 Open iOS project in Xcode (for signing, provisioning, etc.)
open ios/Runner.xcworkspace        # Use this, NOT .xcodeproj

# 🧾 Archive app for distribution via Xcode:
# In Xcode: Product → Archive → Distribute → App Store or Ad Hoc

# 🧪 Build in debug or profile mode for testing
flutter build ios --debug
flutter build ios --profile

# 🔄 Upgrade Flutter SDK
flutter upgrade

# 🩺 Check environment setup
flutter doctor                     # Check for Xcode, CocoaPods, etc.

# 🧰 (If needed) Install CocoaPods (iOS dependency manager)
sudo gem install cocoapods         # Run this if not already installed

# 📦 Install iOS dependencies (inside ios folder)
cd ios
pod install
cd ..
