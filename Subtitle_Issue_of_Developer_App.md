# Subtitle Issue of Developer App
## Issue
When using multiple language in macOS, the "Auto" mode of subtitle shows no title at all.

For example, I set Chinese as my primary language and English as second. When a video is playing, the "Auto" subtitle shows nothing. But if I choose Chinese or English manually, the subtitle shows.

If I removed English and leave only Chinese in System Settings. The "Auto" subtitle works. So the issue was on code level, you should use contain instead of equal. I assumed.

Developer 10.0.4 (1004.1.3). macOS Monterey 12.4 (21F79).