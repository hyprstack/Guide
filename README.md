#GitHub command guide for beginners

--------------------------------------

This is meant to be a very basic and easy to follow guide to help those who are just leanrning to use the command line tool to work on GitHub. 

To create a _repository_, also called a __repo__ for short, you will either have to do this manually at the [GitHub](https://github.com/) website or by using the GitHub application that you can download [here](https://windows.github.com/) for Windows.

Once you have created the repo, open your _powershell_ (for windows) or command line for Mac and change directory to that of the previously created file. 
From here you can start to add documents to your file.

In the Windows powershell when changing directory you will want it to display the following message \[master .....\] ....__This is good!__ 

------------------------------------------

##For a newly created file

1. Now you can type the _init_ command to initialise or access the file.
	Type: `git init FILE_NAME`
	This allows you to now create documents in your file.

2. To create documents use the _touch_ command. This will look for an existing document in the file and will create one if none are found. The parameter of _touch_ will determine what or which file you want to create.
	The README document is the first document one should create in a _repo_ and I will use README as an example using _touch_. 
	Type: `touch DOCUMENT_NAME.type`
	e.g: `touch README.md` _md_ stands for _marked down text_

3. Before you continue using the command line, open your newly created document with your text editor (notepad, sublime, etc.) and write the body of your document (e.g README.md). Then save it!

4. Using the command line or powershell again literally add the file to your local repository on your computer. To do that we will use the _add_ command.
	Type: `git add DOCUMENT_NAME.type`
	e.g: `git add README.md`
	This will make Git notice the document is there.

5. Now take a _snapshot_ of the __project__ by using the _commit -m_ command.
	This will display the message that other users will see when you either make a change to your repository or add something for the first time. It's a description of what you did. This is __important__ because it allows readers to quickly determine what was changed when there is a great amount of code in a single file.
	Type: `git commit -m "Message"`

6. Now check to see if your local repository is connected to your GitHub repository by using:
	`git remote -v`
	If there is a connection this command will yield a list of all the remote origins your local repository knows of. It should be listed twice, which means it is available to _push_ info to and _fetch_ info from.
	If nothing is displayed then type:
	`git remote add origin https://github.com/YOUR_USERNAME/YOUR_PROJECT_NAME.git` _YOUR\_USER\_NAME_ and _YOUR\_PROJECT\_NAME_ should be replaced your actual username on GitHub and the name of your project. 

7. The nest step is to send all of this to GitHub so other users can read your files. To do this use the _push_ command.
	Type: `git push` __SIMPLE!__

	If this produces an error type the following instead (Note that consequent commands using the _push_ command will require only `git push`):
	`git pust -u origin master`

8. THAT'S IT! 

##BUT..... WHAT IF you want to change a file once you have logged-off or you want to add a new file to the repo?

First make the changes to your document and save them.

1. Change directory to the parent file using:
	`cd FILENAME`
	and then
	`git init FILENAME`

2. If you don't need to create a new document, skip this point. 
	If you need to create a new document, use:
	`touch DOCUMENT_NAME.type`
	Just like you did for the _README_ doc.

3. Use `git add DOCUMENT_NAME.type` to add it to the local repo.

4. Then use `git commit -m "Message"` to create a snapshot.

5. Check for the connection with GitHub if you are not sure that it already exists with `git remote -v`

6. Now send it to GitHub with `git push` or if there are any error displayed `git push -u origin master`

Hope this helps!
