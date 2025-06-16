# Installation Guide for Hidemium4 on macOS

1. Download the latest version of Hidemium4 for Mac

<figure><img src="https://docs.hidemium.io/~gitbook/image?url=https%3A%2F%2F699023340-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FiEhmc20xmuwcG5ThYMWS%252Fuploads%252FaAV2XZrado0I2UzoiswJ%252Fimage.png%3Falt%3Dmedia%26token%3D2113c215-0484-4461-88c9-b1e2572a6b82&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=8ffb0e5e&#x26;sv=1" alt=""><figcaption></figcaption></figure>

**2. Install the app**

B1: After downloading successfully, open the .dmg file

B2: Open the .dmg file and drag the Hidemium4 icon into the ‘Applications’ folder.

<figure><img src="https://docs.hidemium.io/~gitbook/image?url=https%3A%2F%2F699023340-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FiEhmc20xmuwcG5ThYMWS%252Fuploads%252FctNkmyb0IXmjhZkFjrYt%252Fimage.png%3Falt%3Dmedia%26token%3D96d04977-f29f-4ed9-bc28-d748b9b63af3&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=466e06e5&#x26;sv=1" alt=""><figcaption></figcaption></figure>



**Note:** After dragging the Hidemium4 icon into the “**Applications**” folder, if this popup appears, click “**Replace**”. If the computer has never had Hidemium installed before, or if it has been uninstalled, this popup will not appear.

![](http://education.hidemium.io/wp-content/uploads/2024/08/Screenshot_1-1.png)

B3: After completing step 2, don’t rush to open the app. Open Terminal, copy and paste the following command into **Terminal**, and press **Enter**:

```
xattr -cr /Applications/Hidemium4.app
```

<figure><img src="http://education.hidemium.io/wp-content/uploads/2024/08/Screenshot_2.png" alt=""><figcaption></figcaption></figure>



**Note:** For devices that have never installed Hidemium 4 before, you only need to run the command `xattr -cr /Applications/Hidemium4.app` to open and use the app. However, for machines that have previously installed the Hidemium 4 app, you will need to run the additional command below.Then you run the following command:**Note: You need to replace&#x20;**_**ten\_may**_**&#x20;with your computer’s name.**

chmod -R +x /Users/ten\_may/.hidemium\_4

&#x20;

![](http://education.hidemium.io/wp-content/uploads/2024/08/Screenshot_1.png)

&#x20;

B4: After that, you can open the Hidemium4 app and use it normally.

<figure><img src="https://docs.hidemium.io/~gitbook/image?url=https%3A%2F%2F699023340-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FiEhmc20xmuwcG5ThYMWS%252Fuploads%252FdI3nk7vJ9BvSqas8oYpC%252Fimage.png%3Falt%3Dmedia%26token%3Df67835ce-f796-49a9-806c-ebf6212ef03c&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=87bfd668&#x26;sv=1" alt=""><figcaption></figcaption></figure>
