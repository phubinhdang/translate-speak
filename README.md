<h2 >Translate Speak</h2>
A mini application works as a speakable translator for Linux(Ubuntu). It is quite helpful when you face a foreign word (or a short sentence). It can give you the meaning and the pronunciation of that word instantly without having to open browser or your dictionary app, no matter where that word is showing up (on browser, pdf reader, terminal,...)

<h2 >Usage</h2>

1. Select a word using single/double click or sentence.
2. Press your personal key shortcut. (see how to create it in [Installation](#Installation))

You will get a push notification showing the translated text, the speech of that word and that word will be stored in a text file named *searches.txt*


<h2 >Supported languages</h2>
Every language which is supported by Google Translate API (auto detect)

<h2 id="Installation">Installation</h2>
Linux (Ubuntu)

Create a text file names *searches.txt* to store your searched words

`touch ~/Documents/searches.txt`

`sudo apt-get install libnotify-bin wget xsel`

`git clone https://github.com/phubinhdang/translate-speak.git`

`cd translate-speak `

`gedit translate-speak` or `nano translate-speak`

A text editor should show up and you can change the following parameters as needed

 * For translation:

http://translate.googleapis.com/translate_a/single?client=gtx&sl=auto&tl=<span>*__de__*</span>&dt=t


After cloned this script will come with <span>*__de__*</span> (German) as target language, which you change as your demand, such as vi for Vietnamese or fr for French.

* For speech: 

http://translate.google.com/translate_tts?ie=UTF-8&client=tw-ob&q=$*&tl=<span>__*en*__</span>

You will get a speech in english (<span>*__en__*</span>) but you can change it base on your source language.

See this [link](https://cloud.google.com/translate/docs/languages) for language code.

You can obviously turn off the speech as needed by commenting out the code for the part *#get speech* in the file.

Make it executeable

`sudo chmod a+x translate-speak`

Copy it to /usr/bin

`cp translate-speak /usr/bin`



Finally, set your shortcut for this script: 

Go to keyboard -> add shortcut (symbol **+**) -> fill the fields as following: 

* Name : translate-speak
* Command : /usr/bin/translate-speak
* Shortcut : set what your want




<h2 >References</h2>

https://websetnet.net/translate-text-select-linux-desktop-keyboard-shortcut-notifications/
https://elinux.org/RPi_Text_to_Speech_(Speech_Synthesis)