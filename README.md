# spnotify
spnotify is a simple bash script that shows desktop notifications when the song played by Spotify changes.

# Installation
Save the spnotify file to any location contained in your `$PATH` variable so it can be found.
Alternatively you can also start it directly specifying the path to the file or set an alias.

Make sure the file is executable (`chmod +x spnotify`).

# Usage
- `spnotify` to toggle the script on/off.

- `spnotify start` start the script, do nothing if another instance is already running.

- `spnotify stop` stop the script if it is running.

# Config
The following variables can be customized directly in the script:

- `spnotify_dir`: The directory where spnotify saves the album art. You can set this to any path you want spnotify to save the images to, e.g. "/tmp/spnotify/" or "$HOME/.spnotify/". The default is `$HOME/.spnotify/`.

- `t_notification`: The time for which the natification is visible (in ms). The default is `8000`.

- `replace_previous_notifications`: If this is set to `true`, spnotify replaces the old notification when the song changes while the previous notification is still visible. The downside of this setting is that if you manually close a notification and the song changes while the closed notification would have still been visible, no new notification will be displayed. Set to `true` by default.

- `urgency`: The urgency level of the notification, can be `low`, `normal`, or `critical`. Set to `normal` by default.

# Why tho?
The Spotify settings include the option "Show desktop notifications when the song changes".
However, this works very unreliably and I did not like the formatting of the notification body,
so I wrote this script which does the same job but better.
