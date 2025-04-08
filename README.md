# jira-user-deletion-script
 Jira Removal Script
This Python script allows you to mass delete Jira users when only given a list of emails.It checks accidentally Migrated Users from Org 1 and then sees if they are in Org 2. This needs the Jira Admin API because we need to query specific user information and perform admin level actions across 2 Jira "Orgs". This is a pretty niche script but it saved me and my coworkers a lot of headache.
 It uses the Atlassian API to:

Read emails from a CSV file.
Extract the username (everything before @ in each email address).
Search for users based on that username in Organization 1 (ORG_ID).
Fetch detailed user information from Organization 2 (ORG_ID_2).
Print user details to the console for confirmation.
Optionally delete users (currently commented out for safety).

Functions
extract_username(email): Extracts the username from an email.
read_emails_from_csv(file_path): Reads emails from a specified CSV file.
search_user(username): Searches for a user in ORG_ID based on the username.
get_user_details(account_id): Fetches user details from ORG_ID_2 using the account ID.
main(): The main function that orchestrates the entire process.

