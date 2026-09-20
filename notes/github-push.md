cd ~/Documents/csharp-notes
git status
git add .
git commit -m "Describe what you changed"
git push

cd = go to the right folder
status = see what's changed
add = select what to save
commit = save it locally with a note
push = upload it to GitHub

cd ~/Documents/csharp-notes
cd stands for "change directory" - it moves your Terminal session into that folder so any git commands you run apply to this project, not wherever you happened to be before. The ~ is shorthand for your home folder, so this means "go to Documents, then into csharp-notes".

git status
This shows you the current state of your working directory comapred to your last commit - essentially "What has git noticed has changed since I last saved a snapshot?" It doesn't stage or save anything; it's purely informational, safe to run any time, as often as you like.

git add .
Stages your changes - tells git "include everything I've edited in this folder in the next snapshot." The . means "this folder and everything inside it." Nothing is saved permanently yet; it just moves your edited filed into a holding area (the staging area) ready to be committed.

git commit -m "Describe what you changed"
Takes whatever's staged and saves it as a permanent snapshto in your local project history, with a message explaining what changed. This is only saved on your Mac at this point - GitHub doesn't know about it yet. -m stands for message - it lets you attaach your commit message directly on the command line, right after the flag, in qoutes.
If you wanted multiple lines of messsages you can either add more -m "Text here" or simply not include -m and it will open a text editor where you can type your message.

git push
Uploads your new commit(s) from your Mac up to GitHub, syncing the remote copy with your local one. This is the step that actually makes the change visible on github.com.

git restore --staged .
This un-stages everything (moves it back to exactly the state before staging). Nothing gets deleted or lost - it only affects what's staged for the next commit.
The . can be replaced with specific file if needed.