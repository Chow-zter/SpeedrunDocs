speedrunDocs
============

Your speedrun notes next to LiveSplit, in one window. Show two documents side
by side, and let your splits turn the pages for you.

Start it by double-clicking speedrunDocs.exe.
It needs the .NET 8 Desktop Runtime and the Microsoft Edge WebView2 Runtime.


ADDING DOCUMENTS
----------------
Each side holds one document:

  - Paste a Google Docs, Google Sheets or ChatGPT share link and press Enter.
  - Or press "Import file..." to open a downloaded file:
    docx, doc, odt, rtf, pdf, xlsx, ods, txt, md, html, csv, json, epub,
    or Google's web-page zip.

Imported files are read-only copies kept by the program, so you can delete the
download afterwards. They are shown one page at a time.

Press "Sign in" on either side to use your Google account. You only do this
once, and both sides use it. Click a side's heading to rename it.


TURNING PAGES
-------------
  Numpad1      next page on the left side
  Numpad2      next page on the right side

The keys work from any program, including during a game. Num Lock must be on.
While the program is open, those keys won't type numbers anywhere else.
To use different keys, click "Key:" on a side and press the new key.
The < and > buttons on a side also turn pages on imported files.


FOLLOWING YOUR SPLITS
---------------------
Works the same with manual splits and auto-splitters. It uses a small local
file only: no server and no network.

One-time setup, for each LiveSplit layout you use:
  1. Right-click LiveSplit and choose Edit Layout.
  2. Press +, then Other, then Side Docs Link, then OK.
  3. Right-click LiveSplit and choose Save Layout.

Choosing pages:
  1. Press "Splits..." in the top bar.
  2. For each split, type the pages for each side, like 1-3 or 4,5,9.
     You can also flip to a page and press "Add current".
     Leave a box empty to keep the pages from the split before.
  3. Close that window and tick "Attach to LiveSplit".

Each split then jumps to the first of its pages, and the page keys loop through
only that split's pages. Example: Tricky Devil on 1-3 and Gryphons on 4-6.
Untick it and splits move nothing, and the keys go through the whole document.

Page numbers for splits work on imported files and Google Docs, not on Sheets
or ChatGPT pages.


OTHER OPTIONS (TOP BAR AND SIDE HEADERS)
----------------------------------------
  Profiles             Type a name and press "Save profile" to keep the current
                       pair of documents and their split pages. Click the name
                       to bring them back.
  Dark docs            Shows the documents themselves in dark colours.
  Show LiveSplit here  Holds the LiveSplit window at the side of this one. It
                       moves and minimises with this window, and is opened for
                       you if it isn't running. The button next to the tick
                       switches between left and right.
  Remove side          Gives the other document the whole window and frees that
                       side's key. "Add side" brings it back.
  Divider              Drag the line between the documents to resize them.


FILES
-----
  speedrunDocs.exe     The whole program.
  SpeedrunDocs.dll     This goes into Livesplits components folder.

LiveSplit uses its own copy at LiveSplit\Program\Components\SpeedrunDocs.dll
That file must keep that name. If you ever need to restore it from the spare,
close LiveSplit first and rename the copy back to SideDocsLink.dll.

Your sign-in, profiles and imported documents are stored separately in
%LOCALAPPDATA%\SideDocs, so moving the program doesn't lose them.


IF SOMETHING ISN'T WORKING
--------------------------
Splits don't move the pages:
  - Check that "Attach to LiveSplit" is ticked.
  - Check that Side Docs Link is in the layout you are using, and that the
    layout was saved.
  - If "Splits..." shows no splits, LiveSplit isn't connected yet.
  - Any component errors are written to %LOCALAPPDATA%\SideDocs\link-errors.txt.

A key shows "(taken)":
  Another program is already using that key. Choose a different one.
