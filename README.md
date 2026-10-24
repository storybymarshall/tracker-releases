# Tracker

Tracker is a small Mac app that keeps your live projects on index cards. Each card's front shows the project, and the back holds its next steps. Focus view lists the one key next step from every project. Cards sync between your Macs through iCloud Drive.

This repo hosts Tracker's downloads and its update feed. The source code lives elsewhere.

## Download

**[Download Tracker (latest)](https://github.com/storybymarshall/tracker-releases/releases/latest/download/Tracker.zip)**

Tracker needs macOS 14 Sonoma or later on an Apple silicon Mac.

1. Open the downloaded `Tracker.zip`. Your Mac unzips it into `Tracker.app`.
2. Drag `Tracker.app` into your **Applications** folder.
3. Open it. The first launch needs one extra step, explained below.

Older versions are on the [Releases](https://github.com/storybymarshall/tracker-releases/releases) page.

## First launch: "Apple could not verify Tracker…"

Tracker isn't signed with an Apple Developer ID yet, so macOS blocks it the first time you open it. You only need to allow it once. After that, it opens normally, and updates install without asking again.

Pick one:

- **System Settings (macOS 15 Sequoia and later):** Open Tracker once and click **Done** on the warning. Then go to **System Settings › Privacy & Security**, scroll down to the message about Tracker, click **Open Anyway**, and confirm with your password.
- **Right-click (macOS 14 Sonoma):** In Applications, right-click (or Control-click) Tracker, choose **Open**, then click **Open** in the dialog.
- **Terminal (any version):** Run this command, then open Tracker as usual:

  ```bash
  xattr -dr com.apple.quarantine /Applications/Tracker.app
  ```

## Updates

Tracker checks for updates by itself and offers to install new versions. You can also choose **Tracker › Check for Updates…** at any time.

Every update is signed, and Tracker verifies that signature before it installs anything. The feed is at <https://storybymarshall.github.io/tracker-releases/appcast.xml>.
