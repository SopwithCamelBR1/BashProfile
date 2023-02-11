# BashProfile
Repository for storing Bash Profiles and Functions

## Set Up
Clone this repository locally, making a note of the full path to the repository root.

Add the following to your `~/.bashrc` or `~/.bash_profile` file:

```
export GIT_BASH_PROFILE_ROOT="<FULL_PATH_TO_LOCAL_COPY_OF_THIS_REPOSITORY>"
if [ -f ${GIT_BASH_PROFILE_ROOT}/custom_profile ]; then
  source ${GIT_BASH_PROFILE_ROOT}/custom_profile
fi
```


### Windows Specific
Follow the above instructions and then add the following to [settings.json](https://learn.microsoft.com/en-us/windows/terminal/install#settings-json-file) of [Windows Terminal](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=en-gb&gl=gb&rtc=1), in the `"profiles: "list": [...` section:

```
{
    "commandline": "C:\\Program Files\\Git\\bin\\bash.exe",
    "guid": "{88cf1b51-b21d-43c7-a381-980e2498011d}",
    "hidden": false,
    "name": "GitBash",
    "icon": "C:\\Program Files\\Git\\mingw64\\share\\git\\git-for-windows.ico",
    "startingDirectory": "F:/git"
}
```

And add 

```
"defaultProfile": "{88cf1b51-b21d-43c7-a381-980e2498011d}",
```

to the [root layer of the settings.json](https://learn.microsoft.com/en-us/windows/terminal/customize-settings/startup#default-profile)