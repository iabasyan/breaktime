# BreakTime App Intro

![macOS Logo](https://img.shields.io/badge/macOS-15.0+-blue.svg)
![Swift Logo](https://img.shields.io/badge/Swift-5.9+-orange.svg)
![Apple Silicon Logo](https://img.shields.io/badge/Architecture-Apple%20Silicon-red.svg)

A macOS menu bar application that helps you maintain healthy work habits by reminding you to take regular breaks. Built with SwiftUI for Apple Silicon Macs.

# Features

### 🕒 Customizable Break Schedules

* Microbreaks: Short 20-second breaks to rest your eyes (default: every 10 minutes)
* Long breaks: Extended 5-minute breaks for stretching and movement (default: every 30 minutes)
* Fully adjustable intervals and durations

### 💪 Exercise Suggestions

* Random exercise suggestions for each break type
* Microbreak exercises: eye rest techniques, neck stretches, breathing exercises
* Long break exercises: walks, full-body stretches, hydration reminders

### 🔔 Smart Notifications

* Pre-break notifications to help you prepare
* Configurable advance notice (10 seconds for microbreaks, 30 seconds for long breaks)
* Respects macOS Do Not Disturb mode
* Custom notification sounds

### 🎯 Flexible Break Management

* Strict Mode: Enforce breaks without skip/postpone options
* Normal Mode: Skip breaks or postpone by 5, 10, or 15 minutes
* Global keyboard shortcuts for quick actions
* Statistics tracking (completed vs. skipped breaks)

### ⌨️ Keyboard Shortcuts

* ⌘X: Skip current break (customizable)
* ⌘⌥5: Postpone by 5 minutes
* ⌘⌥0: Postpone by 10 minutes
* ⌘⌥1: Postpone by 15 minutes

### 🎨 User Interface

* Clean, minimalist break overlay
* Menu bar integration with countdown timers
* Pause functionality (temporary or timed)
* Settings import/export

# Installation
### Requirements

macOS Tahoe
Apple Silicon Mac (M1/M2/M3/M4)

### Installation
Download the installer from the Releases page.


# Usage
### Basic Operation

1. Launch the app: BreakTime runs in your menu bar (clock icon)
2. Click the menu bar icon to view:

* Countdown to next microbreak
* Countdown to next long break
* Pause/Resume controls
* Settings access


3. During breaks: Follow the on-screen exercise suggestions or use skip/postpone options

### Settings Configuration
Access settings from the menu bar popup:

* Break Intervals: Adjust how often breaks occur
* Break Durations: Set how long each break lasts
* Strict Mode: Prevent skipping/postponing breaks
* Exercise Suggestions: Toggle random exercise prompts
* Notifications: Enable pre-break alerts and configure timing
* Do Not Disturb: Respect macOS DND mode
* Statistics: View completion rate and reset counters
* Launch at Login: Start automatically when you log in

### Pause Modes

* Toggle Pause: Pause indefinitely until you resume
* Timed Pause: Pause for 1-5 hours, then auto-resume
* Useful for meetings, focused work sessions, or lunch breaks

#### Settings Import/Export
Export your configuration to share across devices or back up your preferences:

1. Open Settings
2. Click "Export Settings" to save as JSON
3. Click "Import Settings" to load a configuration file

# Privacy

BreakTime:

* Runs entirely on your local machine
* Does not collect or transmit any data
* Does not require internet connectivity
* Stores preferences locally using UserDefaults

# Known Limitations

* Apple Silicon only (no Intel support)
* Requires macOS 15.0+ (SwiftUI dependencies)

# Troubleshooting
Notifications Not Appearing

1. Open System Settings > Notifications
2. Find "BreakTime" in the app list
3. Enable "Allow Notifications"
4. Ensure "Do Not Disturb" is configured appropriately

Launch at Login Not Working

1. Open System Settings > General > Login Items
2. Verify "BreakTime" is in the list
3. Use the "Configure" button in app settings if needed

Breaks Not Triggering

1. Check that the app is not paused (menu bar icon shows status)
2. Verify "Do Not Disturb" respect setting if DND is active
3. Ensure the app hasn't crashed (check Activity Monitor)

# Development
Architecture

* SwiftUI: Modern declarative UI
* Combine: Reactive state management
* UserNotifications: macOS notification framework
* AVFoundation: Audio playback for sounds
* ServiceManagement: Launch at login functionality
* Carbon: Global hotkey registration

# Key Components

* BreakManager: Core timer logic and state management
* BreakWindow: Full-screen break overlay UI
* MenuBarView: Status bar popup interface
* SettingsView: Configuration panel
* GlobalHotkeyManager: Keyboard shortcut handling

### Audio Files
Required audio files (not included in repository):

* notification.wav: Played when break starts
* breakEnd.wav: Played when break completes

Place these in the project bundle or the app will fall back to system beep.

* Contributing
Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add some AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

# Support
If you encounter issues or have suggestions:

1. Check existing issues for solutions
2. Open an issue on GitHub
3. Provide system info (macOS version, Mac model) when reporting bugs
---
Note: This is an independent project not affiliated with Apple Inc. All trademarks are property of their respective owners.
