# my_ui with a Node server 
 
  

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
