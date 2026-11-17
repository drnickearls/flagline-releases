# Flagline

Interoffice messaging for Windows PCs. Every workstation has a name and can join groups;
send to one workstation, a group, or **Everyone**. No server: PCs on the office network
find each other automatically.

This repository holds the public downloads. Get the latest `Flagline.exe` from
**[Releases](../../releases/latest)**.

## What it does

* Incoming messages pop up as sticky notes that stay on top until they're right-clicked
  (which tells the sender "✓✓ seen"). Double-click a note to reply.
* **⚑ Urgent** messages appear big and red in the middle of the screen with a flashing border.
* **💬 Chat** windows for a quick back-and-forth.
* **🔒 Hidden details**: the note shows only the message; the details appear when it's clicked.
* Quick-message buttons, groups, Do not disturb, and messages that wait for a PC that's off.
* Traffic on the network and each PC's 90-day history are encrypted with the office key.

## Install on a PC

1. Download `Flagline.exe` and `firewall.bat` from the latest release and put both in the same
   folder that the PC's user can write to, e.g. `C:\Flagline\`. (Not `C:\Program Files`:
   automatic updates need to replace the file.)
2. Right-click `firewall.bat` → **Run as administrator** (once per PC). It lets Flagline accept
   traffic only from the local office network. If Windows Firewall still asks the first time
   Flagline runs, answer it, then run `firewall.bat` again.
3. Run `Flagline.exe` and open **⚙ Settings**: set the workstation name, its groups, the shared
   folder (e.g. `\\server\share\Flagline`) and the **Office key**. Use the same office key on
   every PC.

Flagline starts with Windows and sits in the system tray.

### Choosing the office key

The office key encrypts all Flagline traffic, so it is the lock on anything sent through Flagline.

* At least 16 characters. Best: 4–5 random, unrelated words.
* Not a name, birthday, the office name, or a password used anywhere else.
* Share it in person, not by email or text.
* Change it on every PC when someone who knew it leaves.

## Updating every PC

Copy the new `Flagline.exe` and `version.txt` from a release into the shared folder. Each PC
checks at start-up and every hour, swaps itself in and restarts. Open notes and waiting
messages are kept.

## Privacy

Flagline only talks to other PCs on the office network. Nothing is sent to the internet.
Without an office key set, a default key is used that is publicly known, so set your own.
