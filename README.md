# MCCH TOKEN

An Android application for booking appointment tokens at Thrissur Govt. Medical College Chest Hospital (GMCCH).

## Tech Stack

### Frontend
- **Language**: Java
- **Framework**: Android SDK
- **Build Tool**: Gradle 8.9.3
- **Minimum SDK**: API 26 (Android 8.0)
- **Target SDK**: API 35 (Android 15)
- **Compile SDK**: API 36

### Libraries and Dependencies
- **UI Components**: AndroidX AppCompat, Material Design, ConstraintLayout, RecyclerView, CardView
- **Navigation**: AndroidX Navigation Component
- **Networking**: Volley
- **Image Loading**: Picasso
- **JSON Parsing**: Gson
- **Lifecycle Management**: AndroidX Lifecycle (ViewModel, LiveData)
- **Testing**: JUnit, Espresso

### Backend
- **Server**: PHP-based API hosted at https://gmcchtsrtoken.com/
- **Database**: (Assumed MySQL, based on typical PHP setups)

## Features

### User Features
- **User Registration/Login**: Secure login using CR number and credentials
- **View Doctors and Units**: Browse available doctors and hospital units
- **Book Appointments**: Schedule tokens for next day's consultations based on unit numbers
- **View Current Bookings**: Check upcoming appointments
- **Cancel Bookings**: Cancel existing appointments
- **Profile Management**: View and manage user profile

### Doctor Features
- **Doctor Login**: Secure authentication for medical staff
- **View Patient Bookings**: See scheduled appointments for their unit
- **Manage Appointment Status**: Update booking statuses (e.g., confirm, complete)

### General Features
- **Splash Screen**: App launch screen
- **Bottom Navigation**: Easy navigation between home and bookings
- **About Section**: Information about the app and hospital
- **Privacy Policy**: Terms and conditions dialog
- **Offline Support**: Basic offline functionality (limited)

## Project Structure

```
app/src/main/java/gmcch/vast/token/
├── MainActivity.java          # Main app activity with navigation
├── SplashScreen.java          # Launch screen
├── About.java                 # About page
├── Config.java                # API endpoints configuration
├── SharedPrefManager.java     # Shared preferences for user data
├── UserSharedPrefManager.java # User-specific preferences
├── Adapter/                   # RecyclerView adapters
│   ├── CustomDoctorListAdapter.java
│   ├── DoctorUserViewAdapter.java
│   └── MybookingviewAdapter.java
├── Doctor/                    # Doctor-related activities
│   ├── DoctorHomePage.java
│   └── DoctorLogin.java
├── ModelClass/                # Data models
│   ├── DoctorUserView.java
│   ├── DoctorlistModelclass.java
│   ├── MyBookingModelClass.java
│   ├── UnitModelclass.java
│   └── Users.java
├── User/                      # User-related activities
│   ├── UserHomePage.java
│   ├── UserLogin.java
│   └── ViewCurentBooking.java
└── ui/                        # Navigation fragments
    ├── home/
    └── notifications/
```

## API Endpoints

- `User_login.php` - User authentication
- `Doctor_login.php` - Doctor authentication
- `view_units.php` - Get hospital units
- `User_doctor_view.php` - View doctors
- `doctor_view.php` - Doctor's booking view
- `changestatus.php` - Update booking status
- `Booking.php` - Create new booking
- `cancel.php` - Cancel booking
- `Your_current_booking.php` - Get user's bookings

## Build and Run

1. **Prerequisites**:
   - Android Studio (latest version recommended)
   - JDK 8 or higher
   - Android SDK API 36

2. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd Token
   ```

3. **Open in Android Studio**:
   - Open Android Studio
   - Select "Open an existing Android Studio project"
   - Navigate to the project directory

4. **Build the project**:
   - Sync Gradle files
   - Build > Make Project

5. **Run on device/emulator**:
   - Connect Android device or start emulator
   - Run > Run 'app'

## Release Build

The project includes release configuration with:
- ProGuard enabled for code obfuscation
- Resource shrinking
- Signed APK generation

Release keystore: `upload-key.jks` (password: 12345678, alias: gectoken)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make changes and test thoroughly
4. Submit a pull request

## License

This project is proprietary software for GMCCH. All rights reserved.

## Contact

For support or inquiries, contact the development team at GMCCH.
