# Unit 18 PWA Homework: Online/Offline Budget Trackers

This was an interesting exercise to add offline functionality to our app.

The app worked by sending requests to the database when transactions are submitted. However, if the database was offline, these transactions wouldn't be recorded, and they would disappear when you reconnected.

To enable "offline data entry", we log these transactions in the indexedDB when the user submits them. These entries are still tallied and displayed while the user's offline. When the user reconnects and submits a new entry, the indexed DB

Issues/room for improvement:

* IF the user enters transactions, disconnects, and reopens the app, they won't see the offline entries until they submit a new transaction. This is because the application only checks the indexedDB when the user submits.
* Deployed but not connected to a remote Mongo database.
