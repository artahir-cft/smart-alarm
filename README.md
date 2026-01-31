# Smart Alarm

Smart Alarm is an Android application that helps you wake up by requiring both biometric authentication (fingerprint) and physical activity (step counting) to stop the alarm. The app is designed to ensure you are fully awake before you can dismiss the alarm.

## How It Works

1. **Set an Alarm:**
	- Use the main screen to pick a time and set an alarm.
2. **Alarm Rings:**
	- When the alarm time is reached, a notification appears and the alarm sound starts.
3. **Stop Alarm Activity:**
	- To stop the alarm, you must scan your fingerprint once, then walk a minimum number of steps (default: 5), and finally scan your fingerprint a second time. The scans are sequential, not simultaneous.
	- Progress bars show your completion status for both tasks.
	- The alarm stops only after both requirements are fulfilled.

## Setup & Installation

1. **Clone the repository:**
	```
	git clone https://github.com/artahir-cft/smart-alarm.git
	```
2. **Open in Android Studio:**
	- Open the project folder in Android Studio.
3. **Build the project:**
	- Let Gradle sync and build the project.
4. **Run on device/emulator:**
	- Make sure your device/emulator has a fingerprint sensor and step counter sensor.
	- Grant required permissions (biometric, activity recognition) when prompted.

## Permissions

- Biometric (Fingerprint) authentication
- Activity Recognition (for step counting)

## Project Structure

- `app/src/main/java/its/unique/smartalarm/`
  - `MainActivity.kt`: Main screen to set alarms
  - `AlarmReceiver.kt`: Receives alarm broadcast and starts the alarm service
  - `AlarmService.kt`: Foreground service that plays alarm sound and shows notification
  - `StopAlarmActivity.kt`: Activity to stop the alarm using fingerprint and steps

## Notes

- The app requires a device with a fingerprint sensor and a step counter sensor.
- If the required sensors are not available, the alarm will stop automatically with a message.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.