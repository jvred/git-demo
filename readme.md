
$yum install git OR
$apt install git

VCS:
====
Centralized VCS – svn				
1. Local copy does not exist
2. Always need internet connectivity
3. Possibility of losing data
	

Distributed VCS – git, bitbucket
1. Data redundancy 
2. Data durability
3. Parallel work

Working dir: where we are working/updating files
Staging dir: where git added/tracking files
Remote: git pushed remote files



% git init
Initialized empty Git repository in /Users/vareredd/Documents/git/dir1/.git/

% git config user.name reddy_vasudeva@yahoo.com
% git config user.pass <password>   

NOTE: Omit --global to set the identity only in this repository
--global for current user


% git config --list --show-origin
file:/Library/Developer/CommandLineTools/usr/share/git-core/gitconfig   credential.helper=osxkeychain
file:config     core.repositoryformatversion=0
file:config     core.filemode=true
file:config     core.bare=false
file:config     core.logallrefupdates=true
file:config     core.ignorecase=true
file:config     core.precomposeunicode=true
file:config     user.name=reddy_vasudeva@yahoo.com
file:config     user.pass=<password>

% ls -la .git
total 24
drwxr-xr-x   9 vareredd  staff  288 Jul  3 15:34 .
drwxr-xr-x   4 vareredd  staff  128 Jul  3 15:24 ..
-rw-r--r--   1 vareredd  staff   23 Jul  3 15:24 HEAD
-rw-r--r--   1 vareredd  staff  197 Jul  3 15:34 config
-rw-r--r--   1 vareredd  staff   73 Jul  3 15:24 description
drwxr-xr-x  14 vareredd  staff  448 Jul  3 15:24 hooks
drwxr-xr-x   3 vareredd  staff   96 Jul  3 15:24 info
drwxr-xr-x   4 vareredd  staff  128 Jul  3 15:24 objects
drwxr-xr-x   4 vareredd  staff  128 Jul  3 15:24 refs


Error:
remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
https://levelup.gitconnected.com/fix-password-authentication-github-3395e579ce74

Error:
remote: Write access to repository not granted.
Select “repo” radio button while creating PAT
 <img width="524" alt="image" src="https://user-images.githubusercontent.com/68779362/184703269-1ff94a71-7efe-440e-afbf-b6f6a9f14139.png">


git remote add origin https://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@github.com/jvred/git-demo.git

####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

>> To undo merge files/content after pull

$git merge --abort [Since git version 1.7.4]

$git reset --merge [prior git versions]


Cherry-picking:
$git switch f1
$git add f1
$git commit -m “f1 add”
$git push origin f1

$git log
Copy commit id (eg:4e1115a890a90bb48cba3250e13c1ca42adf73fb)

$git switch main
$git cherry-pick 4e1115a890a90bb48cba3250e13c1ca42adf73fb
CONFLICT (modify/delete): f2 deleted in HEAD and modified in 4e1115a... adding. Version 4e1115a... adding of f1 left in tree.


$ls (show the new file,content here )

$git add f1

$git commit -m “f1add”

$git push origin main

====================
% git branch release
fatal: Not a valid object name: 'master'.
Git will not create master branch on new repo until you commit anything.
====================

