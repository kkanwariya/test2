# On your bitbucket accounts

1. Create ssh key (with passphrase) on your local machine and upload
   your key.

2. Fork the ppk-teach/tools repository

3. Make a local clone (i.e. on your machine) of your fork created in
   step 2.

# Git

1. Clone a popular repository like https://github.com/jquery/jquery on
   your machine and do some standard git commands on some repositories.

   * git log
   * git branch
   * git remote -v
   * git blame some file # figure out what it does.

2. Create a new git repository and add a Readme file and commit.

3. Branch and merge.

   * Create a topic branch and make some changes on it
   * Merge topic to master using
	 - fast forward
	 - without fast forward (i.e. add on merge flag --no-ff)

   What is the difference in the two cases (check with a graphical
   git browser.

   * Create two branch topic1 and topic2 and do different things in
	 each. Merge them back to master

   * Try out 3.3 with conflicting changes (change the same line of a
	 file differently). See what happens at merge.

4. Create a remote branch and fetch stuff.

5. Try out the fetch/review/merge cycle with some dummy repositories.

# Other tools.

1. Poke around any sufficiently complicated git repository with
   gitk, tig etc

2. Emacs users try magit-mode
