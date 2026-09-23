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

git rm [file]
Deletes the file from your Mac and stages that deletion at the same time, so you don't need a separate git add step — just commit and push straight after.

// STARTING A BRAND NEW REPO FROM SCRATCH AND LINKING IT TO GITHUB //

Before any of this, go to GitHub.com and click "New repository". Give it a name, and leave "Add a README file" unticked. If GitHub creates a README for you, its history won't match your local folder's history, and your first push will get rejected until you merge them - easier to just start it empty and let your first push fill it in.

mkdir project-name
cd project-name
dotnet new console
git init
echo "bin/" > .gitignore
echo "obj/" >> .gitignore
echo ".DS_Store" >> .gitignore
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/username/repo-name.git
git push -u origin main

mkdir = create a new folder
init = start tracking this folder with git
.gitignore = a file that tells git which files/folders to never track
branch -M main = rename the default branch to "main"
remote add origin = link this folder to a repo on GitHub
push -u origin main = upload, and remember this as the default place to push to

mkdir project-name
Creates a new folder for the project. Skip this one if the folder already exists — for example if you ran "dotnet new console" first, that already made the folder for you.

cd project-name
Moves your Terminal session into that new folder, same idea as before — every command after this applies to this project specifically.

dotnet console
.NET CLI command that scaffolds a brand-new console project for you. It creates a Program.cs file with a starter "Hello, World!" line already in it, plus a .csproj file (the project config — target framework, any package references, etc.). Then the first time you build or run it, it also generates the bin/ and obj/ folders

git init
Turns the current folder into a git repository. This creates a hidden .git folder that git uses to track history. You only ever run this once, right at the start of a project.

echo "bin/" > .gitignore
Finder won't let you create a file that starts with a dot, so this is the easiest way to make one — echo prints the text in quotes, and > writes it into .gitignore, creating the file if it doesn't already exist. Only use a single > for the first line, since it overwrites anything already in the file.

echo "obj/" >> .gitignore
echo ".DS_Store" >> .gitignore
Same idea, but >> (two arrows) appends each line instead of overwriting the file, so you don't wipe out what you already added. What goes in here depends on the project - bin/ and obj/ are C# build folders that get regenerated every time you build, so they're never worth saving; .DS_Store is a hidden macOS file Finder creates in every folder, with nothing to do with your code. For a notes repo with no build process, you'd only need the .DS_Store line.

git add .
git commit -m "Initial commit"
Same add and commit as always. Because .gitignore already exists at this point, git skips bin/, obj/, and .DS_Store automatically and only stages your actual project files — so it all goes into one clean first commit. (If you were adding a .gitignore to a repo that already has commits in it, you'd add and commit just that file on its own instead — but for a brand new repo it can just ride along with everything else.)

git branch -M main
Renames your default branch to "main". Git's old default name was "master", but GitHub expects "main", so this makes sure your local branch name matches what GitHub is expecting before you connect the two.

git remote add origin https://github.com/username/repo-name.git
Connects your local folder to the empty repo you created on GitHub, so git knows where "upload" actually means. "origin" is just the standard nickname for that connection. Copy the URL from GitHub's "Quick setup" page on your new repo.

git push -u origin main
Works like a normal push, but the -u flag ("set upstream") tells git to remember that your local main branch should always sync with origin's main branch. After this first push, you can go back to just typing "git push" on its own.

If it ever asks for a username and password on push, use your GitHub username and a Personal Access Token as the password - GitHub doesn't accept your normal account password for this anymore.