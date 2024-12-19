### `README.md`


# Free Fire Info API Integration

This package provides a simple way to fetch player data from the BD Games API using a player's `loginId` (such as a phone number or account ID).

## Installation

You can install the package via npm:

```bash
npm install free-fire-apis
```

## Usage

### Get Player Data

To fetch player data, use the `uid` function by providing the player's `loginId` (which can be their phone number or account ID). 

```javascript
const { uid } = require('free-fire-apis');

const loginId = '6605263063'; // Replace with a valid login ID

uid(loginId)
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error('Error fetching player data:', error.message);
  });
```

### Example Output

If the request is successful, you will get player data like the following:

```javascript
{
  Region: "BD",         // Player's region (e.g., BD for Bangladesh)
  Nickname: "PlayerNick", // Player's in-game nickname
  Uid: "6605263063",    // Provided loginId
  Author: "IMRAN AHMED"  // Author's name (can be modified)
}
```

### Error Handling

In case of an error (such as an invalid `loginId` or network issues), the promise will reject and provide an error message.

```javascript
Error fetching player data: [error_message]
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```


### Final Thoughts:
- Be sure to update any parts of the README that may change in the future, such as the author name or specific details about how the API works.
- If you plan to update or version the package, make sure to keep this README file in sync with the changes.
