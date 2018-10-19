Overview:

Flask is a small and powerful web framework for Python. It's easy to learn and simple to use, enabling you to build your web app in a short amount of time.

Flask can be used for building complex, database-driven websites, starting with mostly static pages will be useful to introduce a workflow, which we can then generalize to make more complex pages in the future.


Installing Flask: 
	
	We can use virtualenv to install Flask.
	
	Virtualenv is a useful tool that creates isolated Python development environments where you 		can do all your development work.

	Install virtualenv:

		$ sudo pip install virtualenv

	Install Flask:
	
		After installing virtualenv, you can create a new isolated development environment:
			
			$ virtualenv flaskapp
		
		Here, virtualenv creates a folder, flaskapp/, and sets up a clean copy of Python 			inside for you to use. It also installs the handy package manager, pip.	
		
		Enter your newly created development environment and activate it so you can begin 			working within it.

			$ cd flaskapp
			$ . bin/activate
		
		*you can safely install Flask:

			$ pip install Flask
