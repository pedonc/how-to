# How To

Below is documentation of several useful procedures.

# Automatically Refresh Website Via Console To Keep Session Alive

These instructions are for using the Web Console to automatically refresh a window to keep an authenticated session alive.

## Firefox Browser On Windows 10

1.  Open the Firefox Browser.
2.  Click the **Open menu** hamburger menu icon in the upper-right corner of the window.
3.  Click **Options**.
4.  In the left column of the Options window, click **Privacy & Security** (lock icon).
5.  Scroll down to the Permissions section, then uncheck **Block pop-up windows**.
6.  Click in the address bar at the top of the window, erase the `about:preferences#privacy` text, and type `https://www.wikipedia.org` then press the **Enter** key on the keyboard.
7.  Click in the address bar at the top of the window, erase the `https://www.wikipedia.org` text, and type `about:blank` then press the **Enter** key on the keyboard.
8.  Hold the **Ctrl** key on the keyboard, then press and release the **T** key on the keyboard to open a new tab.  Release the **Ctrl** key.
9.  In the address bar at the top of the window, enter the address of the site that you want to automatically refresh and press the **Enter** key on the keyboard.  This tab will be the main tab for your session.
10.  Sign in to the website in the main tab.
11.  Once you have signed into the website, navigate to a basic page that can be refreshed repeatedly to keep the session alive.  For example, the main landing page when you sign in or your account profile page may work.  Avoid for the moment any pages with forms that may change or expire while you are logged in.
12. Right-click on the address in the address bar and click **Copy** from the context menu.
13. At the top of the Firefox window, click on the left-most tab labeled **New Tab**.
14. On the keyboard, hold down the **Ctrl** key and the **Shift** key, then press and release the **K** key to open the Web Console.  Release the **Ctrl** and **Shift** keys.
15. Hold the **Ctrl** key on the keyboard and press and release the **V** key, then release the **Ctrl** key.  You may receive a warning in the console about pasting content.  Type `allow pasting` on the keyboard to allow pasting into the Web Console.  Delete all the text entered so that the cursor is blinking immediately after the >> prompt.
16. Type `refreshWindow = window.open("` into the Console after the >> prompt, then hold the **Ctrl** key on the keyboard and press and release the **V** key to paste in the address copied from the main window.  Release the **Ctrl** key on the keyboard.  After the address is pasted in, type `");` after the address.  As an example, if you are signed in to Dropbox on the main tab, the command might read `refreshWindow = window.open("https://www.dropbox.com/home");`.  This command will open a new browser window or tab with the address specified and will store a reference to that browser window or tab in the variable `refreshWindow`.
17. Press the **Enter** key on the keyboard to execute the command.  A new browser window or tab should open with the address that you specified in the command.  This is the refresh window and should not be interacted with until you are ready to end your session on the website.
18. At the top of the Firefox window, click on the left-most **New Tab**.
19. In the Web Console at the bottom of the window, click the mouse after the >> prompt and type `refreshTimer = setInterval(function(){refreshWindow.location.href="` then then hold the **Ctrl** key on the keyboard and press and release the **V** key to paste in the address copied from the main window.  Release the **Ctrl** key on the keyboard and type `"},2*60*1000);` after the address.  As an example, if you are signed in to Dropbox on the main tab, the command might read `refreshTimer = setInterval(function(){refreshWindow.location.href="https://www.dropbox.com/home"},2*60*1000);`.  This command will refresh the designated refresh window every two minutes (2 x 60 seconds per minute x 1000 milliseconds per second = 2 minutes).
20. Press the **Enter** key on the keyboard to execute the command.
21. If you want the browser to block pop-up windows, hold the **Ctrl** key on the keyboard and press and release the **T** key.  Release the **Ctrl** key.  Click the **Open menu** hamburger menu icon in the upper-right corner of the window.  Click **Options**.  In the left column of the Options window, click **Privacy & Security** (lock icon).  Scroll down to the Permissions section, then check **Block pop-up windows**.  Click the **Close tab** X icon on the **Options** tab to close the tab.
22. The commands entered in the Web Console at the bottom of the left-most New Tab will refresh the designated refresh browser window or tab every two minutes.  Leave the left-most New Tab and the designated refresh browser window or tab open and do not interact with them to keep the session alive.  Continue working in the main tab for your session and/or in new browser windows or tabs.
23. When you want to end your session, close the left-most New Tab and close the designated refresh browser window or tab, then sign out of the site in your main tab.

# Clear Settings In Google Chrome Browser To Stop Unwanted Notifications And Pages From Loading

## Chrome On macOS

