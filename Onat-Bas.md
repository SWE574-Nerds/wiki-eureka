# Onat Bas's Personal Log

## Week 1

- Met with the team-members. 
- We've decided on the project structure and how to go from the beginning.
- Researched W3C standards such as Web Annotation Model and RDF.
- I think It's a better idea to do prototyping and get into the actual
work to understand things better, rather than just talking about it, That's why
I experimented with my findings on RDF and Web Annotation Model.
  - I've created an ontotext provided GraphDB 8 instance on AWS. With some example
data I found on the internet, experimented a bit. Then, I experimented with the sample
JSON-LD data I found on the Web Annotation Model documentation. 
  - This helped me understand clearly how to manage this data, what are the strong
and weak points of using this standard. I feel condifent that this way we've found
out is a good technical place to begin from.
- Wrote about the contribution guidelines and the project documentation structure.


## Week 2

- This week's plan is to get the requirements ready as soon as possible and also create some mockups.
- I've written the requirements to the best of my abilities. Still WIP, but It looks ok for now.
- I've created mockups for 

   a. Signup

   b. Home page

   c. First login page

   d. Used home page (home page with content)

   e. Living history page (Annotated, not-annotated, being annotated)
- I've used balsamiq for creating the mockups. The png files and json files for balsamiq mockups are 
added seperately. I also included the balsamiq project file.
- These efforts needs to be discussed by the team so I opened a discussion issue for the team to review
the mockups and give feedback. Hopefully these mockups will help us better design the application.


## Week 3

- We have requirements defined enough to start working on backend features.
- We've decided on using the following technologies for backend:
	a. DigitalOcean - for Hosting

	b. Docker - for Deployment

	c. PostgreSQL - for application DB

	d. GitFlow - for git workflow

- I've created the skeleton project using these technologies. Backend project is created in such a
way the application will run in containers orchestrated with docker-compose. 
- Postgres binding is established, the DB that's being used is also created via docker-compose. 
- Class diagram is being created. Use-case diagrams are opened for discussion in github issues.
