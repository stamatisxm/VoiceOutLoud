# VoiceOutLoud
A Light Tcl/Tk Text To Speech GUI

<img alt="RoughPad Logo" src="http://istos.info/images/VoiceOutLoud.png" width="48px" height="48px" />

## VoiceOutLoud - { Text - To - Speech - GUI }
VoiceOutLoud is a Tcl/Tk application that uses spd-say to send the text pasted in its text area to the speech-dispatcher which synthesizes it into speech. The parameters for the voice, speed, pitch and volume are fully customizable and the program is currently available in two languages, English and Greek.

### { Program Options }
#### As per the settings of spd-say:
- Voice has the following choices:
  - Male1
  - Male2
  - Male3
  - Female1
  - Female2
  - Female3
  - Child(Male)
  - Child(Female)
- Pitch takes values from -100 to 100.
- Rate takes values from -100 to 100.
- Volume can go from -100 to 100.

The "drop-down menu" on the right hand side, changes the text on the program controls and the spd-say language setting.

The Clear button clears the text from the text area without affecting any ongoing playback.

The controls:

- Play
- Pause
- Resume
- Stop
- Exit

function as in any other audio player.

### { Program Setup }
This program is going to be installed by default in your **$HOME/bin** directory. If you have not set your **$HOME/bin** in the **$PATH**, see this [Knowledge Base Snippet](http://istos.info/knowledgebase/knowledgebasesnippet.php?id=15 "Setup your $HOME/bin in the $PATH") for details.

To run this program, you need to have the following packages installed in your system (Check with your package manager):
- _**tcl**_
- _**tk**_
- _**tklib**_
- _**speech-dispatcher**_ (includes _**spd-say**_)
- Either _**tcl-signal**_ or _**tclx**_ (or both)

**\* Arch** and derivative distributions (**ArchBang**, **Manjaro**, etc) may require the package _**speech-to-text-text-to-speech**_ in order for _spd-say_ to interact properly with _speech-dispatcher_ [Many thanks to our affiliate **Debicarus** for pointing this out!]

#### Once the above packages are installed
- Download your preferred variant (**_VoiceOutLoud-tclx_** or _**VoiceOutLoud-tcl-signal**_)
- Move the downloaded tarball into your **$HOME**, as all extracted files and directories will be relative to your **$HOME**
- Expand the tar file in a terminal by issuing:  
<code>**tar xf VoiceOutLoud\_&lt;variant&gt;_&lt;version&gt;.tar**</code>
- Invoke the program from the terminal, running:  
<code>**VoiceOutLoud &**</code>  
to ensure that it loads properly and no error messages are shown.

If everything has gone ok, you should be able to find the program in the _**Accessories**_ program group on your desktop manager.

### { File List }
The tarball contains these files (relative to the user's $HOME):
<pre>
bin/VoiceOutLoud
.icons/VoiceOutLoud-mask.xbm
.icons/VoiceOutLoud.png
.icons/VoiceOutLoud.xbm
.icons/VoiceOutLoud.xpm
.local/share/applications/VoiceOutLoud.desktop
</pre>

### { Note }
There are two variants of the program to download, one is set to work with _**tcl-signal**_ and the other with _**tclx**_. Choose the variant you want to download depending on which of the above package (_tcl-signal_ or _tclx_) you already have (or are planning to install) on your system. The only differences in code in the two variants are as follows:

#### tcl-signal variant:
**#package require Tclx**  
**package require Signal**  

#### tclx variant:
**package require Tclx**  
**#package require Signal**