1.  Quit all open applications on your computer.
2.  Click on the Apple icon in the upper-left corner of the screen, then click **System Preferences**.
3.  Click **Network**, then click **Ethernet** in the left column.  If Ethernet is not listed, go to step 5.
4.  Click on the gear icon below the left column, then click **Make Service Inactive** from the menu that appears.
5.  Click **Wi-Fi** in the left column of the Network preferences window.
6.  On the right side of the window, if available, click the button to **Turn Wi-Fi Off** (if Wi-Fi is already off, please leave it off).  Please note whether Wi-Fi was originally on or off for future reference.
7.  Restart your computer and sign back in to macOS.
8.  When you are back in macOS, click on the Apple icon in the upper-left corner of the screen, then click **System Preferences**.
9.  Click **Notifications**.
10. In Notifications preferences, click **Chrome** in the left column, then click **None** for the App Alert Style on the right.
11. Quit System Preferences.
12. Start Google Chrome (your computer should be disconnected from the Internet, so you may see errors).
13. Click the **Window** menu, then click **Extensions**.
14. Click the **Remove** button for any extensions listed that you don't know/don't need and confirm removal.
15. At the top-right of the Chrome window, click the three dot "More" menu icon, then click **Settings**.
16. Under "On startup," select **Open a specific page or set of pages**.  If there are pages listed, to the right of each address, click the three dot "More" menu icon, then click **Delete** and delete each page listed.
17. When there are no addresses listed, add `https://google.com` as a page to open.
18. Close all open tabs in Chrome.
19. Quit Chrome.
20. Click on the Apple icon in the upper-left corner of the screen, then click **System Preferences**.
21. Click **Network**, then click **Ethernet** in the left column.  If Ethernet is not listed, go to step 23.
22. Click on the gear icon below the left column, then click **Make Service Active** from the menu that appears.
23.  If Wi-Fi was originally on in step 6, click **Wi-Fi** in the left column of the Network preferences window.  On the right side of the window, click the button to **Turn Wi-Fi On**.
24. Restart your computer and sign back in to macOS.

At this point, hopefully Chrome will not provide any notifications, in which case you can skip the following procedure.

If you still have trouble at this point, you can reset many of the settings in Chrome to their defaults.  To do this, follow steps 1-12 above.  Then, in Chrome, at the top-right of the window, click the three dot "More" menu, then click **Settings**.  At the bottom, click **Advanced**.  Under "Reset Settings," click **Restore settings to their original defaults** and then **Reset Settings**.  Quit Chrome.  Follow steps 20-24 above.

# Enabling Encryption On Windows 10

Disk encryption is required to protect data on computers and data storage devices.

Microsoft BitLocker is the recommended tool for encrypting storage on Windows 10.  Unfortunately, Microsoft only provides BitLocker in Windows 10 Pro and Enterprise, not in Windows 10 Home.  If you have Windows 10 Pro or Enterprise installed on your computer, please go to the How To Encrypt With BitLocker section below and follow the instructions to encrypt your computer's disk.

