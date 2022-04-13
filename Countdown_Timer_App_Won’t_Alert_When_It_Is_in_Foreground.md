# Countdown Timer App Won't Alert When It Is in Foreground.
## Issue
When a countdown timer finishes, an alert with sound will start. However, the alert only starts when Countdown Timer is in background. If the app is in foreground, the alert won't start, until the user presses the watch screen.

## Steps
1. Open Countdown Timer app and create a countdown timer.
2. You can choose 1 minute to shorten the testing time. You can choose longer time, the result will be the same.
3. Keep the app in foreground. That means, you don't press the watch crown. The screen can go to energy saving mode, which causes the countdown timer seems stopped, but it still runs.
4. Wait until the countdown finishes.

### Expected
Alert is shown when the countdown finishes.

### Actually Happened
No alert is shown when the countdown finishes. The alert will not be shown until you press the watch screen.

## System
watchOS 8.5.1(19T252)