### 1.5 Generate a Rails application with Webpacker + React.

Create a new directory. 
```
mkdir react-on-rails
```
`react-on-rails` is the directory's name.

Open the directory.
```
cd react-on-rails
```

Generate a Rails application inside the directory.
```
rails new . --webpack=react
```

![Generate a Rails application with Webpacker + React](/README/images/1-5-generate-a-rails-application-with-webpacker-react.gif)

![Tree Logo](/README/images/1-5-tree-logo.png)

![Optional](/README/images/optional.png) Install tree on Mac using the `Homebrew`.
```
brew install tree
```

![Optional](/README/images/optional.png) Display the repository's tree directory.
```
tree -L 1
▶ .
  ├── Gemfile
  ├── Gemfile.lock
  ├── README.md
  ├── Rakefile
  ├── app
  ├── babel.config.js
  ├── bin
  ├── config
  ├── config.ru
  ├── db
  ├── lib
  ├── log
  ├── node_modules
  ├── package.json
  ├── postcss.config.js
  ├── public
  ├── storage
  ├── test
  ├── tmp
  ├── vendor
  └── yarn.lock
```

Start the Rails's server.
```
bundle exec rails s
```

Display the application on a web browser using the url below.
```
http://localhost:3000/
```

![Start the Rails's server](/README/images/1-5-start-the-rails-server.gif)
