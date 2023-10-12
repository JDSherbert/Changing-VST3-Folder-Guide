![image](https://github.com/JDSherbert/Changing-VST3-Folder-Guide/assets/43964243/6b2e5e61-2630-4cc1-9f3f-23185c94ab32)

# Guide: Changing The Default VST3 Folder Location

<!-- Header Start -->
<a href = "https://juce.com/"> <img height="40" img width="40" src="https://cdn.simpleicons.org/juce/white"> </a> 
<img align="right" alt="Stars Badge" src="https://img.shields.io/github/stars/jdsherbert/Changing-VST3-Folder-Guide?label=%E2%AD%90"/>
<img align="right" alt="Forks Badge" src="https://img.shields.io/github/forks/jdsherbert/Changing-VST3-Folder-Guide?label=%F0%9F%8D%B4"/>
<img align="right" alt="Watchers Badge" src="https://img.shields.io/github/watchers/jdsherbert/Changing-VST3-Folder-Guide?label=%F0%9F%91%81%EF%B8%8F"/>
<img align="right" alt="Issues Badge" src="https://img.shields.io/github/issues/jdsherbert/Changing-VST3-Folder-Guide?label=%E2%9A%A0%EF%B8%8F"/>
<img align="right" src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FJDSherbert%2FChanging-VST3-Folder-Guide%2Fhit-counter%2FREADME&count_bg=%2379C83D&title_bg=%23555555&labelColor=0E1128&title=🔍&style=for-the-badge">
<!-- Header End --> 

-----------------------------------------------------------------------

<a href="https://juce.com/"> 
  <img align="left" alt="JUCE Plugin Guide" src="https://img.shields.io/badge/VST%20Plugin%20Guide-black?style=for-the-badge&logo=juce&logoColor=white&color=black&labelColor=black"> </a>
  
<br></br>

-----------------------------------------------------------------------
## Overview
If you are a person who uses DAW to compose music often, you may have come across VST3 plugins. VST3 plugins are awesome, but there are a few issues with them.
The recurring message is this:
> You can’t change the default VST3 folder. It MUST be placed there. This was set by Steinberg, the licensor of the VST format. This has to do with Steinberg’s own DAWs like Nuendo/Cubase and their internal plugin manager, which uses this system folder for installed VST3 plugins. This also has to do with the VST3 preset standard, which is able to save presets with different categories. All DAWs on the marked which support VST3 are forced to search new VST3 plugins in `C:\Program Files\Common Files\VST3`

This would be fine, except I don't like being told "No".

Instead, there are a few ways to "trick" the DAW into searching oher folders for your VST3 plugins. If you're a Reaper user, then cool, you can ignore this as Reaper doesn't care and will blindly search recursively for any VST format. For the rest of us, this little trick should work on FL Studio and Renoise.

-----------------------------------------------------------------------

<a href="https://www.microsoft.com"> 
  <img align="left" alt="Windows" src="https://img.shields.io/badge/Windows%20x86-black?style=for-the-badge&logo=windows&logoColor=white&color=0078D6&labelColor=0078D6"> </a>

<a href="https://www.microsoft.com"> 
  <img align="left" alt="Windows" src="https://img.shields.io/badge/Windows%20x64-black?style=for-the-badge&logo=windows&logoColor=white&color=0078D6&labelColor=0078D6"> </a>

<a href="https://juce.com/"> 
  <img align="left" alt="JUCE Plugin Guide" src="https://img.shields.io/badge/VST%20Plugin%20Guide-black?style=for-the-badge&logo=juce&logoColor=white&color=black&labelColor=black"> </a>

<br></br>

-----------------------------------------------------------------------

### Guide: Changing The Default VST3 Folder On Windows OS

On Windows, you can change the default folder for VST3 Plugins by using Symbolic Links.
To do so, follow this guide.

Firstly, open up Command Prompt by typing cmd into the search bar.

![image](https://github.com/JDSherbert/Changing-VST3-Folder-Guide/assets/43964243/d9f03c6b-8452-4dc2-9422-8f2ae7745fd0)
![image](https://github.com/JDSherbert/Changing-VST3-Folder-Guide/assets/43964243/36270010-724d-45b0-8f32-6591c80abb1f)

Next, right click Command Prompt and select "Run as Administrator". You'll need to do this as you'll be making changes to the C:\ drive, which is usually the OS drive. Windows has special protection and required permissions for this drive.

![image](https://github.com/JDSherbert/Changing-VST3-Folder-Guide/assets/43964243/e104a07b-333d-42cd-a5b8-364b271bda9f)

Next, open File Explorer and navigate to this path: `C:\Program Files\Common Files`

**If it doesn't exist yet, or you deleted it when you moved the plugins, you'll need to recreate this path. Make sure to delete the VST3 folder here as we'll be replacing it with a symbolic link! Make sure the new folder you wish to path to exists as well!**


![image](https://github.com/JDSherbert/Changing-VST3-Folder-Guide/assets/43964243/7cefb9fd-e0db-459e-8076-f8fb094aa003)

Now, in the Command Prompt, type the following command to create a symbolic link (Junction):

`mklink /J "C:\Program Files\Common Files\VST3" "D:\Your\New\VST3\Path"`

![image](https://github.com/JDSherbert/Changing-VST3-Folder-Guide/assets/43964243/e13db923-6af8-43be-8896-372955c5e4cb)
![image](https://github.com/JDSherbert/Changing-VST3-Folder-Guide/assets/43964243/8c5d0ac9-1906-4e7b-afbf-a79bff91a3ff)

And that's pretty much it - if you did it correctly, you should get this message!
Now you should be able to re-scan for plugins in your DAW and it will now pick up your VST3 plugins, without them needing to be in the default folder!

![image](https://github.com/JDSherbert/Changing-VST3-Folder-Guide/assets/43964243/f40a2084-db75-4b7a-b9ff-16491a7b956f)

If this helped you, give this repository a star and share with others!
