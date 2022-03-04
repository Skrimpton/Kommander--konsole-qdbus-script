# Kommander--konsole-qdbus-script
### Konsole (KDE terminal) wrapper script for qdbus commands.

THIS IS A WORK IN PROGRESS, MADE BY AN IDIOT (ME)


Usage examples



kommander

  Without arguments kommander displays a list of currently open konsole-windows and -sessions



kommander 1 ls

  session 1 in the current window will execute <ls>-command



kommander 1 ls org.kde.konsole-<PID>

  Execute <ls>-command in session 1 of the window refrenced

  (org.kde.konsole-<PID> can also be the first argument)



kommander + | kommander split | kommander 1 ls | kommander 2 htop

  Open new konsole window, split it's view into 2 sessions vertically, execute <ls> in left split-view and <htop> in right.



kommander size <HEIGHT> <WIDTH> (org.kde.konsole-<PID>)

  Resize current/given window using wmctrl



kommander size <VERTICAL POS> <HORIZONTAL POS> <HEIGHT> <WIDTH> (org.kde.konsole-<PID>)

  Place on screen and resize current/given window using wmctrl



kommander id (org.kde.konsole-<PID>)

  List and identify the current sessions in the current/given window by executing <echo this is session X> in the session



kommander id list (org.kde.konsole-<PID>)

  List the current sessions in current/given window



kommander window

  Returns the current window's qdbus refrence



kommander <session> kill

  Perform kill -SIGINT (same as pressing ctrl+c) on the current process running in the given session



kommander kill all

  Perform kill -SIGINT on all running processes in all other sessions, in the current window



kommander kill all windows

  Perform kill -SIGINT on all running processes in all other sessions, in all windows



kommander clear all

  Sends clear command to all other sessions in current window, if ps -p says "zsh" is the currently running process



kommander clear all windows

  Sends clear command to all other sessions in all windows,  if ps -p says "zsh" is the currently running process



kommander profile (org.kde.konsole-<PID>)

  Select a profile for the current session from the list of available konsole profiles



kommander <SESSION NUMBER> profile (org.kde.konsole-<PID>)

  Select a profile for the given session from the list of available konsole profiles

