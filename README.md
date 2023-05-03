Download Link: https://assignmentchef.com/product/solved-cs2261-lab0-gba-games
<br>
In this lab, you will be installing the software to write, compile, and run GBA games for this class. It is broken up into various parts. If any part does not produce the expected outcome, alert a TA and fix the problem before continuing.

<ul>

 <li><strong>Part One – Cygwin </strong></li>

</ul>

Ø Cygwin is what students running Windows will use as a C Compiler. This is the biggest difference between the Windows and Mac installations, since the Mac folk (usually) already have a C Compiler installed.

<ol>

 <li>Go to the project website, <u><a href="https://www.cygwin.com/">https://www.cygwin.com/</a></u></li>

 <li>If your computer is 64-bit, click on setup-x86_64.exe. Otherwise, click on setup-x86.exe.</li>

</ol>




<ol start="3">

 <li>Open the folder where it downloaded and run that file.</li>

 <li>On the first popup, click next. Then, select “Install from the Internet” and click next.</li>

 <li>Choose the directory where you want Cygwin to install. This must be somewhere that you will not move or delete until this class is over. <u>Make</u> <u>note of this location, because you will have to find it in a later step.</u> Then click next.</li>

 <li>This next part doesn’t matter. You can just accept the default and click next.</li>

 <li>Select “Use System Proxy Settings” and click next.</li>

 <li>Select the first mirror site in the list, the click next.</li>

 <li>This part is complicated, so pay close attention. In the search bar, type</li>

</ol>

“gcc-core”. Click the plus next to the category “All” and the category

“Devel” and find the package <u>titled exactly “gcc-core”</u>. Find the arrow to the right of the “Skip” for that package, and click it. Select the latest version that does not say “(test)” by it.




<ol start="10">

 <li>Back in the search bar, type “gcc-g++”. Find the package <u>titled exactly</u> <u>“gcc-g++”</u>. Find the arrow to the right of the “Skip” for that package, and click it. Select the latest version that does not say “(test)” by it.</li>

 <li>Again, in the search bar, type “gdb”. Find the package <u>titled exactly “gdb”</u>.</li>

</ol>

Find the arrow to the right of the “Skip” for that package, and click it. Select the latest version that does not say “(test)” by it.

<ol start="12">

 <li>One last time, in the search bar, type “make”. Find the package <u>titled</u> <u>exactly “make”</u>. Find the arrow to the right of the “Skip” for that package, and click it. Select the latest version that does not say “(test)” by it.</li>

 <li>Click next, then next again, then wait quite a while for everything to finish.</li>

</ol>




<ol start="14">

 <li>Uncheck the two boxes (or don’t; it’s your clutter, not mine) and then click finish.</li>

</ol>




<ol start="15">

 <li>The last thing we need to do is add Cygwin’s bin folder to our System path. Open Control Panel, then go to System and Security, then System, then Advanced System Settings.</li>

 <li>In the dialog, click “Environmental Variables”.</li>

 <li>In the new dialog, under System Variables (not User Variables), select “Path” and click “Edit”.</li>

</ol>




<ol start="18">

 <li>This new screen will depend on which version of Windows you are running.</li>

</ol>

<ul>

 <li>If it is an organized list of items (like in the picture below), click “New”, and in the blank that opens up, copy the exact path to where you installed Cygwin (the location I told you to remember earlier) and add “bin” to the end. Then press Enter.</li>

</ul>




<ul>

 <li>If it is a singular text box, move the cursor all the way to the end, type a semicolon, and then copy the exact path to where you installed Cygwin (the location I told you to remember earlier) and add “bin” to the end. If it has any spaces in it, surround the whole thing in quotes (not including the semicolon you added before).

  <ol start="19">

   <li>Press OK on all of the Control Panel dialogs you have opened thus far.</li>

   <li>Open Command Prompt.</li>

   <li>Type “gcc” and press enter. If what you see is something like the picture below, you installed Cygwin correctly. If not, alert a TA.</li>

  </ol></li>

</ul>




Ø Congrats! You have completed the hard part. You are free to delete all of the things associated with this part in your Downloads folder (unless of course you were crazy enough to install Cygwin there).

<strong> </strong>

<ul>

 <li><strong>Part Two – devkitARM </strong></li>

</ul>

Ø DevkitARM is your development kit for the Game Boy Advance, created by a group called devkitPro. Without it, we can compile C code, but not actually format the result for the Gameboy. So let’s fix that.

<ol>

 <li>Go to the project website, <u><a href="https://github.com/devkitPro/installer/releases">https://github.com/devkitPro/installer/releases</a></u></li>

</ol>




