---
started: 2022-01-12 
finished:
rating:
---
Status: #📥
Tags: 
Links: [[+ Videos]]
___
# + Learn the MERN Stack - Full Tutorial for Beginners
> [URL]()

## Notes
### Tinder App
npx create-react-app {name}
- Map things out through comments
- rfce for react export

#### Express
Used to create server
- Seperate folder,  `app-backend`
`git init`
`npm init`
- set main to `server.js`

- node doesn't naturally have import
	- import in package through `'type:' "module"`
	- in scripts type `"start": "node server.js"`
	- put all logic in `server.js`

- `npm i express mongoose`
- import both
MongoDB
- Atlas, create cluster

#### Backend
App Config
- create port 
	- `const app = express();`
	- `const port = process.env.PORT || 8001;`
- copy the connection and put it in app config
	- `const connection_url = {link}`
	- update details (user, pass, dbname)

Middlewares
DB Config
`mongoose.connect(connection_url, {
	use`
API Endpoint
Listener

Sudo npm i -g nodemon

Mongoose to create structure for each database object

express app commands
get to grab
post to upload data

statuses
500 - internal server error
201 - created

#### Postman
- Create API using postman
- copy paste hardcoded thing
- rest client download
- `npm i cors`
	- import cors
		- `app.use(Cors());`
- put stuff through body section in postman using followed thing, send and see results
	- get requests don't have body though
#### Connecting Back to Front
- `npm i axios`
- Create axios file
- implement `useEffect` to fetch data
#### Deploying on heroku
- Create new app
	- Follow commands
- change axios to pull from heroku
#### Firebase
`firebase login`
`build`
y
## Thoughts/Questions
- 
___
# Backlinks
```dataview
list from [[+ Learn the MERN Stack - Full Tutorial for Beginners]]
```
___
Created:: 2022-01-12 21:01


