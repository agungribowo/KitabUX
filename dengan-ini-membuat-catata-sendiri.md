---
description: Berisi Artikel Tutorial Sehari Hari
---

# Artikel Mac



{% tabs %}
{% tab title="How to Split Zip Files in OS X" %}
A ZIP file bundles and, if possible, compresses multiple other files into a convenient and smaller package. However, the ZIP file may still be quite large and cumbersome to transport over the Internet. Split a large ZIP file into multiple parts to allow it to be more easily transported to customers or business partners over the Internet via email or a file-sharing service. You can do this from the terminal window of your OS X Macintosh.

### Existing Zip File

1. Open the Terminal application located in the Applications/Utilities folder or under the Other app group in Launchpad.

2. Navigate to the folder where the ZIP file you wish to split is located. Use the cd \(change directory\) command to change folders. For example, enter "cd Documents" to change to the Documents folder from your home folder. Enter "cd My\ Folder" to change to a folder with a space in the name; the backslash escapes the space character and prevent it from being interpreted as the start of a new command. Enter "cd .." to return to the previous folder. Enter the pwd \(present working directory\) command to check your current directory.

3. Enter the following command into the command line and press "Enter" to execute it. The command takes an input ZIP file and splits it into 100MB segments. The segments are titled in the form SplitArchive.zip, SplitArchive.z01, SplitArchive.z02 and so on.

zip MyArchive.zip --out SplitArchive.zip -s 100m



### New Zip File

1. 

Create a new folder in Finder by selecting "New Folder" from the "File" menu or pressing "Command-Shift-N."2. 

Move the files you wish to archive into a ZIP file into this folder.3. 

Open the Terminal application.4. 

Navigate to the parent folder containing the folder with the files you wish to zip. For example, if you created a folder named "Q2Results" to archive in your Documents folder, you need to navigate to the Documents folder.5. 

Enter the following command into the command line and click "Enter." The command archives the folder Q2Results into Q2Results.zip in 50MB segments titled Q2Results.zip, Q2Results.z01, Q2Results.z02 and so on.

zip Q2Results --out Q2Results.zip -s 50m

**Warnings**

* Multipart ZIP archives require all parts to open correctly.
* If a file is already in a compressed format, it's possible that creating a ZIP from it would not further compress it.
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}



