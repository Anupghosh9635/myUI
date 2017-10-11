# my_ui with a Node server 
 

1. Move the root React app files (including dotfiles) into a `ui/` subdirectory

    ```bash
    mkdir ui
    git mv [!ui]* ui/
    # You'll see "fatal: Not a git repository"; let's fix that error
    mv ui/.git ./
    ```
1. Create a root [`package.json`](package.json), [`server/`](server/), & [`.gitignore`](.gitignore) modeled after the code in this repo
1. Commit and deploy ♻️
  
    ```bash
    git add -A
    git commit -m 'Migrate from my_ui-buildpack to Node server'
    git push heroku master
    ```
  

## Local Development

### Run the API Server

In a terminal:

```bash
# Initial setup
npm install

# Start the server
npm start
```


### Run the React UI

The React app is configured to proxy backend requests to the local Node server. (See [`"proxy"` config](ui/package.json))

In a separate terminal from the API server, start the UI:

```bash
# Always change directory, first
cd ui/

# Initial setup
npm install

# Start the server
npm start
```
