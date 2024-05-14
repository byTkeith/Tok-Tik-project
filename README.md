# TokTik: A Simple Social Media Application

## Overview

TokTik is a simple proof-of-concept replica of some functionality found in social media applications like TikTok. It uses Binary Search Trees (BSTs) to manage user accounts and posts. The application assumes that data is stored in memory while performing various functions on-demand.

## Features

1. **Find Profile Description for a Given Account**
   - Given an account name, retrieve the associated profile description.
2. **List All Accounts**
   - Display all user accounts (in any order).
3. **Create an Account**
   - Add a new user account with an account name and profile description.
4. **Delete an Account**
   - Remove an existing user account.
5. **Display All Posts for a Single Account**
   - Show all posts associated with a specific account (newest posts first).
6. **Add a New Post for an Account**
   - Create a new post for a user account, including a title, video clip filename, and number of likes.
7. **Load Actions from Disk**
   - Process a file containing Create and Add actions to initialize accounts and posts.
8. **Quit**
   - Exit the application.

## Usage

1. Compile Java code:
   ```
   javac -cp bin TokTik.java
   ```

2. Run the application:
   ```
   java -cp bin TokTik
   ```

3. Follow the menu prompts to interact with the application.

## Implementation Details

- Use a Binary Search Tree (BST) to store user accounts.
- Each account has three data fields: account name, profile description, and a list of posts.
- Posts include a title, video clip filename, and number of likes.

## Loading Actions from Disk

The application processes a file with lines in the following format:

```
Create hussein The lecturer dude.
Add hussein video34.mpg 34 Yet another video of cats
Add hussein video45.mpg 53 Omg more video of cats
```

- The first word indicates the action (Create or Add).
- Account names and video filenames are single words with no spaces.
- The integer after the filename represents the number of likes.
- The rest of each line contains the description or title.


## Incremental Development

Started by creating a data structure for account names and descriptions. Then added functions related to posts. Finally, implemented loading from an external file.

