# About searching on GitHub

Our integrated search covers the many repositories, users, and lines of code on GitHub.

## About searching on GitHub

You can search globally across all of GitHub, or scope your search to a particular repository or organization.

* To search globally across all of GitHub, type what you're looking for into the search field at the top of any page, and choose "Search all of GitHub" in the search dropdown menu.

* To search within a particular repository or organization, navigate to the repository or organization page, type what you're looking for into the search field at the top of the page, and press **Enter**.

  You can also use suggestions and completions in the search bar to quickly find what you need.

* If you click on the search bar in the top navigation of GitHub.com, you will see a list of suggestions organized by category, including recent searches and suggested repositories, teams, and projects that you have access to.

* Clicking on any of the specific suggestions will take you directly to the page for that suggestion (for example, the repository or project page). If you click on a recent search, depending on the type of search, the search term will appear in the search bar or you will be taken to the search results page for the search term.

* Once you start typing, you will see a list of completions and suggestions that match your query. You can click on a suggestion to jump to a specific location. As you continue to type, you will see more specific suggestions, such as code files you can jump to directly.

After typing a search query, you can press **Enter** to go to the full search results view, where you can see each match and a visual interface for applying filters. For more information, see [Searching using a visual interface](#searching-using-a-visual-interface).

> \[!NOTE]
>
> * You must be signed into a personal account on GitHub to search for code across all public repositories.
> * GitHub Pages sites are not searchable on GitHub. However you can search the source content if it exists in the default branch of a repository, using code search. For more information, see [Understanding GitHub Code Search syntax](/en/search-github/github-code-search/understanding-github-code-search-syntax). For more information about GitHub Pages, see [What is GitHub Pages?](/en/pages/getting-started-with-github-pages/about-github-pages)
> * Currently our search doesn't support exact matching.

After running a search on GitHub, you can sort the results, or further refine them by clicking one of the languages in the sidebar. For more information, see [Sorting search results](/en/search-github/getting-started-with-searching-on-github/sorting-search-results).

GitHub search uses an ElasticSearch cluster to index projects every time a change is pushed to GitHub. Issues and pull requests are indexed when they are created or modified.

## Types of searches on GitHub

You can search for the following information across all repositories you can access on GitHub.

* [Repositories](/en/search-github/searching-on-github/searching-for-repositories)
* [Topics](/en/search-github/searching-on-github/searching-topics)
* [Issues and pull requests](/en/search-github/searching-on-github/searching-issues-and-pull-requests)
* [Discussions](/en/search-github/searching-on-github/searching-discussions)
* [Code](/en/search-github/github-code-search/understanding-github-code-search-syntax)
* [Commits](/en/search-github/searching-on-github/searching-commits)
* [Users](/en/search-github/searching-on-github/searching-users)
* [Packages](/en/search-github/searching-on-github/searching-for-packages)
* [Wikis](/en/search-github/searching-on-github/searching-wikis)

## Searching using a visual interface

In addition to the search bar, you can search GitHub using the [search](https://github.com/search) page or [advanced search](https://github.com/search/advanced) page. Alternatively, you can use the interactive search in the GitHub Command Palette to search your current location in the UI, a specific user, repository or organization, and globally across all of GitHub, without leaving the keyboard. For more information, see [GitHub Command Palette](/en/get-started/accessibility/github-command-palette).

The [advanced search](https://github.com/search/advanced) page provides a visual interface for constructing search queries. You can filter your searches by a variety of factors, such as the number of stars or number of forks a repository has. As you fill in the advanced search fields, your query will automatically be constructed in the top search bar.

![Advanced Search page. Top search bar holds "kittens user:octocat" query. Under "Advanced options", "From these owners" text box holds term "octocat".](/assets/images/help/search/advanced-search.png)

## Searching repositories on GitHub.com from your private enterprise environment

If you use GitHub.com or GHE.com as well as GitHub Enterprise Server, and an enterprise owner has enabled unified search, you can search across both environments at the same time from GitHub Enterprise Server. For more information, see [About searching on GitHub](/en/enterprise-server@3.21/search-github/getting-started-with-searching-on-github/about-searching-on-github#searching-repositories-on-githubcom-from-your-private-enterprise-environment) in the GitHub Enterprise Server documentation.

## Further reading

* [Understanding the search syntax](/en/search-github/getting-started-with-searching-on-github/understanding-the-search-syntax)
* [Searching on GitHub](/en/search-github/searching-on-github)# User manual

[[toc]]

## Start Shizuku

Shizuku supports startup in the following three ways.

::: tip If you are using GrapheneOS

System settings - "Security" - "Secure app spawning" may need to be disabled.

[Source](https://github.com/RikkaApps/websites/pull/79#issue-1751837442)

:::

### Start with root

For rooted devices, just start directly.

### Start via wireless debugging

Starting with wireless debugging works on Android 11 or above. This startup method does not require a connection to a computer. Due to system limitations, the startup steps need to be performed again after each reboot.

#### Enable Wireless debugging

1. Search the web for how to enable "Developer options" for your device model
2. Enable "Developer options" and "USB Debugging"<br><br><img :src="$withBase('/images/enable_dev_options.png')" style="max-width:320px;width:100%">
3. Enter "Wireless debugging"<br><br><img :src="$withBase('/images/enter_wireless_debugging.png')" style="max-width:320px;width:100%">
4. Enable "Wireless debugging"<br><br><img :src="$withBase('/images/enable_wireless_debugging.png')" style="max-width:320px;width:100%">
   
#### Pairing (only needs once)

1. Start pairing in Shizuku<br><img :src="$withBase('/images/start_paring_from_shizuku.png')" style="max-width:320px;width:100%">
2. [Enable Wireless debugging](#enable-wireless-debugging)
3. Tap "Pair device with pairing code" in "Wireless debugging"<br><img :src="$withBase('/images/start_pairing.png')" style="max-width:320px;width:100%">
4. Enter pairing code in Shizuku's notificaiton<br><img :src="$withBase('/images/enter_pairing_code.png')" style="max-width:320px;width:100%">

#### Start Shizuku

<img :src="$withBase('/images/start_shizuku.png')" style="max-width:320px;width:100%">

If it does not start, try disabling and enabling wireless debugging.

### Start by connecting to a computer

This boot method works on unrooted devices running Android 10 and below. Unfortunately, this startup method requires a computer. Due to system limitations, the boot steps need to be performed again after each reboot.

#### What is `adb`?

Android Debug Bridge (`adb`) is a versatile command-line tool that lets you communicate with a device. The adb command facilitates a variety of device actions, such as installing and debugging apps, and it provides access to a Unix shell that you Can use to run a variety of commands on a device.

See [Android Developer](https://developer.android.com/studio/command-line/adb) for more information.

#### Install `adb`

1. Download "SDK Platform Tools" provided by Google and extract it to any folder

   * [Windows](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)
   * [Linux](https://dl.google.com/android/repository/platform-tools-latest-linux.zip)
   * [Mac](https://dl.google.com/android/repository/platform-tools-latest-darwin.zip)

2. Open the folder, right click to select

   * Windows 10: Open PowerShell windows here (**hold down Shift to show this option**)
   * Windows 7: Open command window here (**hold down Shift to show this option**)
   * Mac or Linux: Open Terminal

3. Enter `adb`, if success, you can see a long list of content instead of the prompt not finding adb.

::: tip
1. Please do not close this window. The "terminal" mentioned later refers to this window (if you closed the window, please go back to step 2)
2. If you use PowerShell or Linux/Mac, all `adb` should be replaced with `./adb`
:::

#### Setting `adb`

To use `adb` you first need to turn on USB debugging on your device, usually by following these steps:

1. Open system Settings and go to About.
2. Click "Build number" quickly for several times, you can see a message similar to "You are a developer".
3. At this point, you should able to find "Developer Options" in Settings,  enable "USB Debugging".
4. Connect the device to the computer and type `adb devices` in the terminal.
5. At this time, the dialog "Allow debugging" will appear on the device, check "Always allow" and confirm.
6. Enter `adb devices` again in the terminal. If there is no problem, you will see something like the following.

   ```
   List of devices attached
   XXX      device
   ```

::: tip
The steps for enabling Developer Options on different devices may vary, please search for yourself.
:::

#### Start Shizuku

Copy the command and paste into the terminal. If there is no problem, you will see that Shizuku has started successfully in Shizuku app.


::: details Command for Shizuku v11.2.0+

```
adb shell sh /sdcard/Android/data/moe.shizuku.privileged.api/start.sh
```
:::

## FAQ

Many manufacturers have made modifications to the Android system that prevent Shizuku from working properly.

### Start via wireless debugging: keeps showing "Searching for pairing service"

Please allow Shizuku to run in the background.

Searching for pairing service requires access to the local network, and many manufacturers disable network access for apps as soon as they become invisible. You can search the web for how to allow apps to run in the background on your device.

### Start via wireless debugging: immediately fail after tapping "Enter pairing code"

#### MIUI (Xiaomi, POCO)

Switch notification style to "Android" from "Notification" - "Notification shade" in system settings.

### Start via wireless debugging/Start by connecting to a computer: the permission of adb is limited

#### MIUI (Xiaomi, POCO)

Enable "USB debugging (Security options)" in "Developer options". **Note that this is a separate option from "USB debugging".**

#### ColorOS (OPPO & OnePlus)

Disable "Permission monitoring" in "Developer options".

#### Flyme (Meizu)

Disable "Flyme payment protection" in "Developer options".

### Start via wireless debugging/Start by connecting to a computer: Shizuku randomly stops

#### All devices

- Make sure Shizuku can run in the background.
- Do not disable "USB debugging" and "Developer options".
- Change the USB usage mode to "Charge only" in the "Developer options".
  
  On Android 8, the option is "Select USB configuration" - "Charge only".
  
  On Android 9+, the option is "Default USB configuration" - "No data transfer".

- (Android 11+) Enable "Disable adb authorization timeout" option

#### EMUI (Huawei)

Enable "Allow ADB debugging options in 'Charge only' mode" in "Developer options".

#### MIUI (Xiaomi, POCO)

Do not use the scan feature in MIUI's "Security" app, since it will disable "Developer options".

#### Sony

Don't click the dialog shows after connecting the USB, because it will change USB usage mode.

### Start via root: cannot start on boot

Please allow Shizuku to run in the background.
