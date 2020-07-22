# API Authentication using NodeJs

This is an Authentication API using JWT's that you can plug inside your current project or you can start with a new one. Email & Password is used for authentication.

The API based on Node.js, Express, MongoDB & Redis, following the **MVC pattern** i.e. Model ~~View~~ Controller.

**Mongoose** is used for storing Users in Database.
**Redis** is used for storing Refresh Tokens - to validate them as well at the same time Blacklisting them.

The application is **production ready**.

---

## To start setting up the project

Step 1: Clone the repo

```bash
git clone https://github.com/trulymittal/API-Authentication-NodeJs.git
```

Step 2: cd into the cloned repo and run:

```bash
npm install
```

Step 3: Put your credentials in the .env file.

```bash
PORT=3000
MONGODB_URI=mongodb://localhost:27017
DB_NAME=YOUR_DB_NAME
ACCESS_TOKEN_SECRET=GENERATE_FROM_GENERATE_KEYS_FILE_IN_HELPER
REFRESH_TOKEN_SECRET=GENERATE_FROM_GENERATE_KEYS_FILE_IN_HELPER
```

Step 4: To generate 256-bit keys for JWT

```bash
node ./helpers/generate_keys.js
```

Step 5: Install Redis (Linux Ubuntu)

```bash
sudo apt-get install redis-server
```

Step 6: Run Redis Server (Linux Ubuntu)

```bash
redis-server
```

Step 7: Install MongoDB (Linux Ubuntu)

See <https://docs.mongodb.com/manual/installation/> for more infos

Step 8: Run Mongo daemon

```bash
sudo service mongod start
```

Step 9: Start the API by

```bash
npm start
```

Step 10 (Optional): Change the expiration time of Access Token and Refresh Token according to your needs by going inside the **`./helpers/jwt_helper.js`** file.

## Author

- [**Truly Mittal**](https://trulymittal.com)

## Contribute

You can fork this repo and send me a PR.

## License

This project is licensed under the MIT License.
