# Prime on Linux :clapper:

This is a project that creates an independent Prime profile on your Firefox browser and makes it *almost* look like a Prime app. So, this is **not** an app.

> Also check out my [Netflix on Linux](https://github.com/kylethedeveloper/netflix-on-linux) project.

### Why I made this?

Because I do not recommend and use [DRM option](https://support.mozilla.org/en-US/kb/enable-drm) on my browser. Because I do not want to involve any plugin or extension or settings that do not respect my privacy. As known, Prime uses an advanced technology to protect its contents so you gotta compromise your privacy over your browser. Well, no. That's why I created a whole different profile **just to use** Prime.

## Requirements

To be able to use this on your Linux machine, requirements are:

- sudo privilege
- Firefox Browser
- GNOME Desktop Environment
- xdotool

## Installation

```shell
sudo git clone https://github.com/kylethedeveloper/prime-on-linux.git /opt/prime-on-linux
cd /opt/prime-on-linux
sudo ./install
```

### Installation script steps

`install` script does the following. Examine before running and use at your own risk :warning:

1. Create a new Firefox profile called '**primeonlinux**'
2. Copy the [profile properties](./properties) that I prepared to the newly created profile.
3. Run 'primeonlinux' profile for a moment to initialize the profile and close afterwards. (Initialization does not work sometimes)
4. Copy the [prime.desktop](./prime.desktop) file to the **/usr/share/applications** directory.
5. Restart GNOME Shell. (equivalent to Alt+F2+'r'+Enter)

## Uninstall

To uninstall prime-on-linux from your system, go to application directory and run `uninstall` script.

```shell
cd /opt/prime-on-linux
sudo ./uninstall
```

### Uninstall script steps

`uninstall` script does the following. Examine before running and use at your own risk :warning:

1. Open up Firefox Profile Manager for user to delete **primeonlinux** profile. At this step, do the following to properly uninstall Firefox profile. This must be done by hand as there is no command for it.
   - Choose **primeonlinux** from the list.
   - Click **Delete Profile**.
   - Click **Delete Files** to remove all files associated with the profile.
   - Exit.
2. Delete files in `/opt/prime-on-linux` directory *(except uninstall script)*. If desired, directory must be deleted manually. To do so, run `sudo rm -rvf /opt/prime-on-linux`.
3. Delete `/usr/share/applications/prime.desktop` file.

## TODO

- [x] Make `user.js` more privacy friendly.
- [x] Prepare an uninstall script.
- [x] Add xdotool to requirements.

***

![*Prime Video in Application Menu*](https://user-images.githubusercontent.com/8023096/147381551-2621f666-5f20-4118-ad14-05d78e455e08.png)

**Note:** Prime homepage might not load at the first time you click on the icon, which it is supposed to. So the second time and forever will work.
