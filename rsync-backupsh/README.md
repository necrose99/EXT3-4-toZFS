I snagged this to aid in Dumping drive to Drive and I can tweak to call the fuctions in other scripts by minor 
refactoring of code to call as fuctions in other scripts but hear it is in this one untouced. 
__do fucntion_ etc or so I can wildcard the some of the paths to my needs in a working copy.

Makrdown converted page below.
=========================================================================================================================
Creating an rsync backup script
===============================

<nav class="treeBranch">[Bobulous Central][] → [Miscellaneous pages][] → An rsync backup script.</nav>

Why use rsync for backup?
-------------------------

<script type="text/javascript"><!--
google_ad_client = "ca-pub-6536468970450249";
/* Misc top-of-page embedded */
google_ad_slot = "9245723422";
google_ad_width = 300;
google_ad_height = 250;
//-->
</script>
<script type="text/javascript" src="http://pagead2.googlesyndication.com/pagead/show_ads.js">
</script>

It’s important to backup your important computer files to avoid losing them if your PC fails. But if you have gigabytes of data you want to keep safe, simply copying all of your files from one place to another will likely take hours.

Luckily Linux offers a command-line tool called rsync which only copies a file to a backup location if the file is new or has changed since the last backup. This selective copying usually means an rsync backup takes a fraction of the time taken by a simple “copy all” backup.

Seeing as you ought to backup your system frequently, it makes sense to create a backup script which runs customised rsync commands to backup all of the files you want to keep, but none of those you don’t. This page is all about creating a <abbr title="GNU Bourne-Again SHell">Bash</abbr> script which runs an rsync backup. I’m using Kubuntu 14.10, but the advice on this page should apply to users of other Linux distributions (though you may need to vary some steps, so check carefully for any incompatible commands, options, etc).

**Important note**: this page is intended to help people discover how useful rsync can be. You follow the advice on this page at your own risk, so make sure you understand the consequences of any commands or actions you intend to take. Read the <abbr title="manual">man</abbr> pages for any commands or flags with which you’re not familiar.

Before you backup
-----------------

<figure class="captionedImage">
[![screenshot: The ring chart in Disk Usage Analyser.][]][]

<figcaption>
Disk Usage Analyser showing that my photo collection is the biggest use of disk space.

</figcaption>
</figure>
The first step is decidin

  [Bobulous Central]: ../index.html
  [Miscellaneous pages]: index.html
  [screenshot: The ring chart in Disk Usage Analyser.]: images/disk-usage-analyser_thumb.png "Disk Usage Analyser ring chart"
  [![screenshot: The ring chart in Disk Usage Analyser.][]]: images/disk-usage-analyser.png
