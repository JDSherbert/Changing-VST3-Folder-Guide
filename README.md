![image](https://github.com/JDSherbert/Changing-VST3-Folder-Guide/assets/43964243/6b2e5e61-2630-4cc1-9f3f-23185c94ab32)

# Guide: Changing The Default VST3 Folder Location

<!-- Header Start -->
<a href = "https://juce.com/"> <img height="40" img width="40" src="https://cdn.simpleicons.org/juce/white"> </a> 
<img align="right" alt="stars badge" src="https://img.shields.io/github/stars/jdsherbert/JDSherbert-Repo-Template"/>
<img align="right" alt="forks badge" src="https://img.shields.io/github/forks/jdsherbert/JDSherbert-Repo-Template?label=Fork"/>
<img align="right" alt="Visitors" src="https://visitor-badge.glitch.me/badge?page_id=github.com/jdsherbert/JDSherbert-Repo-Template"/>
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
  <img align="left" alt="Windows" src="https://img.shields.io/badge/Windows-black?style=for-the-badge&logo=windows&logoColor=white&color=#0078D6&labelColor=#0078D6"> </a>

-----------------------------------------------------------------------

