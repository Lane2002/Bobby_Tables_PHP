# Bobby_Tables_PHP
LEARN PHP
Bobby Tables
Collecting input from users is necessary, but nefarious users can use this as an opportunity to mess with things.

Just like the parents of Bobby Tables.

We’ve made a form for a user to create a profile on our site. We want to collect the user’s name, character, email and birth year. Our users have been having a field day with this and we need to clean up our form.

Let’s begin!

Tasks
15/15 Complete
Mark the tasks as complete by checking them off
What's in a name?
1.
Try submitting some HTML in the name input box, like <h1>HELLO</h1>.

Can you see how this could cause problems if another user was browsing this profile?


Stuck? Get a hint
2.
We want to allow users to use HTML characters in their names, but we don’t want to interpret them.

Where we are assigning $name to the input value, use a built-in function to transform any HTML characters in the input into HTML entities.


Stuck? Get a hint
3.
Let’s also remove any leading or trailing whitespace from the name.

Use a built-in function for this.


Stuck? Get a hint
4.
We also want to prevent people impersonating other users. To do this, we need to check the name from the input against the contents of the array $existing_users.

Instead of assigning to the variable $name directly, assign the transformed value of the input to $raw_name.


Stuck? Get a hint
5.
Check if $raw_name is in $existing_users, using the built-in function in_array.

If it is, concatenate "This name is taken. <br>"; to $validation_error.

If it is a new name, assign $raw_name to $name.


Stuck? Get a hint
Strange characters
6.
We intend for users to be a wizard, mage, or orc. Even though the character is a radio button selection, users can set themselves to something besides these options!

Try this yourself by inspecting one of the options from the embedded browser (in Chrome, right click on one of the options, like “Wizard”, and inspect).

You can change the “value” for the option to a different string, like "puppy". Select that option and submit the form to see what happens.


Stuck? Get a hint
7.
Instead of assigning the character input to $character, save it to a new variable $raw_character so we can validate it.


Stuck? Get a hint
8.
Use the built-in function in_array to check if $raw_character is in the array ["wizard", "mage", "orc"].

If it is, assign $raw_character to $character.

If it isn’t, concatenate "You must pick a wizard, mage, or orc. <br>" to $validation_error.


Stuck? Get a hint
Emails that aren't emails
9.
We want to prevent users from entering email addresses that aren’t…. well… email addresses.

Begin by assigning the email input to a new variable $raw_email, so we can validate it.


Stuck? Get a hint
10.
Use a built-in PHP function to check if $raw_email is an email address.

If it is, assign $raw_email to $email.

If it isn’t, concatenate "Invalid email. <br>" to $validation_error.


Stuck? Get a hint
How old???
11.
We’re using the user’s birth year to display an age in the user’s profile. Try entering a birth year way in the future or past and see what happens.


Stuck? Get a hint
12.
Instead of assigning the birth year input to $birth_year directly, assign it to a new variable $raw_birth_year.


Stuck? Get a hint
13.
We’re going to use filter_var with some options to limit the range of years that users can submit.

Create an $options variable to set the minimum and maximum values to realistic years.

You can get the current year using date("Y").


Stuck? Get a hint
14.
Add a check to ensure that $raw_birth_year is an integer in the range defined by $options.

If it is, assign $raw_birth_year to $birth_year.

If it isn’t, concatenate "That can't be your birth year. <br>" to $validation_error.


Stuck? Get a hint
Great!
15.
Congratulations, you should now have a form that is mostly impervious to ill intentioned users!

If you’d like some more practice, consider implementing the following:

Mages have to be born on leap years
Names must all start with lowercase characters
Emails must end in .com
