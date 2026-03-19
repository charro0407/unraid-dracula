### [Unraid](https://unraid.net)

#### Install using the Unraid Plugin Manager

1. Open your Unraid WebUI;
2. Navigate to **Plugins** > **Install Plugin**;
3. Paste the following URL:

```
https://github.com/charro0407/unraid-dracula/raw/refs/heads/main/dracula.theme.plg
```

4. Click **Install**.

#### Install using the terminal

SSH into your Unraid server and run:

```bash
plugin install https://github.com/charro0407/unraid-dracula/raw/refs/heads/main/dracula.theme.plg
```

#### Updating the theme

To update to the latest version:

```bash
rm -f /boot/config/plugins/dracula.theme/dracula-theme.css /usr/local/emhttp/plugins/dracula.theme/dracula-theme.css
plugin remove dracula.theme
wget -q -O /tmp/dracula.theme.plg "https://raw.githubusercontent.com/charro0407/unraid-dracula/main/dracula.theme.plg?nocache=$(date +%s)"
plugin install /tmp/dracula.theme.plg
```

#### Uninstalling

```bash
plugin remove dracula.theme
rm -rf /boot/config/plugins/dracula.theme
```

#### Activating theme

1. Go to **Settings** > **Utilities** > **Dracula Theme**;
2. Set **Enable Dracula Theme** to **Enabled**;
3. Click **Apply**;
4. Refresh your browser.
