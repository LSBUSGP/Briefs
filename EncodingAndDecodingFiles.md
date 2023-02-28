# Encoding and Decoding Files

A popular console platform requires its cloud stored save files to be uploaded as base64 encoded binary CDATA sections inside an XML file.

The format of the file should look like this:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<Cloud>
  <User>
    <Account an="player_account@email.com" />
    <Title id="12345678" />
  </User>
  <Data>
    <Folders>
      <Folder name="Settings">
        <Files>
          <File name="settings.bin">
<![CDATA[
AAECAwQFBgcICQoLDA0ODxAREhMUFRYXGBkaGxwdHh8gISIjJCUmJygpKissLS4vMDEyMzQ1Njc4
OTo7PD0+P0BBQkNERUZHSElKS0xNTk9QUVJTVFVWV1hZWltcXV5fYGFiY2RlZmdoaWprbG1ub3Bx
cnN0dXZ3eHl6e3x9fn+AgYKDhIWGh4iJiouMjY6PkJGSk5SVlpeYmZqbnJ2en6ChoqOkpaanqKmq
q6ytrq+wsbKztLW2t7i5uru8vb6/wMHCw8TFxsfIycrLzM3Oz9DR0tPU1dbX2Nna29zd3t/g4eLj
5OXm5+jp6uvs7e7v8PHy8/T19vf4+fr7/P3+/w==
]]>
          </File>
          <! additional files can go here >
        </Files>
      </Folder>
      <! additional folders can go here >
    </Folders>
  </Data>
</Cloud>
```

The layout of the files in the folders is as follows:
```
SaveData
-> Settings
-> -> settings.bin
-> Saves
-> -> save1.bin
-> -> save2.bin
-> -> etc ...
```
There can be any number of folders or files, but the folders are only ever one level deep and the files must be in one of the folders.

A Unity editor extension is required to create an XML file from a folder of files, or create the folders and files from XML as specified above.

You must include the following in your Unity package:

1. scripts containing the Unity editor extensions
2. a set of sample files to turn into XML and vice versa
3. documentation on how to use these extensions

## Extra credit

Ensure that the XML output file is tabulated and that the base64 CDATA sections are fixed width limited to 65 characters.