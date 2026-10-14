# Debounce

![Screenshot](https://raw.githubusercontent.com/markupboy/debounce-releases/main/.github/images/debounce.png)

Debounce is a small menu bar app for macOS that quiets the noise from GitHub. Instead of a stream of notifications, it shows the open pull requests that involve you, sorted by what each one needs next: what's waiting on you, what you're waiting on, and what's ready to go.

This repository hosts Debounce's signed and notarized builds, along with the update feed the app checks for new versions.

## What it shows

Click the icon in the menu bar to open your inbox. Pull requests are grouped into sections:

- **Needs your review**: someone asked you directly for a review.
- **Needs your teams' review**: a review was requested from a team you're on, but not from you.
- **Your drafts**: your open draft pull requests.
- **Waiting for reviews or checks**: your pull requests with reviews outstanding or checks still running.
- **Needs action**: your pull requests with requested changes, failing checks, or merge conflicts.
- **Ready to merge**: your pull requests that are approved and passing.

Click a pull request to open it on GitHub. Empty sections are hidden, so when nothing needs you, the inbox says so.

Debounce refreshes every five minutes. When a pull request shows up in a section or moves to a new one, you get a macOS notification. Clicking it opens the pull request. Team-only review requests don't notify.

Right-click the menu bar icon for Settings, Check for Updates, and Quit.

## Requirements

- macOS 15 (Sequoia) or later
- A GitHub account

## Installing

1. Download the zip from the [latest release](https://github.com/markupboy/debounce-releases/releases/latest).
2. Unzip it and move `Debounce.app` to your Applications folder.
3. Open it. The Debounce icon appears in your menu bar.

## Signing in

Open Settings from the right-click menu and choose **Sign in with GitHub**. Debounce copies a one-time code to your clipboard and opens GitHub in your browser. Paste the code there and approve access. Your token is stored in the macOS keychain.

Debounce asks for the `repo` scope because GitHub has no read-only option for private repositories. It only ever reads.

If pull requests from an organization are missing, the organization may restrict third-party apps. Choose **Organisation Access…** in Settings and request or grant access for Debounce.

## Updates

Debounce checks this repository for new releases and offers to install them. You can turn automatic checks off in Settings, or check by hand with **Check for Updates…** in the right-click menu.
