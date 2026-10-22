# container-prune

## Usage Guide
```bash
# copy files in the src folder to your server '~/.config/systemd/user' folder

# add job
systemctl --user daemon-reload
systemctl --user enable --now container-prune.timer

# execute on-demand
systemctl --user start container-prune.service

# check logs
systemctl --user status container-prune.service
journalctl --user -xeu container-prune.service

# remove job
systemctl --user disable --now container-prune.timer
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.