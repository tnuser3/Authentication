# Authentication
## Advanced Authentication for .NET, C, C++, and Unity Applications
- Security is our top priority. We ensure that both your data and your users' data are protected using industry-standard encryption and sanitization practices. Our API is flexible, accepting GET, multipart, and JSON data, so you don't need to worry about the format of -your requests—just focus on building great applications.
- This GitHub repository will regularly change as its being developed. Be sure to check back regularly for updates.
## Shortform Endpoints
### 1. POST/GET `/api/blacklist/`
- **Description**: Blacklists a given key.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): The key to be blacklisted.
### 2. POST/GET `/api/unblacklist/`
- **Description**: Unblacklists a given key.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): The key to be unblacklisted.
### 3. POST/GET `/api/clearData/`
- **Description**: Clears all stored data on a given key.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): Given key to clear data of.
### 4. POST/GET `/api/createKey/`
- **Description**: Generates keys.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `amount` (required): Amount of keys to generate (MAX 20,000).
### 5. POST/GET `/api/deleteKey/`
- **Description**: Deletes a given key.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): Target key to delete.
### 6. POST/GET `/api/discordBlacklist/`
- **Description**: Blacklists a target key based on the connected discord account.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `id` (required): Target discord userID connected to a key to blacklist.
### 7. POST/GET `/api/discordUnblacklist/`
- **Description**: Unblacklists a target key.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `id` (required): Target discord userID connected to a key to unblacklist.
### 8. POST/GET `/api/getAllKeys/`
- **Description**: Gets all registered keys owned by a target privateKey.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
### 9. POST/GET `/api/getAllSessions/`
- **Description**: Gets all sessions.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
### 10. POST/GET `/api/getKeyInfo/`
- **Description**: Gets all info of target key.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): Target key to retrieve the data of.
### 11. POST/GET `/api/getUserInfo/`
- **Description**: Gets all info of target key connected to a user.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `id` (required): Target discord userID to get key info.
### 12. POST/GET `/api/globalVar/createVar/`
- **Description**: Creates a server sided variable that you can retrieve from your application.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `object` (required): Object you want to store in the variable.
### 13. POST/GET `/api/globalVar/deleteVar/`
- **Description**: Deletes a server sided variable that you can retrieve from your application.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `id` (required): The ID of the target variable you want to delete.
### 14. POST/GET `/api/globalVar/getVar/`
- **Description**: Retrieves a server sided variable with stored information inside.
- **Parameters**:
  - `privateKey`: The private key given upon registering
  - `publicKey`: The public key given upon registering
  - `id` (required): The ID of the target variable you want to retrieve.
  - **Note**: At least one `publicKey` or `privateKey` must be provided.
### 15. POST/GET `/api/globalVar/setVar/`
- **Description**: Sets the object stored in a target variable.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `id` (required): The ID of the target variable you want to edit.
  - `data` (required): The object you want to set the variable to.
### 16. POST/GET `/api/nonce/createSession/`
- **Description**: Generates a session.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `forKey` (required): The target key you want to link the session to.
### 17. POST/GET `/api/nonce/deleteSession/`
- **Description**: Deletes a target session.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `session` (required): The id of the target session.
### 17. POST/GET `/api/nonce/validateSession/`
- **Description**: Validates a target session.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `session` (required): The id of the target session.
  - `key` (required): The key the target session is linked to.
### 18. POST/GET `/api/redeemKey/`
- **Description**: Redeems a target key (Links to discord account).
- **Parameters**:
  - `privateKey`: The private key given upon registering
  - `publicKey`: The public key given upon registering
  - `key` (required): The target key you want to link to the given ID.
  - `id` (required): The target discord userID you want to link to the given key.
  - **Note**: At least one `publicKey` or `privateKey` must be provided.
### 19. POST/GET `/api/resetHwid/`
- **Description**: Resets all locked IDs to the given key.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): The target key to reset the locked IDs of.
### 20. POST/GET `/api/resetIP/`
- **Description**: Clears all saved ips of the given key.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): The target key to reset the ips of.
### 21. POST/GET `/api/addHwid/`
- **Description**: Adds a given id to the target key's locked ID array.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): The target key to add the HWID to.
  - `value` (required): The id you want to ad.
### 22. POST/GET `/api/addIP/`
- **Description**: Adds a given ip to the target key's ip array.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): The target key to set the IP of.
  - `value` (required): The value you want to set the IP to.
### 23. POST/GET `/api/deleteIP/`
- **Description**: Deletes a given ip in a target key's IP array.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): The target key to remove the IP of.
  - `value` (required): The value of the ip you want to remove.
### 24. POST/GET `/api/deleteHwid/`
- **Description**: Deletes a given hwid in a target key's locked ID array.
- **Parameters**:
  - `privateKey` (required): The private key given upon registering
  - `key` (required): The target key to remove the HWID of.
  - `value` (required): The value of the id you want to remove.