<ol start="2">

 <li>Click on “devkitProUpdater-3.0.3.exe” to download it.</li>

 <li>When the download finishes, open it, then hit Next.</li>

</ol>




<ol start="4">

 <li>Click “Download and install/ install from downloaded files” and hit Next.</li>

 <li>Select “Remove downloaded files” and hit Next.</li>

</ol>




<ol start="6">

 <li>During this step, deselect everything in the list <strong>except</strong> GBA, and hit Next.</li>

 <li>Select a destination folder somewhere that you will not move or delete until this class is over. The same folder where you put Cygwin will usually suffice. <u>Make note of this location, because you will have to find it in a</u> <u>later step.</u></li>

 <li>When asked to choose the Start Menu Folder, put whatever you want. The default is fine. Hit Next, wait for the install to finish (it will take a long time, and open a bunch of strange terminal windows, and look like it’s going to fail, but it won’t).</li>

</ol>

Ø That’s all you have to do for devkitARM. Easy, right?

<strong> </strong>

<ul>

 <li><strong>Part Three – VisualBoyAdvance-M </strong></li>

</ul>

Ø VisualBoyAdvance-M is your emulator. Since we can now compile and format our code, it would be useless if we couldn’t actually run it. So let’s fix that.

<ul>

 <li>Note: if you already have a GBA emulator that you are comfortable with, I still highly recommend you use this one for this class. It has some special features that will come in handy for debugging.

  <ol>

   <li>Downloading this from its website requires having 7-Zip installed, so I provided it to you in a .zip Extract this file.</li>

   <li>Find the folder it creates once unzipped, and move it somewhere that you will not move or delete until this class is over. The same folder where you put Cygwin and devkitARM will usually suffice. <u>Make note of this location,</u> <u>because you will have to find it in a later step.</u></li>

  </ol></li>

</ul>

Ø That’s all have to do for VisualBoyAdvance-M. Even easier.

<strong> </strong>

<ul>

 <li><strong>Part Four – Makefile </strong></li>

</ul>

Ø Now that we have installed everything, we need to set up the compilation process so that we don’t have to run 1,000 commands every time we want to compile our code. C uses Makefiles for this. I have provided one for you, but it needs to know where to find the things you just installed.

<ol>

 <li>In the provided Sample Project, find Makefile and open with a text editor (like Notepad or Sublime Text). Near the beginning, you will see three lines that end in “=”.</li>

 <li>After the “=” next to “CCPATH”, type the exact path to the cygwin (or cygwin64) folder, and add “bin” to the end. If there are any spaces in the path, surround it in quotes.</li>

 <li>After the “=” next to “DKPATH”, type the exact path to the devkitPro folder (you don’t need to add anything to the end for this one). If there are any spaces in the path, surround it in quotes.</li>

 <li>After the “=” next to “VBASIM”, type the exact path to the vbam-2.0.1 folder, add “bin” to the end, then add “visualboyadvance-m.exe”. If there are any spaces in the path, surround it in quotes.</li>

 <li>Make sure the result looks something like the following picture.</li>

</ol>




<ol start="6">

 <li>Save and close the file.</li>

</ol>

Ø Congrats. We now officially have everything it takes to simply compile, format, and run GBA games. Now let’s make it simpler.

<ul>

 <li><strong>Part Five – Sublime Text </strong></li>

</ul>

Ø We can make the process even more streamlined by incorporating the compilation process into our text editor.  For this class, we highly encourage Sublime Text. <u>Even if you have Sublime Text installed, do not</u> <u>skip these steps.</u>

<ol>

 <li>If you don’t have Sublime Text installed, download it from the project website, <u><a href="https://www.sublimetext.com/3">https://www.sublimetext.com/3</a></u><a href="https://www.sublimetext.com/3">.</a> I don’t need to walk you through this installation process; it’s user-friendly enough.</li>

 <li>Once you have Sublime Text installed, open it, then go to Tools, then Build System, then click “New Build System…”</li>

 <li>It will open a new file. Delete everything in it, then paste in everything from the provided txt.</li>

</ol>




<ol start="4">

 <li>Save it in the folder it suggests when you hit save, and title it</li>

</ol>

“GBA.sublime-build”.

<ol start="5">

 <li>Close everything in Sublime Text, and then close Sublime Text.</li>

 <li>Reopen Sublime Text, then use it to open Makefile in the Sample Project folder.</li>

 <li>Go to Tools, then Build System, and make sure GBA is selected.</li>

 <li>Go to Tools, then Build With, then select Run.</li>

</ol>




After completing all of these steps, you should see output in the console at the bottom of Sublime Text that looks something like the following picture.




You should also see a GBA game running that looks something like the following picture.




If so, you are done with the lab. If not, there is an issue somewhere