If your computer has Windows 10 Home installed, there multiple possible ways to upgrade a Windows 10 Home computer to Windows 10 Professional and enable BitLocker encryption.  These include purchasing a Windows 10 upgrade from Microsoft's App Store or using your organization's Key Management Server (KMS, if available in your organization) to upgrade the license on a Windows computer (which does not require an additional purchase, but does require that the computer periodically check in with your organization's license server to remain active).

Another option, which works on some, but not all, Windows 10 Home computers, is to enable Microsoft's "Device Encryption" mode.  This mode is not BitLocker, it typically requires a Microsoft account and stores the decryption key in Microsoft's cloud, and the device must meet certain hardware requirements (many Windows 10 Home computers do not have the required specifications).

## Comparison Of Windows 10 Encryption Options

| Windows 10 Encryption Mode                             | Benefits                                                                                                                                                                            | Drawbacks                                                                                                                                                                                                  |
| ---                                                    | ---                                                                                                                                                                                 | ---                                                                                                                                                                                                        |
| Windows 10 Home Device Encryption                      | 1. No additional purchase<br/>2. Remains active<br/>3. No upgrade necessary                                                                                        | 1. Incompatible with most computers<br/>2. May require a Microsoft account and storing decryption key in cloud                                                                             |
| Purchased Windows 10 Pro Upgrade With BitLocker        | <ol><li>Remains active</li><li>Enables computer owner to privately store and manage decryption key</li>                                                                             | <ol><li>Cost</li></ol>                                                                                                                                                                                     |
| Organization KMS Windows 10 Pro Upgrade With BitLocker | <ol><li>No additional purchase (assuming organization has already procured requisite license)</li><li>Enables computer owner to privately store and manage decryption key</li></ol> | <ol><li>Only available if your organization purchases and maintains KMS licenses and infrastructure</li><li>Requires computer to periodically check in with organization's server to re-activate</li></ol> |

## Enabling Your Computer's Trusted Platform Module (If Available)

Regardless of which of these options you choose, it is important to first ensure that if your computer has a Trusted Platform Module (TPM) it is enabled.  A TPM is required for Windows 10 Home Device Encryption and it is recommended for BitLocker in Windows 10 Pro.  To do this, please:

1.  Back up all the important data on your computer.
2.  Disconnect all external drives and peripherals from your computer.
3.  If your device is portable, ensure that it is plugged into a power source.
4.  Sign into Windows with an account that has administrative privileges.
5.  Right-click on the Windows Start button in the lower-left corner of the screen and click **Device Manager**.
6.  In the Device Manager window that appears, look for a Security devices branch.  If it exists, expand it and see if a Trusted Platform Module is listed.  If it is, close the Device Manager window and proceed to one of the options below for enabling encryption on your computer.
7.  If no Trusted Platform Module is listed in the Device Manager, close the Device Manager window, then click the Windows Start button.
8.  Click the **Settings** (gear) icon in the left column of the Start menu.
9.  Click **Update & Security**.
10. Click **Recovery**.
11. Under the Advanced startup section, click **Restart now**.
12. After the computer restarts, click **Troubleshoot**.
13. Click **Advanced options**.
14. Click **UEFI Firmware Settings**.
15. Click **Restart**.  Your computer should restart into your device's hardware configuration utility.
16. The hardware configuration utility will vary depending upon the model computer you have.  Please be careful to not alter any settings inadvertently.  Look for any options to enable a TPM/Trusted Platform Module/Security device and enable the device if it is available and not enabled.  It may be necessary to refer to documentation from your computer's manufacturer.  It may also be the case that your computer does not have a TPM or any setting to enable one.
17. If you made any changes in step 16, please save the changes and exit your device's hardware configuration utility.  If you did not make any changes, please exit without saving changes.  The computer should restart into Windows.

Please refer to the instructions below for the 3 options to enable encryption.

## Option 1 - Use Device Encryption On Windows Home Computer, If Available

1.  Ensure that all the data on your computer are backed up.
2.  Disconnect all external drives and peripherals from your computer.
3.  If your device is portable, ensure that it is plugged into a power source.
4.  Sign into Windows with an account that has administrative access.
5.  Click the Windows Start button.
6.  Click the **Settings** (gear) icon in the left column of the Start menu.
7.  Click **Update & Security**.
8.  See if there is a Device Encryption option.  If the option is not listed, your computer does not support Device Encryption.  Please use one of the other options to upgrade your computer to Windows 10 Pro and encrypt via BitLocker.  If Device Encryption is listed, click it and follow the instructions to encrypt the computer.  Be sure to note the password that you use for encryption.

Importantly, once your device is encrypted, please be sure to regularly backup data from your computer to a secure location.  If your computer has hardware/software problems or is lost/stolen it may not be possible to recover data from the encrypted drive.

## Option 2 - Buy A Windows 10 Pro Upgrade From Microsoft

Please note that this option is the only one that requires an additional purchase (the options above and below, if available, have no associated extra monetary cost).

It is possible to purchase an in-place upgrade from Windows 10 Home to Windows 10 Professional (which includes BitLocker software) through the digital Microsoft App Store.  To do this, please:

1.  Ensure that all the data on your computer are backed up.
2.  Disconnect all external drives and peripherals from your computer.
3.  If your device is portable, ensure that it is plugged into a power source.
4.  Click the Windows Start button.
5.  Click the **Settings** (gear) icon in the left column of the Start menu.
6.  Click **Update & Security**.
7.  Click **Activation** in the left column.
8.  Click **Go To Store** and follow the instructions to purchase and install the upgrade from Windows 10 Home to Windows 10 Pro.

Once you have upgraded to Windows 10 Pro, please follow the instructions below in the How To Encrypt With BitLocker section to encrypt your computer with BitLocker.

## Option 3 - Use Your Organization's Key Management Server To Upgrade To Windows 10 Pro

Please note that this process will only work if your organization has purchased the required licenses from Microsoft and maintains KMS infrastructure.  Please consult your organization's administrators for more specific information.  The computer will need to connect to your organization's internal network to connect to the KMS server, both to complete the installation and periodically thereafter to re-authorize the Windows 10 Pro license.  To upgrade the computer to Windows 10 Pro:

1.  Ensure that all the data on your computer are backed up.
2.  Disconnect all external drives and peripherals from your computer.
3.  If your device is portable, ensure that it is plugged into a power source.
4.  Click the Windows Start button.
5.  Click the **Settings** (gear) icon in the left column of the Start menu.
6.  Click **Update & Security**.
7.  Click **Activation** in the left column.
8.  Click **Change Product Key**.
9.  Enter the generic Windows 10 Pro KMS Key from Microsoft, which is `W269N-WFGWX-YVC9B-4J6C9-T83GX` and follow steps to upgrade your edition of Windows.  The computer will restart (possibly several times).
10. When the computer has finished upgrading, log in to Windows with an account with administrative access.
11. Connect the computer to your organization's internal network (possibly utilizing VPN if your computer is off campus).
12. Once the computer is connected to your organization's network (either on-campus or via VPN), right-click on the Windows Start button and click **Windows PowerShell (Admin)**.
13. In the PowerShell window that appears, type `slmgr.vbs /skms KMSSERVERADDRESS` (where KMSSERVERADDRESS is the name of your organization's KMS server) and press the **Enter** key.
14. Type `slmgr.vbs /ato` and press the **Enter** key.
15. The computer should activate the Windows 10 Pro license.  Once the license is activated, the computer can be disconnected from your organization's network.

The computer will occasionally attempt to renew its activation via your organization's KMS server or will prompt for re-activation if it cannot automatically reactivate.  It is good practice to reconnect the computer to your organization's network at least once every few months to renew the activation.

Once you have upgraded to Windows 10 Pro, please follow the instructions below in the How To Encrypt With BitLocker section to encrypt your computer with BitLocker.

## How To Encrypt With BitLocker

1.  Ensure that all the data on your computer are backed up.
2.  Disconnect all external drives and peripherals from your computer.
3.  If your device is portable, ensure that it is plugged into a power source.
4.  Right-click on the the Windows Start button.
5.  Click **Run**.
6.  In the Open field, type `gpedit.msc` and press the **Enter** key.
7.  In the Local Group Policy Editor windows that appears, under the Computer Configuration section, expand Administrative Templates.
8.  Expand Windows Components.
9.  Expand BitLocker Drive Encryption.
10. On the right side of the window, double-click **Choose drive encryption method and cipher strength (Windows 10 [Version 1511] and later)** (you may need to resize the window, resize the columns on the right side, and/or scroll the window horizontally to view the correct setting, as there are several similarly named policy settings).
11. Click **Enabled**.
12. In the lower-left pane, set Select the encryption method for operating system drives to **XTS-AES 256-bit**.
13. Set Select the encryption method for fixed data drives to **XTS-AES 256-bit**.
14. Set Select the encryption method for removable data drives to **AES-CBC 256-bit**.
15. Click **OK**.
16. If you determined that your system does have a TPM installed and enabled in the "Enabling Your Computer's Trusted Platform Module (If Available)" section above, please skip to step 21.
17. Double click the **Operating System Drives** folder on the right side of the Local Group Policy Editor window.
18. On the right side of the window, double click **Require additional authentication at startup**.
19. Click **Enabled**.
20. Click **OK**.
21. Close the Local Group Policy Editor window.
22. Restart the computer and log in to an account with administrative access.
23. Right-click on the Windows Start button.
24. Click **Run**.
25. In the Open field, type `control panel` and press the **Enter** key.
26. In the upper-right corner of the Control Panel window that appears, from the View by pulldown menu, click **Large icons**.
27. Click **BitLocker Drive Encryption**.
28. For the Operating system drive (C:), click **Turn On BitLocker**.
29. If you have no TPM on your computer, you will be asked to Choose how to unlock your drive at startup.  Click **Enter a password**, enter a strong password and be sure to note the password, then click **Next**.
30. You will be asked How do you want to back up your recovery key?  Click **Print the recovery key**.  Select the **Microsoft Print to PDF** printer and click **Print**.  Save the PDF file to your Desktop folder with an identifiable name.  Once the PDF is saved, keep the BitLocker Drive Encryption (C:) window open and use Windows File Explorer to open the PDF file that was generated.  Ensure that you can read the contents of the PDF.  Close the PDF, then return to the BitLocker Drive Encryption (C:) window.
31. Click **Next**.
32. When prompted to Choose how much of your drive to encrypt, select **Encrypt entire drive (slower, but best for PCs and drives already in use)**.
33. Click **Next**.
34. Click **Start Encrypting**.
35. Windows will take a while to encrypt the computer's disk.  While this process is running, please backup the PDF file you created in step 30 to a secure location off your computer.  Keep the PDF secure; you will need it if you get locked out of your computer.

# Restoring Common Sidebar Shortcuts To Finder In macOS

If some of the default shortcuts in macOS Finder's sidebar are hidden or removed, they can be restored as follows:

1.  Quit all programs on the computer.
2.  Restart the computer and sign in.
3.  Click on the Finder icon on the Dock, then click the **Finder** menu and click **Preferences**.
4.  In the Finder Preferences window that appears, click the **Sidebar** tab.
5.  In the Favorites section, ensure that **Applications**, **Desktop**, and **Downloads** are checked.  In the Locations section, ensure that **Hard disks** is checked.  If these were already checked, please uncheck and re-check them.  Please note that Hard disks can be displayed with a minus (-) sign; please ensure that it shows as a checked box.
6.  Close the Finder Preferences window.
7.  If you do not see an open Finder window, click the **File** menu and click **New Finder Window**.
8.  On the left side of the window, the Sidebar column should be visible.  If it is not, click the **View** menu then click **Show Sidebar**.
9.  At the top of the Sidebar, you should see the Favorites section.  It may be necessary to scroll the sidebar up to see this section.
10. The Applications, Desktop, and Downloads icons should be visible under the Favorites section in the Sidebar.  If they are not, move the mouse cursor over the word **Favorites** in the Sidebar and click to show the Favorites section.

If the Finder is working properly, after making the above changes, the Desktop should show up on the Sidebar in file navigation windows when the Sidebar is visible.

# Fixing Issues With The Spotlight Indexing Service In macOS

A fundamental problem with file systems is that it is too slow to read through all the files on a disk every time a window is opened that needs to display the disk's contents.  macOS continually indexes files on the computer through a service called Spotlight so that applications can refer to the pre-compiled index of files instead of reading through the contents of the disk.  This, however, can cause problems if the Spotlight service crashes or doesn't keep up with changes made to the contents of a disk.  There may also be conflicts between Spotlight (built into macOS) and Dropbox, since Spotlight generally assumes that files listed in the disk's filesystem are on the disk, but Dropbox tries to present files that are on its cloud servers through the computer's file browser.  This could potentially cause Spotlight or applications that rely on Spotlight to try to read a file from the disk that isn't actually there (which could cause problems).  Both Apple and Dropbox are continually updating their software to try to work around these limitations and fix bugs, but there are many inherent conflicts with how these services work.

To start, it is possible to disable Spotlight, which also can be used to try to force Spotlight to re-build its index of the computer's files:

1.  Ensure that all your computer's data are securely backed up.
2.  Click the Apple menu (upper-left corner of the screen).
3.  Click **System Preferences**.
4.  Click the **Show All** (grid) button at the top of the window to display all the System Preferences.
5.  Click **Spotlight**.
6.  Click the **Privacy** tab.
7.  Click the plus (+) button.
8.  In the file browser that appears, select the main hard disk for your computer (often **Macintosh HD**) in the left Sidebar and click the **Choose** button.
9.  Confirm that you want to stop Spotlight from indexing the hard disk (even though it may break searching).
10. Close the Spotlight settings window.
11. Restart the computer and sign in.

The computer should now have Spotlight disabled, which may cause some programs to behave differently.  The next step is to update (not upgrade) macOS to see if Apple has fixed any Finder/Spotlight bugs that may be causing problems.  To do this:

1.  Click the Apple menu (upper-left corner of the screen).
2.  Click **System Preferences**.
3.  Click the **Show All** (grid) button at the top of the window to display all the System Preferences.
4.  Click **Software Update**.
5.  Importantly, Apple uses this location to advertise upgrades to new versions of macOS as well as provide updates to macOS.  At this point, please do not upgrade the full OS (e.g., to Mojave, Catalina, etc. as that can take a long time and cause several other issues).
6.  In the Software Update preferences, if there are any updates listed, click **More info**.  This should provide a checklist of updates available for your computer.  If there are no updates available for your computer, skip steps 7-9.
7.  Please ensure that all updates to your current macOS are checked and that any full upgrades to Mojave, Catalina, etc. are not checked.  As a note, if you are already running the latest version of macOS available on your computer (Mojave, Catalina, etc.), there may be a updates (not upgrades) that include Mojave or Catalina in the name (and these should be applied).  The key is to check/enable updates but not upgrades.
8.  Click **Install Now**.
9.  The computer will download updates.  Once the updates are downloaded and ready to install, please restart the computer (the system will likely prompt you to do so).  Applying the updates may take a while and your computer may reboot several times.  Once this process is finished, sign in to macOS.  Repeat steps 1-9 until there are no more updates (there may still be upgrades) listed for your computer.

Now that macOS is up-to-date, please re-enable Spotlight:

1.  Click the Apple menu (upper-left corner of the screen).
2.  Click **System Preferences**.
3.  Click the **Show All** (grid) button at the top of the window to display all the System Preferences.
4.  Click **Spotlight**.
5.  Click the **Privacy** tab.
6.  Click on your hard disk in the list and click the minus (-) button to remove the disk from the list and re-enable Spotlight indexing of the hard disk.
7.  Close the Spotlight settings window.
8.  Restart the computer and sign in.

The Spotlight service will re-index your computer's disk.  This can take a while.

# License

All content copyright (c) 2020 Curtis Glavin, Jonathan Huppi, Robert Burkey

All code in this repository is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License version 3 as published by the Free Software Foundation.

All code in this repository is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

A copy of the GNU General Public License version 3 is available [in this repository](https://raw.githubusercontent.com/pedonc/windows-deployment/master/LICENSE) and from the Free Software Foundation at [https://www.gnu.org/licenses/gpl-3.0.txt](https://www.gnu.org/licenses/gpl-3.0.txt).

All documentation in this repository is licensed under the GNU Free Documentation License version 1.3.

Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License, Version 1.3 or any later version published by the Free Software Foundation; with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license is included in the section entitled "GNU Free Documentation License".  Additionally, a copy of the license is available [in this repository](https://raw.githubusercontent.com/pedonc/windows-deployment/master/fdl.txt) and from the Free Software Foundation at [https://www.gnu.org/licenses/fdl.txt](https://www.gnu.org/licenses/fdl.txt).

## GNU Free Documentation License

Version 1.3, 3 November 2008

Copyright © 2000, 2001, 2002, 2007, 2008 Free Software Foundation, Inc. <https://fsf.org/>

Everyone is permitted to copy and distribute verbatim copies of this license document, but changing it is not allowed.

0\. PREAMBLE

The purpose of this License is to make a manual, textbook, or other functional and useful document "free" in the sense of freedom: to assure everyone the effective freedom to copy and redistribute it, with or without modifying it, either commercially or noncommercially. Secondarily, this License preserves for the author and publisher a way to get credit for their work, while not being considered responsible for modifications made by others.

This License is a kind of "copyleft", which means that derivative works of the document must themselves be free in the same sense. It complements the GNU General Public License, which is a copyleft license designed for free software.

We have designed this License in order to use it for manuals for free software, because free software needs free documentation: a free program should come with manuals providing the same freedoms that the software does. But this License is not limited to software manuals; it can be used for any textual work, regardless of subject matter or whether it is published as a printed book. We recommend this License principally for works whose purpose is instruction or reference.

1\. APPLICABILITY AND DEFINITIONS

This License applies to any manual or other work, in any medium, that contains a notice placed by the copyright holder saying it can be distributed under the terms of this License. Such a notice grants a world-wide, royalty-free license, unlimited in duration, to use that work under the conditions stated herein. The "Document", below, refers to any such manual or work. Any member of the public is a licensee, and is addressed as "you". You accept the license if you copy, modify or distribute the work in a way requiring permission under copyright law.

A "Modified Version" of the Document means any work containing the Document or a portion of it, either copied verbatim, or with modifications and/or translated into another language.

A "Secondary Section" is a named appendix or a front-matter section of the Document that deals exclusively with the relationship of the publishers or authors of the Document to the Document's overall subject (or to related matters) and contains nothing that could fall directly within that overall subject. (Thus, if the Document is in part a textbook of mathematics, a Secondary Section may not explain any mathematics.) The relationship could be a matter of historical connection with the subject or with related matters, or of legal, commercial, philosophical, ethical or political position regarding them.

The "Invariant Sections" are certain Secondary Sections whose titles are designated, as being those of Invariant Sections, in the notice that says that the Document is released under this License. If a section does not fit the above definition of Secondary then it is not allowed to be designated as Invariant. The Document may contain zero Invariant Sections. If the Document does not identify any Invariant Sections then there are none.

The "Cover Texts" are certain short passages of text that are listed, as Front-Cover Texts or Back-Cover Texts, in the notice that says that the Document is released under this License. A Front-Cover Text may be at most 5 words, and a Back-Cover Text may be at most 25 words.

A "Transparent" copy of the Document means a machine-readable copy, represented in a format whose specification is available to the general public, that is suitable for revising the document straightforwardly with generic text editors or (for images composed of pixels) generic paint programs or (for drawings) some widely available drawing editor, and that is suitable for input to text formatters or for automatic translation to a variety of formats suitable for input to text formatters. A copy made in an otherwise Transparent file format whose markup, or absence of markup, has been arranged to thwart or discourage subsequent modification by readers is not Transparent. An image format is not Transparent if used for any substantial amount of text. A copy that is not "Transparent" is called "Opaque".

Examples of suitable formats for Transparent copies include plain ASCII without markup, Texinfo input format, LaTeX input format, SGML or XML using a publicly available DTD, and standard-conforming simple HTML, PostScript or PDF designed for human modification. Examples of transparent image formats include PNG, XCF and JPG. Opaque formats include proprietary formats that can be read and edited only by proprietary word processors, SGML or XML for which the DTD and/or processing tools are not generally available, and the machine-generated HTML, PostScript or PDF produced by some word processors for output purposes only.

The "Title Page" means, for a printed book, the title page itself, plus such following pages as are needed to hold, legibly, the material this License requires to appear in the title page. For works in formats which do not have any title page as such, "Title Page" means the text near the most prominent appearance of the work's title, preceding the beginning of the body of the text.

The "publisher" means any person or entity that distributes copies of the Document to the public.

A section "Entitled XYZ" means a named subunit of the Document whose title either is precisely XYZ or contains XYZ in parentheses following text that translates XYZ in another language. (Here XYZ stands for a specific section name mentioned below, such as "Acknowledgements", "Dedications", "Endorsements", or "History".) To "Preserve the Title" of such a section when you modify the Document means that it remains a section "Entitled XYZ" according to this definition.

The Document may include Warranty Disclaimers next to the notice which states that this License applies to the Document. These Warranty Disclaimers are considered to be included by reference in this License, but only as regards disclaiming warranties: any other implication that these Warranty Disclaimers may have is void and has no effect on the meaning of this License.

2\. VERBATIM COPYING

You may copy and distribute the Document in any medium, either commercially or noncommercially, provided that this License, the copyright notices, and the license notice saying this License applies to the Document are reproduced in all copies, and that you add no other conditions whatsoever to those of this License. You may not use technical measures to obstruct or control the reading or further copying of the copies you make or distribute. However, you may accept compensation in exchange for copies. If you distribute a large enough number of copies you must also follow the conditions in section 3.

You may also lend copies, under the same conditions stated above, and you may publicly display copies.

3\. COPYING IN QUANTITY

If you publish printed copies (or copies in media that commonly have printed covers) of the Document, numbering more than 100, and the Document's license notice requires Cover Texts, you must enclose the copies in covers that carry, clearly and legibly, all these Cover Texts: Front-Cover Texts on the front cover, and Back-Cover Texts on the back cover. Both covers must also clearly and legibly identify you as the publisher of these copies. The front cover must present the full title with all words of the title equally prominent and visible. You may add other material on the covers in addition. Copying with changes limited to the covers, as long as they preserve the title of the Document and satisfy these conditions, can be treated as verbatim copying in other respects.

If the required texts for either cover are too voluminous to fit legibly, you should put the first ones listed (as many as fit reasonably) on the actual cover, and continue the rest onto adjacent pages.

If you publish or distribute Opaque copies of the Document numbering more than 100, you must either include a machine-readable Transparent copy along with each Opaque copy, or state in or with each Opaque copy a computer-network location from which the general network-using public has access to download using public-standard network protocols a complete Transparent copy of the Document, free of added material. If you use the latter option, you must take reasonably prudent steps, when you begin distribution of Opaque copies in quantity, to ensure that this Transparent copy will remain thus accessible at the stated location until at least one year after the last time you distribute an Opaque copy (directly or through your agents or retailers) of that edition to the public.

It is requested, but not required, that you contact the authors of the Document well before redistributing any large number of copies, to give them a chance to provide you with an updated version of the Document.

4\. MODIFICATIONS

You may copy and distribute a Modified Version of the Document under the conditions of sections 2 and 3 above, provided that you release the Modified Version under precisely this License, with the Modified Version filling the role of the Document, thus licensing distribution and modification of the Modified Version to whoever possesses a copy of it. In addition, you must do these things in the Modified Version:

A. Use in the Title Page (and on the covers, if any) a title distinct from that of the Document, and from those of previous versions (which should, if there were any, be listed in the History section of the Document). You may use the same title as a previous version if the original publisher of that version gives permission.

B. List on the Title Page, as authors, one or more persons or entities responsible for authorship of the modifications in the Modified Version, together with at least five of the principal authors of the Document (all of its principal authors, if it has fewer than five), unless they release you from this requirement.

C. State on the Title page the name of the publisher of the Modified Version, as the publisher.

D. Preserve all the copyright notices of the Document.

E. Add an appropriate copyright notice for your modifications adjacent to the other copyright notices.

F. Include, immediately after the copyright notices, a license notice giving the public permission to use the Modified Version under the terms of this License, in the form shown in the Addendum below.

G. Preserve in that license notice the full lists of Invariant Sections and required Cover Texts given in the Document's license notice.

H. Include an unaltered copy of this License.

I. Preserve the section Entitled "History", Preserve its Title, and add to it an item stating at least the title, year, new authors, and publisher of the Modified Version as given on the Title Page. If there is no section Entitled "History" in the Document, create one stating the title, year, authors, and publisher of the Document as given on its Title Page, then add an item describing the Modified Version as stated in the previous sentence.

J. Preserve the network location, if any, given in the Document for public access to a Transparent copy of the Document, and likewise the network locations given in the Document for previous versions it was based on. These may be placed in the "History" section. You may omit a network location for a work that was published at least four years before the Document itself, or if the original publisher of the version it refers to gives permission.

K. For any section Entitled "Acknowledgements" or "Dedications", Preserve the Title of the section, and preserve in the section all the substance and tone of each of the contributor acknowledgements and/or dedications given therein.

L. Preserve all the Invariant Sections of the Document, unaltered in their text and in their titles. Section numbers or the equivalent are not considered part of the section titles.

M. Delete any section Entitled "Endorsements". Such a section may not be included in the Modified Version.

N. Do not retitle any existing section to be Entitled "Endorsements" or to conflict in title with any Invariant Section.

O. Preserve any Warranty Disclaimers.
If the Modified Version includes new front-matter sections or appendices that qualify as Secondary Sections and contain no material copied from the Document, you may at your option designate some or all of these sections as invariant. To do this, add their titles to the list of Invariant Sections in the Modified Version's license notice. These titles must be distinct from any other section titles.

You may add a section Entitled "Endorsements", provided it contains nothing but endorsements of your Modified Version by various parties—for example, statements of peer review or that the text has been approved by an organization as the authoritative definition of a standard.

You may add a passage of up to five words as a Front-Cover Text, and a passage of up to 25 words as a Back-Cover Text, to the end of the list of Cover Texts in the Modified Version. Only one passage of Front-Cover Text and one of Back-Cover Text may be added by (or through arrangements made by) any one entity. If the Document already includes a cover text for the same cover, previously added by you or by arrangement made by the same entity you are acting on behalf of, you may not add another; but you may replace the old one, on explicit permission from the previous publisher that added the old one.

The author(s) and publisher(s) of the Document do not by this License give permission to use their names for publicity for or to assert or imply endorsement of any Modified Version.

5\. COMBINING DOCUMENTS

You may combine the Document with other documents released under this License, under the terms defined in section 4 above for modified versions, provided that you include in the combination all of the Invariant Sections of all of the original documents, unmodified, and list them all as Invariant Sections of your combined work in its license notice, and that you preserve all their Warranty Disclaimers.

The combined work need only contain one copy of this License, and multiple identical Invariant Sections may be replaced with a single copy. If there are multiple Invariant Sections with the same name but different contents, make the title of each such section unique by adding at the end of it, in parentheses, the name of the original author or publisher of that section if known, or else a unique number. Make the same adjustment to the section titles in the list of Invariant Sections in the license notice of the combined work.

In the combination, you must combine any sections Entitled "History" in the various original documents, forming one section Entitled "History"; likewise combine any sections Entitled "Acknowledgements", and any sections Entitled "Dedications". You must delete all sections Entitled "Endorsements".

6\. COLLECTIONS OF DOCUMENTS

You may make a collection consisting of the Document and other documents released under this License, and replace the individual copies of this License in the various documents with a single copy that is included in the collection, provided that you follow the rules of this License for verbatim copying of each of the documents in all other respects.

You may extract a single document from such a collection, and distribute it individually under this License, provided you insert a copy of this License into the extracted document, and follow this License in all other respects regarding verbatim copying of that document.

7\. AGGREGATION WITH INDEPENDENT WORKS

A compilation of the Document or its derivatives with other separate and independent documents or works, in or on a volume of a storage or distribution medium, is called an "aggregate" if the copyright resulting from the compilation is not used to limit the legal rights of the compilation's users beyond what the individual works permit. When the Document is included in an aggregate, this License does not apply to the other works in the aggregate which are not themselves derivative works of the Document.

If the Cover Text requirement of section 3 is applicable to these copies of the Document, then if the Document is less than one half of the entire aggregate, the Document's Cover Texts may be placed on covers that bracket the Document within the aggregate, or the electronic equivalent of covers if the Document is in electronic form. Otherwise they must appear on printed covers that bracket the whole aggregate.

8\. TRANSLATION

Translation is considered a kind of modification, so you may distribute translations of the Document under the terms of section 4. Replacing Invariant Sections with translations requires special permission from their copyright holders, but you may include translations of some or all Invariant Sections in addition to the original versions of these Invariant Sections. You may include a translation of this License, and all the license notices in the Document, and any Warranty Disclaimers, provided that you also include the original English version of this License and the original versions of those notices and disclaimers. In case of a disagreement between the translation and the original version of this License or a notice or disclaimer, the original version will prevail.

If a section in the Document is Entitled "Acknowledgements", "Dedications", or "History", the requirement (section 4) to Preserve its Title (section 1) will typically require changing the actual title.

9\. TERMINATION

You may not copy, modify, sublicense, or distribute the Document except as expressly provided under this License. Any attempt otherwise to copy, modify, sublicense, or distribute it is void, and will automatically terminate your rights under this License.

However, if you cease all violation of this License, then your license from a particular copyright holder is reinstated (a) provisionally, unless and until the copyright holder explicitly and finally terminates your license, and (b) permanently, if the copyright holder fails to notify you of the violation by some reasonable means prior to 60 days after the cessation.

Moreover, your license from a particular copyright holder is reinstated permanently if the copyright holder notifies you of the violation by some reasonable means, this is the first time you have received notice of violation of this License (for any work) from that copyright holder, and you cure the violation prior to 30 days after your receipt of the notice.

Termination of your rights under this section does not terminate the licenses of parties who have received copies or rights from you under this License. If your rights have been terminated and not permanently reinstated, receipt of a copy of some or all of the same material does not give you any rights to use it.

10\. FUTURE REVISIONS OF THIS LICENSE

The Free Software Foundation may publish new, revised versions of the GNU Free Documentation License from time to time. Such new versions will be similar in spirit to the present version, but may differ in detail to address new problems or concerns. See [https://www.gnu.org/licenses/](https://www.gnu.org/licenses/).

Each version of the License is given a distinguishing version number. If the Document specifies that a particular numbered version of this License "or any later version" applies to it, you have the option of following the terms and conditions either of that specified version or of any later version that has been published (not as a draft) by the Free Software Foundation. If the Document does not specify a version number of this License, you may choose any version ever published (not as a draft) by the Free Software Foundation. If the Document specifies that a proxy can decide which future versions of this License can be used, that proxy's public statement of acceptance of a version permanently authorizes you to choose that version for the Document.

11\. RELICENSING

"Massive Multiauthor Collaboration Site" (or "MMC Site") means any World Wide Web server that publishes copyrightable works and also provides prominent facilities for anybody to edit those works. A public wiki that anybody can edit is an example of such a server. A "Massive Multiauthor Collaboration" (or "MMC") contained in the site means any set of copyrightable works thus published on the MMC site.

"CC-BY-SA" means the Creative Commons Attribution-Share Alike 3.0 license published by Creative Commons Corporation, a not-for-profit corporation with a principal place of business in San Francisco, California, as well as future copyleft versions of that license published by that same organization.

"Incorporate" means to publish or republish a Document, in whole or in part, as part of another Document.

An MMC is "eligible for relicensing" if it is licensed under this License, and if all works that were first published under this License somewhere other than this MMC, and subsequently incorporated in whole or in part into the MMC, (1) had no cover texts or invariant sections, and (2) were thus incorporated prior to November 1, 2008.

The operator of an MMC Site may republish an MMC contained in the site under CC-BY-SA on the same site at any time before August 1, 2009, provided the MMC is eligible for relicensing.

ADDENDUM: How to use this License for your documents

To use this License in a document you have written, include a copy of the License in the document and put the following copyright and license notices just after the title page:

Copyright (C)  YEAR  YOUR NAME.
Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License, Version 1.3 or any later version published by the Free Software Foundation; with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
A copy of the license is included in the section entitled "GNU Free Documentation License".

If you have Invariant Sections, Front-Cover Texts and Back-Cover Texts, replace the "with … Texts." line with this:

with the Invariant Sections being LIST THEIR TITLES, with the Front-Cover Texts being LIST, and with the Back-Cover Texts being LIST.
If you have Invariant Sections without Cover Texts, or some other combination of the three, merge those two alternatives to suit the situation.

If your document contains nontrivial examples of program code, we recommend releasing these examples in parallel under your choice of free software license, such as the GNU General Public License, to permit their use in free software.
