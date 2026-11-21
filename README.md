# My Game Profile

This repo holds an encrypted backup of a Game Profile from everythingyouneed.dev. Without the password nothing in vault/ can be read.

The public profile (public/profile.json) only contains games, numbers and matches from the game APIs. For games without an API key (such as chess) it only holds the player name: viewers fetch the numbers and games themselves. Every 6 hours a GitHub Action (.github/workflows/refresh.yml) refreshes the games that need your own API key, using the encrypted secret GAME_PROFILE_REFRESH. Delete that workflow to stop it. View it at https://everythingyouneed.dev/tools/game/?u=klaasvm

Restore it on https://everythingyouneed.dev/tools/game/ via Settings, Fetch from GitHub. Don't edit anything here by hand: that can break the backup.
